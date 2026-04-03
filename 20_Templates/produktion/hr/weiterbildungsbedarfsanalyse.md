# Template: Weiterbildungsbedarfsanalyse für technische Teams

**Framework:** CRAFT | **Level:** 3 | **Bereich:** HR

---

## Kontext

Weiterbildungsbudgets sind begrenzt, der Kompetenzbedarf in technischen Teams wächst schneller als die Kapazität für Schulungen. Ohne strukturierte Bedarfsanalyse landen Weiterbildungsmaßnahmen nach Bauchgefühl oder lautem Zuruf, nicht nach strategischem Bedarf. Dieses Template führt die KI durch eine vollständige Skill-Gap-Analyse: von der Rollenanforderung über die Ist-Kompetenz bis zur priorisierten Maßnahmenempfehlung, abgestimmt auf das Budget und den Betriebskalender.

---

## Template (zum Ausfüllen)

```
CONTEXT: Wir führen eine Weiterbildungsbedarfsanalyse für das Team
[Teambezeichnung, z.B. "Embedded Software Entwicklung, 8 Personen"]
im Unternehmen [Name, Branche] durch.

Strategischer Hintergrund:
[z.B. "Umstieg von AUTOSAR Classic auf AUTOSAR Adaptive bis Q3,
neues Kundenprojekt erfordert ISO 26262 ASIL-C-Kompetenz ab Q2,
aktuell kein zertifizierter Functional-Safety-Engineer im Team"]

Rollen im Team und ihre Anforderungsprofile:
- Rolle 1: [z.B. "Senior Embedded Developer, 3 Personen:
  Soll-Kompetenzen: AUTOSAR Adaptive, C++17, ASPICE Level 2,
  Ist-Kompetenzen (Selbsteinschätzung): AUTOSAR Classic (Expert),
  C++11 (Fortgeschritten), ASPICE (Grundkenntnisse)"]
- Rolle 2: [z.B. "Testingenieur, 2 Personen:
  Soll: HIL-Testing, ISO 26262 Verifikation, CANoe
  Ist: SIL-Testing (gut), ISO 26262 (Grundkenntnisse), CANoe (keine)"]
- [weitere Rollen ergänzen]

Bewertungsskala für Ist-Kompetenzen:
[z.B. "0 = keine Kenntnisse, 1 = Grundkenntnisse, 2 = Anwender,
3 = Fortgeschritten, 4 = Experte / kann andere schulen"]

Rahmenbedingungen:
- Weiterbildungsbudget: [z.B. "12.000 Euro pro Jahr für das Team"]
- Verfügbare Tage pro Person: [z.B. "max. 5 Schulungstage/Jahr,
  keine Abwesenheit in Projektphasen Q1 und Q3"]
- Bevorzugte Formate: [z.B. "externe Zertifizierungen bevorzugt,
  E-Learning als Ergänzung akzeptiert, keine mehrtägigen
  Abwesenheiten im Schichtbetrieb"]
- Interne Ressourcen: [z.B. "Senior-Kollege kann intern zu
  AUTOSAR Classic schulen, kein dedizierter Trainer vorhanden"]

ROLE: Du bist ein erfahrener HR Business Partner und
Organisationsentwickler mit Branchenkenntnissen in der Automobil-
und Elektronikindustrie. Du kennst den Weiterbildungsmarkt für
technische Fachkräfte (TÜV, VDI, PerForma, Vogel, herstellerspezifische
Akademien), kannst Kosten realistisch einschätzen und weißt,
welche Zertifizierungen von OEMs und Tier-1-Kunden anerkannt werden.
Du denkst in Prioritäten: Was ist geschäftskritisch, was ist
nice-to-have, was lässt sich intern abdecken?

ACTION: Erstelle die Bedarfsanalyse in vier Schritten.
Präsentiere jeden Schritt einzeln und warte auf Bestätigung:

Schritt 1: Skill-Gap-Matrix
  - Erstelle eine Tabelle: Kompetenz | Soll | Ist (Durchschnitt Team)
    | Gap (Differenz) | Anzahl betroffene Personen
  - Markiere kritische Gaps (geschäftskritisch oder regulatorisch
    verpflichtend) gesondert
  - Identifiziere Kompetenzen, die intern weitergegeben werden können
    (interner Wissenstransfer als günstige Alternative)

Schritt 2: Priorisierung der Gaps
  - Bewerte jeden Gap nach zwei Kriterien:
    Dringlichkeit (Zeitdruck durch Projekt oder Norm) und
    Auswirkung (Risiko bei Nicht-Schließung: Projektverzug,
    Compliance-Verstoß, Kundenverlust)
  - Ergebnis: Prioritätsmatrix (hoch/mittel/niedrig) mit Begründung
  - Empfehle, welche Gaps im laufenden Jahr zwingend adressiert
    werden müssen und welche auf das Folgejahr verschoben werden können

Schritt 3: Maßnahmenplan
  - Pro priorisiertem Gap: empfohlene Maßnahme mit
    Format (externe Schulung / Zertifizierung / E-Learning /
    interner Workshop / Mentoring), Anbieter-Vorschlag,
    Dauer in Tagen, Kosten (Schätzung), empfohlener Zeitraum,
    Zielgruppe (alle / Rolle X / Einzelperson)
  - Gesamtkosten-Übersicht: Budget-Soll vs. Budget-Ist
  - Falls Budget überschritten: Priorisierungsvorschlag
    mit Streichempfehlung und Begründung

Schritt 4: Erfolgsmessung und Nachverfolgung
  - Definiere für jede Maßnahme ein messbares Ziel:
    [z.B. "Zertifikat vorhanden", "kann Aufgabe X selbstständig
    ausführen", "Code-Review-Fehlerquote sinkt um Y%"]
  - Schlage Zeitpunkte für Transfergespräche vor
    (4-6 Wochen nach Schulung)
  - Empfehle ein einfaches Nachverfolgungsformat
    (Tabelle, Skill-Matrix-Update, Jahresgespräch-Integration)

FORMAT: Tabellen für Skill-Gap-Matrix, Prioritätsmatrix und
Maßnahmenplan. Fließtext nur für Begründungen und Empfehlungen.
Kosten in Euro, Dauer in Tagen. Ausgabe auf Deutsch,
geeignet als Vorlage für Geschäftsführungs-Präsentation
und HR-Jahresplanung.

TARGET: HR Business Partner und Teamleiter in technischen
Abteilungen, die das Ergebnis der Geschäftsführung und dem
Betriebsrat vorlegen. Das Dokument muss nachvollziehbare
Priorisierungen enthalten und Budgetentscheidungen begründen.
```

---

## Ausgefülltes Beispiel: Embedded-Software-Team, AUTOSAR-Transition

```
CONTEXT: Weiterbildungsbedarfsanalyse für das Embedded-Software-Team
(6 Entwickler, 1 Testingenieur) bei Zulieferer Bauer Automotive,
Entwicklungsstandort Ingolstadt.

Strategischer Hintergrund: OEM-Auftrag Plattform-ECU ab Q3
erfordert AUTOSAR Adaptive und ISO 26262 ASIL-B-Nachweis.
Aktuell kein zertifizierter Functional-Safety-Engineer im Team.
Ohne Nachweis droht Projektverlust (Umsatz 2.4 Mio. Euro/Jahr).

Rollen und Kompetenzprofile:
- Senior Embedded Developer (3 Personen):
  Soll: AUTOSAR Adaptive (3), C++17 (3), ISO 26262 ASIL-B (3),
  ASPICE Level 2 (2)
  Ist: AUTOSAR Classic (4), C++11 (3), ISO 26262 (1), ASPICE (1)
- Junior Developer (2 Personen):
  Soll: AUTOSAR Classic (2), C (3), Unittest (2)
  Ist: C (2), AUTOSAR Classic (1), Unittest (0)
- Testingenieur (1 Person):
  Soll: CANoe (3), HIL-Testing (3), ISO 26262 Verifikation (2)
  Ist: CANoe (1), HIL (0), ISO 26262 (1)
- Teamleiter (1 Person):
  Soll: ISO 26262 ASIL-B Projektleitung (3), ASPICE Assessor (2)
  Ist: ISO 26262 (2), ASPICE (1)

Bewertungsskala: 0 = keine, 1 = Grundkenntnisse, 2 = Anwender,
3 = Fortgeschritten / zertifiziert, 4 = Experte / schulungsfähig

Rahmenbedingungen:
- Budget: 18.000 Euro für das Gesamtteam, laufendes Jahr
- Max. 4 Schulungstage/Person, keine Abwesenheit Juli-August
  (Serienanlauf Projekt Alpha)
- Externe Zertifizierungen bevorzugt (OEM-anerkannt)
- Interner Senior kann zu AUTOSAR Classic schulen (Juniors)

ROLE: HR Business Partner, Branchenkenntnisse Automotive,
Weiterbildungsmarkt technische Fachkräfte.

ACTION: Vier Schritte mit Bestätigung zwischen den Schritten.

FORMAT: Tabellen, Kosten in Euro, Tage. Geeignet für
Geschäftsführungspräsentation und Betriebsrat.

TARGET: HR Business Partner und Teamleiter,
Vorlage für Geschäftsführung und Betriebsrat.
```

---

## Ergänzende Hinweise

**Regulatorische Gaps zuerst:** In der Automobilindustrie sind ISO-26262-, ASPICE- und TISAX-Kompetenznachweise vertraglich oder normativ verpflichtend. Diese Gaps haben unabhängig vom Budget immer höchste Priorität. Die KI kennzeichnet regulatorisch verpflichtende Maßnahmen automatisch, wenn der Normbezug im Context steht.

**Internen Wissenstransfer ausschöpfen:** Bevor externe Schulungen gebucht werden, prüft die KI, welche Soll-Kompetenzen durch vorhandene interne Experten abgedeckt werden können. Interner Wissenstransfer spart Budget und stärkt die Teamkohäsion. Im Context angeben: "Wer im Team kann was auf Level 4?"

**Anbieter-Vorschläge anpassen:** Die KI nennt bekannte Anbieter (TÜV SÜD, TÜV Rheinland, VDI Wissensforum, PerForma, Vector Informatik, dSPACE Academy). Für aktuelle Preise und Termine immer die Anbieter-Websites prüfen, da sich Kursangebote und Kosten ändern.

**Betriebsrat und Mitbestimmung:** Bei Qualifizierungsplänen, die Rollenanforderungen oder Beurteilungskriterien verändern, frühzeitig den Betriebsrat einbinden. Die KI kann einen kurzen Abschnitt "Mitbestimmungsrelevanz" auf Anfrage ergänzen.

---

*© PROMETO GmbH 2026 | www.prometo.ai | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/deed.de)*
