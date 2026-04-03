# Profi-Übungen (Level 3–4)

Diese Übungen trainieren den systematischen Einsatz von CRAFT und AIM anhand praxisnaher Szenarien aus technologiegetriebenen Unternehmen. Die Aufgaben sind nach Unternehmensrolle gegliedert: Schlag direkt im für dich relevanten Abschnitt auf. Eigene Branche, eigenes Unternehmen und eigene Details sind ausdrücklich erwünscht: Die Vorlagen sind Ausgangspunkte, keine Pflichtaufgaben.

**Zeitbedarf gesamt:** ca. 60–90 Minuten (alle Bereiche) oder 20–30 Minuten (ein Bereich)

**Werkzeug:** Teile deinen Bildschirm: GitHub links, dein KI-Tool rechts (ChatGPT, Claude, Microsoft Copilot, Gemini oder ein anderes). Schreibe deinen Prompt im KI-Tool, kopiere ihn per Copy-Paste in den Feedback-Prompt unten und schicke ihn zur Bewertung zurück an die KI.

---

## Feedback-Prompts zum Kopieren

Nachdem du einen Prompt geschrieben und das KI-Ergebnis erhalten hast: Kopiere den passenden Feedback-Prompt, ersetze die Platzhalter und schicke ihn an dein KI-Tool. Du bekommst eine strukturierte Bewertung mit konkretem Verbesserungsvorschlag.

**Feedback-Prompt für CRAFT-Übungen:**

```
Bewerte den folgenden CRAFT-Prompt nach diesen 5 Kriterien (je 1–5 Punkte):

1. Context (C): Ist der Hintergrund ausreichend und präzise beschrieben?
2. Role (R): Ist die KI-Persona sinnvoll gewählt und mit konkreten Eigenschaften versehen?
3. Action (A): Ist die Aufgabe klar, spezifisch und umsetzbar formuliert?
4. Format (F): Ist die gewünschte Ausgabestruktur eindeutig definiert?
5. Target (T): Ist die Zielgruppe klar beschrieben?

Mein CRAFT-Prompt:
[HIER DEINEN PROMPT EINFÜGEN]

KI-Ergebnis:
[HIER DAS KI-ERGEBNIS EINFÜGEN]

Gib für jedes Kriterium eine kurze Begründung und einen Score (1–5).
Nenne das stärkste und das schwächste Element.
Schließe mit einem einzigen, konkreten Verbesserungsvorschlag ab.
```

**Feedback-Prompt für AIM-Übungen:**

```
Bewerte den folgenden AIM-Prompt nach diesen 4 Kriterien (je 1–5 Punkte):

1. Actor: Ist die Persona klar, realistisch und mit konkreten Eigenschaften beschrieben?
2. Input: Sind alle relevanten Rahmendaten vollständig und übersichtlich angegeben?
3. Mission: Ist das Ziel konkret, handlungsleitend und eindeutig formuliert?
4. Praxisbezug: Lässt sich der Prompt direkt im Berufsalltag einsetzen?

Mein AIM-Prompt:
[HIER DEINEN PROMPT EINFÜGEN]

KI-Ergebnis:
[HIER DAS KI-ERGEBNIS EINFÜGEN]

Gib für jedes Kriterium eine kurze Begründung und einen Score (1–5).
Schließe mit einem einzigen, konkreten Verbesserungsvorschlag ab.
```

---

## Für Führungskräfte und Management

### Übung F-1: Entscheidungsvorlage mit CRAFT (20 Min.)

**Hintergrund:** Führungskräfte erhalten mit KI oft generische Texte, die nicht zur eigenen Situation passen. CRAFT verhindert das, indem die Entscheidungsgrundlage präzise beschrieben wird.

**Aufgabe:** Erstelle einen vollständigen CRAFT-Prompt für eine Entscheidungsvorlage aus deinem Führungsalltag.

Wähle eines dieser Szenarien oder ersetze es durch ein eigenes:

- **Option A:** Du willst entscheiden, ob euer Unternehmen einen KI-Dienst (z.B. Microsoft Copilot) einführt. Die Entscheidungsvorlage geht an die Geschäftsführung.
- **Option B:** Du willst eine Make-or-Buy-Entscheidung für eine Softwarekomponente vorbereiten.
- **Option C:** Du willst die Kurzarbeit-Option für ein Quartal bewerten lassen, bevor du sie dem Betriebsrat vorschlägst.

Dein CRAFT-Prompt:
```
CONTEXT:

ROLE:

ACTION:

FORMAT:

TARGET:
```

**Gütekriterium:** Enthält dein Prompt alle Rahmendaten, die ein externer Berater bräuchte, um dieselbe Vorlage zu erstellen?

---

### Übung F-2: Kommunikation in die Organisation mit AIM (15 Min.)

**Hintergrund:** AIM eignet sich besonders gut für Szenarien, in denen die KI eine bestimmte Stimme oder Perspektive einnehmen soll: Townhall-Ansprache, Schichtleiterkommunikation, E-Mail ans Team.

**Aufgabe:** Schreibe einen AIM-Prompt für eine Kommunikationsaufgabe in die Organisation.

Mögliche Szenarien:

- Ankündigung einer Reorganisation gegenüber dem Team
- Monatliche Führungskräfte-E-Mail über Produktionsergebnisse
- Kurze Townhall-Ansprache zum Thema KI-Einführung im Unternehmen

```
ACTOR:

INPUT:

MISSION:
```

**Reflexion:** Hat die KI den richtigen Ton getroffen? Was hättest du anders formuliert, und warum hat die KI es anders gemacht?

---

## Für Entwickler und Techniker (Embedded, Elektronik, Mechanik)

### Übung T-1: Technische Analyse Schritt für Schritt mit CRAFT (20 Min.)

**Hintergrund:** Technische Analysen scheitern mit KI oft daran, dass der Context zu dünn ist: kein Bauteil, keine Norm, kein Ziel. CRAFT erzwingt Vollständigkeit.

**Aufgabe:** Erstelle einen CRAFT-Prompt für eine technische Analyse aus deiner täglichen Arbeit.

Mögliche Szenarien:

- **Embedded:** Bewertung zweier Mikrocontroller-Plattformen für ein neues Projekt (Kosten, AUTOSAR-Eignung, Verfügbarkeit)
- **Elektronik:** Auswahl einer Stromversorgungsarchitektur (Buck vs. LDO) für eine Sensorplatine
- **Mechanik:** Bewertung zweier Fügeverbindungen (Kleben vs. Schweißen) für eine Gehäusebaugruppe hinsichtlich Crash-Anforderungen

```
CONTEXT:

ROLE:

ACTION:

FORMAT:

TARGET:
```

**Gütekriterium:** Würde ein Kollege aus einer anderen Fachabteilung mit deinem Prompt dieselbe Analyse erhalten?

---

### Übung T-2: Schwacher Prompt verbessern (10 Min.)

**Aufgabe:** Identifiziere die Probleme im folgenden Prompt und schreibe eine CRAFT-Version.

**Schwacher Prompt:**
```
Erkläre mir AUTOSAR. Was ist der Unterschied zwischen Classic und Adaptive?
Soll für unsere Entwickler sein. Bitte nicht zu kompliziert, aber vollständig.
```

1. Welche drei Elemente fehlen vollständig?
2. Was ist am Action-Teil unklar?
3. Schreibe eine CRAFT-Version für Embedded-Software-Entwickler, die von Classic auf Adaptive umsteigen sollen (erfinde sinnvolle Details).

---

## Für Produktion und Qualitätsmanagement

### Übung P-1: Ursachenanalyse mit AIM (15 Min.)

**Hintergrund:** AIM eignet sich für Simulationen und Rollenspiele. In der Produktion heißt das: die KI als Moderator einer Ursachenanalyse, als Ishikawa-Experte oder als 5-Why-Gesprächspartner einsetzen.

**Aufgabe:** Schreibe einen AIM-Prompt für eine Ursachenanalyse einer Produktionsstörung.

Mögliche Szenarien:

- Erhöhter Ausschuss an der Lötstelle einer Platinenbaugruppe (plötzlich, nach Rüstwechsel)
- Wiederkehrendes Drehmoment-NOK an einer Schraubstation (ca. 3% Ausschussrate)
- Fehlerhafter Barcode-Scan am Bandende (MES-Anbindung, Linie steht)

```
ACTOR:

INPUT:

MISSION:
```

**Zusatz:** Ergänze deinen Prompt um einen der 7 Profi-Tipps. Welcher passt hier am besten und warum?

---

### Übung P-2: Arbeitsanweisung optimieren mit CRAFT (15 Min.)

**Aufgabe:** Nimm eine bestehende Arbeitsanweisung aus deinem Betrieb (oder beschreibe einen Prozessschritt aus dem Gedächtnis) und erstelle einen CRAFT-Prompt, der die KI anweist, daraus eine verbesserte, shopfloor-taugliche Version zu erstellen.

Fokus: kurze Sätze, Aktivform, Poka-Yoke-Hinweise, eindeutige Qualitätskriterien.

```
CONTEXT:

ROLE:

ACTION:

FORMAT:

TARGET:
```

**Gütekriterium:** Würde ein Werker ohne Rückfragen nach dieser Anweisung arbeiten können?

---

## Für HR und Personal

### Übung H-1: Anforderungsprofil mit CRAFT (15 Min.)

**Hintergrund:** Stellenanzeigen für technische Fachkräfte sind oft entweder zu generisch (kein Kontext) oder zu technisch (Kandidaten schrecken ab). CRAFT hilft, den richtigen Ton zu treffen.

**Aufgabe:** Erstelle einen CRAFT-Prompt für ein Anforderungsprofil oder eine Stellenanzeige.

Mögliche Szenarien:

- Senior Embedded Software Engineer (AUTOSAR, ISO 26262)
- Schichtführer in der Elektronikmontage
- HR Business Partner für einen Produktionsstandort mit 600 Mitarbeitenden

```
CONTEXT:

ROLE:

ACTION:

FORMAT:

TARGET:
```

**Gütekriterium:** Könnte die Anzeige so direkt auf LinkedIn veröffentlicht werden, ohne dass HR-Kollegen noch etwas nachbessern müssen?

---

### Übung H-2: Skill-Gap-Gespräch simulieren mit AIM (10 Min.)

**Hintergrund:** Entwicklungsgespräche sind schwierig vorzubereiten, besonders wenn der Mitarbeitende defensiv reagiert oder klare Kompetenzmängel thematisiert werden müssen. AIM ermöglicht eine realistische Simulation.

**Aufgabe:** Schreibe einen AIM-Prompt, der ein Entwicklungsgespräch simuliert.

Mögliche Szenarien:

- Mitarbeitender hat Potenzial, lehnt aber Weiterbildung ab
- Fachexperte soll in Zukunft Teamleitungsverantwortung übernehmen
- Leistungsträger aus dem Ausland, Sprachbarriere bei Dokumentation

```
ACTOR:

INPUT:

MISSION:
```

**Reflexion:** Wie realistisch hat die KI reagiert? Welche Argumente des "Mitarbeitenden" hätte ein echter Mensch vermutlich anders eingebracht?

---

## Bereichsübergreifend: Die 7 Profi-Tipps einsetzen (10 Min.)

**Aufgabe:** Nimm einen Prompt, den du in einer der obigen Übungen geschrieben hast, und ergänze ihn um zwei verschiedene Profi-Tipps. Vergleiche die drei Ergebnisse:

| Version | Profi-Tipp | Ergebnis (kurze Notiz) | Qualität 1–5 |
|---------|-----------|----------------------|-------------|
| Original | (keiner) | | |
| Version A | Tipp Nr. __ | | |
| Version B | Tipp Nr. __ | | |

**Leitfragen:**
- Welcher Tipp hat den größten Unterschied erzeugt?
- Bei welchem Prompt-Typ wirkt welcher Tipp am stärksten?

→ [Alle 7 Profi-Tipps mit Erklärungen und Varianten](../20_Templates/allgemein/profi-tipps.md)

---

## Selbstcheck: Bin ich auf Level 4?

| Kriterium | ✅ | ⚠️ | ❌ |
|-----------|---|---|---|
| Ich nutze CRAFT oder AIM systematisch, nicht nur intuitiv | | | |
| Ich definiere immer eine Zielgruppe (Target) oder einen Actor | | | |
| Ich lege Format und Länge in jedem wichtigen Prompt fest | | | |
| Ich gebe der KI explizit Domänenkenntnisse über die Role | | | |
| Ich iteriere Prompts (v1 → v2) statt einmalig zu senden | | | |
| Ich nutze mindestens einen Profi-Tipp pro Woche gezielt | | | |

4–5 ✅: Du arbeitest auf Level 4. Bleib dabei und hilf anderen im Team.
6 ✅: Du bist bereit für die PROMETO-Zertifizierung.

---

## Du willst mehr?

Die Übungen hier sind der Einstieg. Im PROMETO-Training gehst du mit eigenen Use Cases aus deinem Unternehmen in die Tiefe: Live-Feedback auf deine Prompts, Peer-Austausch mit Teilnehmenden aus derselben Branche und eine Zertifizierung, die dein Niveau dokumentiert.

- 🎓 **[Selbstlernkurs](https://www.prometo.ai/kurse)** – 30 Minuten, interaktiv, mit Quizzes und Übungen direkt im Browser
- 🧑‍🏫 **[Präsenztraining & Workshops](https://www.prometo.ai/trainings)** – eigene Use Cases, Live-Feedback, Zertifizierung
- 🏢 **[Unternehmenstraining](https://www.prometo.ai/firmentraining)** – maßgeschneidert für Teams, mit branchenspezifischen Szenarien aus Automotive, Industrieautomatisierung und Maschinenbau

---

*© PROMETO GmbH 2026 | www.prometo.ai | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/deed.de)*
