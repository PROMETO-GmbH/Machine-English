# Template: Sensor-Integration in C – Architektur, Treiber und Testcases

**Framework:** CRAFT | **Level:** 4 | **Bereich:** Embedded Software

---

## Kontext

Dieses Template steuert die vollständige Integration eines Sensor-ICs in ein Embedded-C-Projekt auf einem Mikrocontroller. Es deckt die drei Phasen ab, die in der Praxis häufig unstrukturiert ablaufen: Architekturentscheidung, Treiberimplementierung und Verifikation. Die KI arbeitet eine explizite Strategie Schritt für Schritt ab und wartet nach jedem Schritt auf Bestätigung.

Der Platzhalter **[SENSOR]** steht für einen generischen I2C-Sensor (z.B. einen „Jelly Bean"-Sensor wie einen Temperatur-/Feuchtigkeitssensor mit Registerzugriff). Der Platzhalter **[MCU]** steht für den Ziel-Mikrocontroller (hier exemplarisch TI MSPM0).

---

## Template (zum Ausfüllen)

```
CONTEXT: Wir entwickeln eine Embedded-C-Firmware fuer den Mikrocontroller
[MCU, z.B. "TI MSPM0L1306, Cortex-M0+, 32 MHz, 32 KB Flash, 4 KB SRAM"].
Der bestehende Code nutzt [z.B. "TI MSPM0 SDK mit DriverLib, kein RTOS,
Bare-Metal, MISRA-C:2012 teilweise eingehalten"].
Wir integrieren den Sensor [SENSOR, z.B. "I2C-Temperatursensor mit
8-Bit-Registerinterface, 7-Bit-Adresse 0x48, Datenblatt liegt vor"].
Das Datenblatt beschreibt folgende Kernregister:
[Registerauszug einfuegen, z.B.:
  - 0x00: Temperatur MSB (Read)
  - 0x01: Temperatur LSB (Read)
  - 0x03: Config-Register (Read/Write, Default 0x60)
  - 0x04: One-Shot-Trigger (Write)]
Anforderungen: Messrate 1 Hz, Genauigkeit +/- 0.5 Grad C, Stromsparmodus
zwischen Messungen, Fehlerbehandlung bei I2C-Timeout und NACK.

ROLE: Du bist ein erfahrener Embedded-Software-Architekt mit Fokus auf
ressourcenbeschraenkte Mikrocontroller in C (C99). Du kennst TI DriverLib,
MISRA-C:2012 und schreibst sauberen, portierbaren HAL-Code. Du erklaerst
architektonische Entscheidungen kurz und praegnant.

ACTION: Arbeite die folgende Strategie Schritt fuer Schritt ab.
Praesentiere nach jedem Schritt das Ergebnis und warte auf explizite
Bestaetigung ("weiter" oder Korrekturfeedback), bevor du den naechsten
Schritt beginnst.

STRATEGIE:

Schritt 1: Architektur-Review
  - Schlage eine Softwareschichtung vor (HAL / Treiber / Applikation)
  - Definiere die Datei- und Modulstruktur (sensor_hal.h, sensor_drv.h/.c,
    app_temperature.c o.ae.)
  - Beschreibe die Schnittstellen zwischen den Schichten in Pseudocode
  - Benenne 2 Risiken und wie die Architektur sie adressiert

Schritt 2: HAL-Implementierung
  - Implementiere sensor_hal.h mit plattformunabhaengigem Interface
    (i2c_write, i2c_read, delay_ms, error_t)
  - Implementiere sensor_hal.c mit TI MSPM0 DriverLib als Backend
  - Fehlerbehandlung: Timeout (>10 ms), NACK, Bus-Fehler -> error_t-Codes

Schritt 3: Treiber-Implementierung
  - Implementiere sensor_drv.h mit oeffentlichem API:
    sensor_init(), sensor_read_temperature(), sensor_set_powermode()
  - Implementiere sensor_drv.c mit vollstaendigem Registerprotokoll
    gemaess Datenblatt
  - One-Shot-Messung, Power-Down zwischen Messungen
  - Alle Magic Numbers als benannte Konstanten (#define oder enum)
  - Kommentare auf MISRA-C:2012 Konformitaet hinweisen wo relevant

Schritt 4: Applikationsintegration
  - Zeige app_temperature.c mit 1-Hz-Messschleife (Timer-basiert oder
    Polling mit SysTick)
  - Anbindung an bestehende Projektstruktur (main.c Snippet)
  - Ausgabe der Messwerte ueber UART (printf-Ersatz fuer Bare-Metal)

Schritt 5: Testcases
  - Erstelle Unit-Tests fuer sensor_drv.c mit Mock fuer sensor_hal
    (kein Hardware-Zugang noetig)
  - Mindestens folgende Faelle:
    a) Normalbetrieb: Korrekte Temperaturberechnung aus Rohdaten
    b) I2C-Timeout: Fehlercode wird korrekt weitergegeben
    c) NACK bei falscher I2C-Adresse: Fehlerbehandlung greift
    d) Power-Down/Wake-Up-Sequenz: Korrekte Registersequenz
    e) Grenzwerte: Minimale und maximale Rohwerte des Sensors
  - Testframework: [z.B. "Unity / CMock" oder "einfache assert-basierte
    Tests ohne Framework"]

FORMAT: Pro Schritt: kurze Erklaerung der Entscheidung (max. 3 Saetze),
dann vollstaendiger, kompilierbarer C-Code in Codeblock. Dateinamen als
Ueberschrift ueber jedem Block. Keine Implementierung ohne vorherige
Erklaerung.

TARGET: Embedded-Software-Entwickler mit 2-5 Jahren Erfahrung in C,
kein Vorwissen zum spezifischen Sensor, aber vertraut mit I2C und
Mikrocontroller-Peripherie.
```

---

## Ausgefülltes Beispiel: Jelly-Bean-Temperatursensor auf TI MSPM0L1306

```
CONTEXT: Wir entwickeln Bare-Metal-Firmware fuer den TI MSPM0L1306
(Cortex-M0+, 32 MHz, 32 KB Flash, 4 KB SRAM, TI MSPM0 SDK 2.x mit
DriverLib). Wir integrieren einen generischen I2C-Temperatursensor
(intern "Jelly Bean" genannt) mit folgenden Eigenschaften:
  - I2C, 7-Bit-Adresse 0x48, Fast Mode (400 kHz)
  - Register 0x00: Temp MSB | Register 0x01: Temp LSB
    (12-Bit-Wert, MSB-first, LSB[3:0] = Nachkommastellen * 0.0625 Grad C)
  - Register 0x03: Config (Default 0x60 = Continuous, 12-Bit)
  - Register 0x04: One-Shot (Write 0x01 triggert Einzelmessung)
  - Stromsparmodus: Config-Bit 8 = 1 -> Shutdown Mode
Anforderungen: 1-Hz-Messung, +/-0.5 Grad C, Shutdown zwischen Messungen,
Fehlerbehandlung bei I2C-Timeout (>10 ms) und NACK.

ROLE: Du bist ein erfahrener Embedded-Software-Architekt fuer
ressourcenbeschraenkte Cortex-M0+-Systeme in C99. Du kennst
TI MSPM0 DriverLib und schreibst portierbare HAL-Architektur.

ACTION: Arbeite die fuenf Schritte der Strategie ab. Warte nach jedem
Schritt auf Bestaetigung.

STRATEGIE: [wie im Template oben]

FORMAT: Kurze Entscheidungserklaerung + vollstaendiger C-Code je Schritt.

TARGET: Embedded-Entwickler mit I2C-Grundkenntnissen, kein Vorwissen
zum Sensor oder MSPM0-DriverLib.
```

---

## Hinweise zur Anwendung

**Datenblatt-Auszug vorbereiten:** Die Qualitaet des generierten Codes steigt erheblich, wenn Registernamen, Adressen und Bitkonfigurationen direkt aus dem Datenblatt in den INPUT-Abschnitt eingefuegt werden. Vollstaendige Datenblatt-PDFs uebersteigen die Kontextlaenge der meisten KI-Modelle.

**Strategie anpassen:** Wer nur den Treiber benoetigt, kann Schritte 1 und 4 weglassen. Wer die Architektur bereits festgelegt hat, startet direkt bei Schritt 2.

**Schrittweise Ausfuehrung:** Das explizite Warten auf Bestaetigung zwischen den Schritten verhindert, dass die KI eine grosse Menge ungeprüften Codes auf einmal produziert. Jeder Schritt kann korrigiert oder angepasst werden, bevor der naechste beginnt.

**Testframework-Wahl:** Fuer MSPM0-Projekte ohne RTOS eignen sich Unity/CMock (portierbar, C99) oder einfache assert()-basierte Tests, die auf dem Host-PC laufen und die Hardware-HAL mocken.

---

*© PROMETO GmbH 2026 | www.prometo.ai | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/deed.de)*
