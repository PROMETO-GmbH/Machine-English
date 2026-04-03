# Template: Stabilitätsbewertung eines Operationsverstärker-Regelkreises

**Framework:** CRAFT | **Level:** 4 | **Bereich:** Elektronik

---

## Kontext

Die Stabilitätsanalyse rückgekoppelter Schaltungen mit Operationsverstärkern ist eine der anspruchsvollsten Aufgaben im analogen Schaltungsdesign. Phasenreserve, Verstärkungsreserve und Kompensationsstrategie müssen auf Basis von Datenblatt-Parametern und der konkreten Schaltungsarchitektur bewertet werden. Dieses Template führt die KI durch eine strukturierte Stabilitätsanalyse auf Basis eines vorliegenden Schaltplans und der Datenblätter der eingesetzten Chips.

---

## Template (zum Ausfüllen)

```
CONTEXT: Wir analysieren die Stabilität einer Operationsverstärkerschaltung
in [Anwendungskontext, z.B. "einem Motorstromregelkreis für einen
bürstenlosen DC-Motor in einem Haushaltsgerät"].

Schaltungstyp: [z.B. "invertierender Verstärker mit kapazitiver Last /
nicht-invertierender Integrator / PI-Regler / Transimpedanzverstärker"]

Topologie und Bauteilwerte aus dem Schaltplan:
- R1: [Wert, z.B. "10 kOhm, Feedback-Widerstand"]
- R2: [Wert, z.B. "1 kOhm, Eingangswiderstand"]
- C1: [Wert, z.B. "100 nF, Gegenkopplungskondensator"]
- Last: [z.B. "CL = 470 nF, RL = 100 Ohm"]
- Versorgung: [z.B. "+/-12 V symmetrisch"]

Relevante Datenblatt-Parameter des Operationsverstärkers [Typ einfügen]:
- Open-Loop-Verstärkung (DC): [z.B. "110 dB"]
- Einheitsverstärkungs-Bandbreite (GBW/ft): [z.B. "10 MHz"]
- Slew Rate: [z.B. "20 V/μs"]
- Open-Loop-Ausgangsimpedanz (Ro): [z.B. "75 Ohm"]
- Phasenreserve (unbelastet, Einheitsverstärkung): [z.B. "60°"]
- Eingangsstufen-Kapazität: [z.B. "Cin = 5 pF"]

Bekannte Probleme oder Beobachtungen: [z.B. "Einschwingüberschwinger
bei Sprungantwort, Oszillation bei kapazitiver Last > 1 nF beobachtet"]

ROLE: Du bist ein erfahrener Analogschaltungsentwickler mit Fokus
auf rückgekoppelte Verstärkerschaltungen und Regelkreisstabilität.
Du analysierst Schaltungen mit Bode-Plot-Methodik, kennst die
Auswirkungen kapazitiver Lasten und beherrschst Kompensationsstrategien
(In-Loop, Out-of-Loop, Snubber). Du erklärst Entscheidungen kompakt
und schlägst direkt umsetzbare Maßnahmen vor.

ACTION: Führe eine vollständige Stabilitätsanalyse in vier Schritten durch.
Präsentiere jeden Schritt einzeln und warte auf Bestätigung:

Schritt 1: Schleifenverstärkung und Polstellen
  - Berechne die Schleifenverstärkung T(s) = A(s) * Beta(s)
  - Identifiziere dominante Pole und Nullstellen der Rückkopplungsschleife
  - Bestimme die kritischen Frequenzen (Durchtrittsfrequenz, Phasendurchgang)

Schritt 2: Phasenreserve und Verstärkungsreserve
  - Berechne Phasenreserve (Ziel: > 45°, empfohlen > 60°)
  - Berechne Verstärkungsreserve (Ziel: > 10 dB)
  - Bewerte Stabilität unter Worst-Case-Bauteilstreuungen (+/-20%)

Schritt 3: Ursachenanalyse (falls instabil oder grenzwertig)
  - Identifiziere den dominanten Stabilitätskiller
    (kapazitive Last, parasitäre Kapazitäten, zu hohe Bandbreite)
  - Quantifiziere den Einfluss auf Phasenreserve

Schritt 4: Kompensationsempfehlung
  - Schlage mindestens zwei Kompensationsstrategien vor mit:
    Schaltungsänderung, neue Bauteilwerte, erwartete neue Phasenreserve
  - Empfehle die beste Option mit Begründung
  - Weise auf Auswirkungen auf Bandbreite und Slew Rate hin

FORMAT: Pro Schritt: Formel oder Herleitung (kompakt), Zahlenergebnis,
kurze Interpretation. Abschliessend: Zusammenfassung auf einer
halben Seite als Entscheidungsvorlage. Gleichungen in üblicher
Ingenieurnotation, keine LaTeX.

TARGET: Elektronikentwickler mit Grundkenntnissen in analoger
Schaltungstechnik und Regelkreistheorie, aber ohne Spezialisierung
auf Stabilitätsanalyse. Ergebnis wird im Design-Review präsentiert.
```

---

## Ausgefülltes Beispiel: PI-Stromregler mit kapazitiver Last an der Treiberstufe

```
CONTEXT: Wir analysieren die Stabilität eines PI-Stromreglers für
einen bürstenlosen DC-Motor (BLDC) in einer Waschmaschinen-Steuerung.

Signalkette: Shunt-Stromsensor → TLV9001 PI-Regler (Analog) →
PWM-Komparator (Dreieckssignal 20 kHz) → Gate-Treiber → MOSFET-Halbbrücke → Motor.
Der Motor ist eine induktive Last (ca. 1.5 mH, 0.8 Ohm Wicklungswiderstand).
Die kapazitive Last am Op-Amp-Ausgang stammt aus der Eingangskapazität
des PWM-Komparators und PCB-Leiterbahnen. Beobachtetes Problem:
Überschwinger > 20% bei Laststufen.

Schaltungstyp: Nicht-invertierender PI-Regler, Op-Amp-Ausgang treibt
Eingang des PWM-Komparators (kapazitive Last)

Bauteilwerte:
- R1: 10 kOhm (Integrator-Widerstand)
- R2: 100 kOhm (Proportionalanteil)
- C1: 10 nF (Integratorkondensator)
- Last am Op-Amp-Ausgang: CL = 2.2 nF (Komparator-Eingangskapazität
  + PCB-Streukapazität), RL = 1 kOhm (Eingangswiderstand Komparator)

OpAmp: TLV9001 (TI), Datenblatt-Parameter:
- GBW: 1 MHz
- Slew Rate: 2 V/μs
- Open-Loop Ro: 160 Ohm
- Phasenreserve (Einheitsverstärkung, unbelastet): 66°
- Versorgung: 3.3 V single supply

Beobachtung: Überschwinger ~25% bei Motoranlauf,
keine Dauerschwingung.

ROLE: Erfahrener Analogschaltungsentwickler, Fokus auf
Regelkreisstabilität, Kompensationsstrategien für kapazitive Lasten.

ACTION: Vier Schritte der Stabilitätsanalyse mit Bestätigung
zwischen den Schritten.

FORMAT: Formel + Zahlenergebnis + Interpretation pro Schritt,
Zusammenfassung als Design-Review-Vorlage.

TARGET: Elektronikentwickler, Design-Review-Präsentation.
```

---

## Ergänzende Hinweise

**Begriffsklärung: kapazitive Last im BLDC-Stromregelkreis:** In einer typischen BLDC-Stromregelung durchläuft das Signal mehrere Stufen: Stromsensor (Shunt oder Hall) → Op-Amp als PI-Stromregler → PWM-Modulator (Komparator mit Dreieckssignal oder dedizierter PWM-Controller-IC) → Gate-Treiber → MOSFET-Halbbrücke → Motor. Der Motor selbst ist eine induktive Last (Wicklungsinduktivität + Wicklungswiderstand). Die "kapazitive Last" im Sinne der Op-Amp-Stabilitätsanalyse entsteht am Ausgang des Operationsverstärkers durch die Eingangskapazität des nachgeschalteten PWM-Komparators oder PWM-Controller-ICs, typischerweise einige Pikofarad bis wenige Nanofarad, zuzüglich PCB-Leiterbahnkapazitäten. Diese Kapazität bildet zusammen mit dem Open-Loop-Ausgangswiderstand Ro des Op-Amp einen zusätzlichen Pol, der die Phasenreserve reduziert. Im Context immer die vollständige Signalkette benennen und die kapazitive Last dem richtigen Systemknoten zuordnen: nicht dem Motor, sondern dem Eingang der PWM-Stufe.

**Schaltplan-Daten strukturiert übergeben:** Je präziser die Bauteilwerte und Datenblatt-Parameter im Context, desto genauer die Stabilitätsaussage. Parasitäre Elemente (PCB-Leiterbahnkapazitäten, Steckverbindungsindukitivitäten) als Schätzwerte mit angeben, falls relevant.

**Grenzen der KI-Analyse:** Die KI arbeitet analytisch auf Basis der angegebenen Parameter. SPICE-Simulation und Messung am realen Prototyp bleiben unersetzlich für die finale Verifikation. Das Template liefert die analytische Grundlage und Kompensationsstrategie vor der Simulation.

---

*© PROMETO GmbH 2026 | www.prometo.ai | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/deed.de)*
