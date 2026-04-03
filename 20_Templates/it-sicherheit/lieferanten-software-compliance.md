# Template: Compliance-Bewertung von Lieferanten-Software

**Framework:** AIM | **Level:** 4 | **Bereich:** IT & Sicherheit

---

## Kontext

Seit UN R155 (UNECE WP.29) ist die Cybersecurity-Bewertung von zugelieferter Software verpflichtend fuer Fahrzeughersteller und deren Zulieferer. Dieses Template unterstuetzt die strukturierte Erstbewertung einer Softwarekomponente eines Lieferanten, bevor sie in die eigene Entwicklungsumgebung oder das Serienprodukt integriert wird.

---

## Template (zum Ausfüllen)

```
ACTOR: Du bist ein erfahrener IT-Sicherheitsbeauftragter und
Cybersecurity-Engineer in einem Tier-1-Zulieferer der Automobilindustrie.
Du kennst die Anforderungen aus UN R155, ISO/SAE 21434, TISAX und
MISRA aus aktiven Projekten. Du denkst in Risiken und
Handlungsempfehlungen, nicht in theoretischen Frameworks.

INPUT:
- Lieferant: [Name und Herkunftsland des Lieferanten]
- Komponente: [z.B. "AUTOSAR-BSW-Stack", "CAN-Stack", "OTA-Middleware"]
- Einsatzkontext: [z.B. "Steuergeraet fuer Bremssystem, ASIL-B"]
- Vorliegende Unterlagen: [z.B. "Produktdatenblatt, SBOM, Security-Summary"]
- Bekannte Abhaengigkeiten: [z.B. "OpenSSL 1.1.1, FreeRTOS 10.x"]
- Vertraglicher Rahmen: [z.B. "NDA vorhanden, kein Quellcode-Zugang"]
- Bewertungszeitraum: [z.B. "Ergebnis benoetigt bis 15. Mai"]

MISSION: Erstelle eine strukturierte Compliance-Bewertung der
Softwarekomponente mit:
1. Ampel-Bewertung (gruen/gelb/rot) fuer UN R155, MISRA-Konformitaet,
   TISAX-Relevanz und Open-Source-Risiken (Lizenz, bekannte CVEs)
2. Die drei groessten identifizierten Risiken mit Eintrittswahrscheinlichkeit
   und Auswirkung
3. Konkreten Nachforderungen an den Lieferanten (maximal 5 Punkte)
4. Empfehlung: Integration freigeben, bedingt freigeben oder ablehnen

Umfang: maximal 1 DIN-A4-Seite als Entscheidungsvorlage fuer den
Entwicklungsleiter.
```

---

## Ausgefuelltes Beispiel: OTA-Middleware eines asiatischen Zulieferers

```
ACTOR: Du bist ein erfahrener IT-Sicherheitsbeauftragter und
Cybersecurity-Engineer in einem Tier-1-Zulieferer der Automobilindustrie.
Du kennst UN R155, ISO/SAE 21434, TISAX und MISRA aus aktiven Projekten.

INPUT:
- Lieferant: Koreanischer Softwareanbieter, spezialisiert auf
  Automotive-Middleware, besteht seit 2015
- Komponente: OTA-Update-Middleware fuer Infotainment-Steuergeraete
- Einsatzkontext: Infotainment-ECU, kein direkter Safety-Bezug,
  aber Netzwerkzugang zum Fahrzeug-Backbone (CAN/Ethernet)
- Vorliegende Unterlagen: Produktdatenblatt, Security-Whitepaper,
  keine SBOM vorhanden
- Bekannte Abhaengigkeiten: cURL 7.68, mbedTLS 2.28, proprietaerer
  Signaturmechanismus (kein Standard)
- Vertraglicher Rahmen: NDA vorhanden, Quellcode-Einsicht gegen
  Aufpreis moeglich
- Bewertungszeitraum: Entscheidung bis naechsten Freitag erforderlich

MISSION: Erstelle eine strukturierte Compliance-Bewertung mit
Ampel-Bewertung fuer UN R155, MISRA, TISAX und Open-Source-Risiken,
den drei groessten Risiken, maximal 5 Nachforderungen an den
Lieferanten und einer klaren Freigabe-Empfehlung. Maximal 1 DIN-A4-Seite,
Entscheidungsvorlage fuer den Entwicklungsleiter.
```

---

## Haeufige Schwachstellen bei Lieferanten-Software

| Schwachstelle | Typisches Indiz | Massnahme |
|---------------|----------------|-----------|
| Fehlende SBOM | Keine Aussage zu Open-Source-Abhaengigkeiten | SBOM als Lieferpflicht vertraglich verankern |
| Veraltete Bibliotheken | cURL, OpenSSL aelter als 2 Jahre | CVE-Pruefung anfordern, Update-Prozess klaeren |
| Proprietaere Krypto | Eigener Signaturmechanismus ohne Audit | Wechsel auf NIST-konforme Algorithmen fordern |
| Kein Penetrationstest | Security-Whitepaper ohne externe Pruefung | Aktuellen Pentest-Bericht (max. 12 Monate) anfordern |
| Fehlende UN R155-Dokumentation | Kein CSMS-Nachweis | ISO/SAE 21434-Konformitaetserklaerung einfordern |

---

*© PROMETO GmbH 2026 | www.prometo.ai | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/deed.de)*
