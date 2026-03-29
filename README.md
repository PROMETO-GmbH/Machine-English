# PROMETO's AI Framework: Machine English

**Die deutschsprachige Referenz für professionelles Prompt Engineering im Business-Kontext**

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/deed.de)

> *Prompts schreiben ist eine Sprache und diese Sprache kann man lernen.*

---

## Über PROMETO

PROMETO steht für die Überzeugung, dass **KI das Rückgrat moderner Unternehmen** werden wird: nicht als Randwerkzeug, nicht als bloße Tooleinführung, sondern als tragende Säule von Entscheidung, Entwicklung und Betrieb. Wir begleiten Unternehmen auf diesem Weg und teilen dabei gerne, was funktioniert.

Dieses Repository ist Ausdruck dieser Haltung: ein offenes Framework, das Führungskräften und Fachleuten in technologiegetriebenen, regulierten Unternehmen hilft, das volle Potenzial von KI-Systemen zu erschließen, methodisch, reproduzierbar und ohne Umwege. Gerade dort, wo Normen, Standards und Vorschriften den Handlungsspielraum prägen, braucht der Einsatz von KI eine klare Methodik.

---

## Was ist Machine English?

Machine English ist die Fähigkeit, KI-Systeme präzise, effektiv und reproduzierbar anzuleiten. Die meisten Menschen nutzen KI wie eine Suchmaschine: mit kurzen, vagen Eingaben und entsprechend mittelmäßigen Ergebnissen. Machine English ist der Weg heraus.

**Zur Entstehung:** Dieses Framework ist inspiriert von Konzepten und Diskussionen, die in der weltweiten KI-Community öffentlich geführt werden, von Anthropic, OpenAI, Google DeepMind und unabhängigen Forschern. PROMETO hat diese Ansätze aufgegriffen, strukturiert, auf den deutschsprachigen Business-Kontext übertragen und um eigene Methoden erweitert. CRAFT und AIM sind das Ergebnis dieser Arbeit.

---

## Die zwei Kern-Methoden

### AIM: Der Einstieg

> Das englische Wort *to aim* bedeutet: etwas anstreben, gezielt auf ein Ziel ausrichten. Diese Methode bringt KI-Interaktionen auf den Punkt: drei Elemente, sofort anwendbar.

```
A: Actor    Wer ist die KI in diesem Szenario?
I: Input    Welche Informationen bekommt die KI?
M: Mission  Was ist das konkrete Ziel?
```

→ [Vollständige AIM-Dokumentation](10_Framework/AIM.md)

---

### CRAFT: Die Vertiefung

> Das englische Wort *to craft* bedeutet: etwas mit Sorgfalt und Können erschaffen. Diese Methode ist der nächste Schritt: kein zufälliges Ausprobieren, sondern das bewusste Bauen eines präzisen Prompts mit fünf Dimensionen.

```
C: Context      Welcher Hintergrund und welche Situation sind relevant?
R: Role         Welche Expertise soll die KI einnehmen?
A: Action       Was soll die KI konkret tun?
F: Format       Wie soll die Ausgabe aussehen?
T: Target       Für wen ist die Ausgabe bestimmt?
```

→ [Vollständige CRAFT-Dokumentation](10_Framework/CRAFT.md)

---

## Für alle, die bereits gute Prompts schreiben: Die 7 Profi-Tipps

Wer AIM und CRAFT bereits beherrscht, findet hier den nächsten Hebel. Diese sieben Zusätze lassen sich an **jeden** bestehenden Prompt anhängen: sie verändern nicht die Frage, sondern die Art, wie die KI denkt.

| # | Zusatz | Wirkung |
|---|--------|---------|
| **1** | *„Formuliere das so, dass es meine Sicht auf das Problem komplett verändert."* | Zwingt zur alternativen Rahmung, durchbricht eingefahrenes Denken |
| **2** | *„Was würde ein Top-0,1%-Experte in diesem Bereich denken und anders machen?"* | Aktiviert Tiefe statt Durchschnitt |
| **3** | *„Stelle Rückfragen, bis eine 90%ige Sicherheit besteht, die Aufgabe perfekt zu lösen."* | Verhindert generische Antworten durch gezielte Klärung |
| **4** | *„Welche Frage hätte ich stellen sollen, aber nicht gestellt?"* | Macht blinde Flecken sichtbar |
| **5** | *„Nenne die 3 häufigsten Fehler in dieser Situation und wie man sie vermeidet."* | Lernen aus Anti-Mustern, bevor sie entstehen |
| **6** | *„Spiele den Advocatus Diaboli: Warum könnte dieser Ansatz komplett falsch sein?"* | Stresstesting vor der Entscheidung |
| **7** | *„Was wäre der unkonventionellste, aber potenziell effektivste Weg? Jenseits offensichtlicher Lösungen."* | Durchbricht konventionelle Denkmuster |

→ [Ausführliche Dokumentation mit Beispielen und Varianten](20_Templates/allgemein/profi-tipps.md)

---

## Das Level-System

| Level | Bezeichnung | Beschreibung |
|-------|------------|--------------|
| **1** | Einsteiger | Allgemeine, unspezifische Anfragen ohne Kontext |
| **2** | Anwender | Kontextbezogen, mit konkreten Details und klarer Aufgabe |
| **3** | Fortgeschritten | Persona + Kontext + Referenzmaterial kombiniert |
| **4** | Experte | Systematischer Einsatz von AIM oder CRAFT |

→ [Level-System im Detail](10_Framework/level-system.md)

---

## Prompt-Bibliothek

Kuratierte Templates für Unternehmen, die eingebettete Systeme entwickeln und fertigen: von Automotive, Bahntechnik, Haushaltsgeräte, Industrieautomatisierung und Maschinenbau bis zur Zulieferindustrie. Die Bibliothek ist nach Verantwortungsbereichen gegliedert:

| Bereich | Ausrichtung |
|---------|-------------|
| [Führung & Strategie](20_Templates/fuehrung/) | Strategieentwicklung, Entscheidungsvorbereitung, Kommunikation in die Organisation |
| [IT & Sicherheit](20_Templates/it-sicherheit/) | Risikoanalysen, Sicherheitskonzepte, Dokumentation, Compliance |
| [Embedded Software](20_Templates/embedded-software/) | Anforderungsanalyse, Code-Review-Vorbereitung, Technologiebewertung, AUTOSAR/MISRA-Kontext |
| [Elektronik & Mechanik](20_Templates/elektronik-mechanik/) | Designreviews, Stücklistenanalyse, Fehlerbaumanalysen, Lieferantenbewertung |
| [Produktion](20_Templates/produktion/) | Prozessoptimierung, Qualitätssicherung, Störungsanalyse, Ramp-up-Vorbereitung |
| [HR & Personal](20_Templates/hr/) | Stellenprofile, Entwicklungsgespräche, Onboarding, Führungskommunikation |
| [Marketing & Vertrieb](20_Templates/marketing/) | Positionierung, Content, Kundenansprache, Messeauftritte |

---

## Übungen

Wer dieses Repository nutzt, hat ein klares Ziel: Level 4. Die Übungen setzen daher mit AIM und CRAFT als Werkzeug an, angewandt auf reale Szenarien aus technologiegetriebenen Unternehmen. Grundlagen werden nicht erklärt, sondern durch Anwendung erarbeitet.

- [Übungen (Level 3-4)](30_Uebungen/profi-uebungen.md) – Systematischer Einsatz von AIM und CRAFT anhand praxisnaher Aufgabenstellungen

---

## Weiterführendes Training

Dieses Repository ist die offene Wissensbasis. Für strukturiertes Lernen mit direktem Praxisbezug:

- 🎓 **[Selbstlernkurs](https://www.prometo.ai/kurse)** – 30-minütiger Einstieg, inkl. Quizzes und Übungen
- 🧑‍🏫 **[Präsenztraining & Workshops](https://www.prometo.ai/trainings)** – Vertiefung mit eigenen Use Cases und Live-Feedback
- 🏢 **[Unternehmenstraining](https://www.prometo.ai/firmentraining)** – Maßgeschneidert für Teams in der Industrie

---

## Lizenz

Dieses Framework steht unter der **[Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/deed.de)**.

Das bedeutet: freie Nutzung, Weitergabe und Anpassung, auch kommerziell, unter der Bedingung, dass PROMETO als Quelle genannt wird.

**Namensnennung:** PROMETO GmbH | www.prometo.ai

---

*© PROMETO GmbH 2026 | www.prometo.ai | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/deed.de)*
