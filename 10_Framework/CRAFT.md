# CRAFT Framework – Vollständige Dokumentation

**CRAFT** ist ein strukturiertes Framework für professionelles Prompt Engineering. Es stellt sicher, dass KI-Systeme den nötigen Kontext erhalten, um präzise und nützliche Antworten zu liefern.

---

## Die fünf Elemente

### C – Context (Kontext)
*Welcher Hintergrund ist für die Aufgabe relevant?*

Der Kontext gibt der KI das nötige Umfeld, um die Aufgabe einzuordnen. Dazu gehören:
- Branche und Unternehmensgröße
- Ausgangssituation und Problem
- Relevante Einschränkungen oder Besonderheiten
- Vorhandene Informationen

**Schlecht:** (kein Kontext)
```
Erstelle eine Marketingkampagne.
```

**Gut:**
```
CONTEXT: Wir sind ein mittelständisches Unternehmen (120 MA) aus dem
Maschinenbau-Sektor. Wir haben im letzten Jahr eine neue Predictive-
Maintenance-Software entwickelt und möchten sie auf dem deutschen Markt
einführen. Budget: 30.000 € für die erste Kampagne. Unsere Zielkunden
sind Produktionsleiter in Industrieunternehmen mit 50–500 Mitarbeitenden.
```

---

### R – Role (Rolle)
*Welche Expertise und Perspektive soll die KI einnehmen?*

Die Rollenzuweisung aktiviert domänenspezifisches Wissen und sorgt für einen passenden Ton und Ansatz. Eine gute Rolle enthält:
- Berufsbezeichnung / Expertise
- Erfahrungslevel
- Spezifisches Fachwissen
- Haltung / Verhalten

**Schlecht:**
```
Sei ein Marketingexperte.
```

**Gut:**
```
ROLE: Du bist ein erfahrener B2B-Marketingberater mit 15 Jahren Fokus
auf den deutschen Industrie- und Maschinenbausektor. Du kennst die
langen Entscheidungszyklen und die Bedeutung von Fachmessen und
direktem Vertrieb in dieser Branche. Du arbeitest faktenbasiert und
vermeidest Marketing-Buzzwords.
```

---

### A – Action (Aufgabe/Aktion)
*Was soll die KI konkret tun?*

Die Aufgabe ist das Herzstück des Prompts. Sie sollte:
- Klar und handlungsorientiert formuliert sein
- Den Umfang definieren
- Spezifische Anforderungen benennen
- Wenn nötig: Schritt-für-Schritt-Anweisungen enthalten

**Schlecht:**
```
Hilf mir mit dem Marketing.
```

**Gut:**
```
ACTION: Entwickle eine 3-Monats-Marketingstrategie zur Einführung unserer
Predictive-Maintenance-Software auf dem deutschen Markt. Die Strategie soll
folgende Elemente enthalten:
1. Positionierungsstatement (max. 50 Wörter)
2. Drei Kernbotschaften für die Zielgruppe
3. Maßnahmenplan mit Zeitachse (Monat 1–3)
4. Empfohlene Kanäle mit Begründung
5. Erfolgs-KPIs
```

---

### F – Format (Format)
*Wie soll die Ausgabe strukturiert sein?*

Das Format gibt vor, in welcher Form die KI antworten soll:
- Struktur: Tabelle, Liste, Fließtext, Markdown, JSON
- Länge: Wörteranzahl, Anzahl Bullet Points, Anzahl Seiten
- Stil: Formal, informell, präsentationsfertig
- Sprache: Deutsch, Englisch, Du/Sie

**Schlecht:**
```
(kein Formathinweis)
```

**Gut:**
```
FORMAT: Strukturiere die Ausgabe als präsentationsfertiges Strategiepapier
mit nummerierten Abschnitten. Maximale Länge: 800 Wörter. Verwende
Zwischenüberschriften und eine tabellarische Maßnahmenübersicht. Schreibe
in professionellem Deutsch, Sie-Form.
```

---

### T – Target Audience (Zielgruppe)
*Für wen ist die Ausgabe bestimmt?*

Die Zielgruppe beeinflusst Sprache, Komplexität und Fokus der Antwort:
- Wer liest die Ausgabe?
- Welchen Wissensstand haben sie?
- Was ist ihre primäre Motivation/Frage?

**Schlecht:**
```
(keine Zielgruppenangabe)
```

**Gut:**
```
TARGET: Die Strategie ist für unseren Geschäftsführer und den Vertriebsleiter
bestimmt. Beide haben technisches Grundverständnis, aber keinen Marketing-
Hintergrund. Sie interessieren sich primär für ROI und konkrete Maßnahmen,
nicht für Marketingtheorie.
```

---

## Vollständiges CRAFT-Beispiel

**Aufgabe:** Entscheidungsvorlage für ein KI-Pilotprojekt in der Fertigung

```
CONTEXT: Wir sind ein Hersteller von Industriepumpen (280 MA, Standort NRW).
Seit 6 Monaten erfassen wir Vibrations- und Temperaturdaten an 12 kritischen
Pumpenaggregaten. Drei ungeplante Ausfälle im vergangenen Quartal haben
Gesamtkosten von ca. 85.000 € verursacht. Die Geschäftsführung hat
grundsätzliches Interesse an KI-gestützter Früherkennung signalisiert,
möchte aber eine fundierte Entscheidungsgrundlage vor einer Investition.

ROLE: Du bist ein erfahrener Berater für Digitalisierung und Predictive
Maintenance im Maschinenbau. Du kennst die typischen Vorbehalte von
Produktionsleitern und weißt, wie man technische Konzepte
entscheidungsreif aufbereitet. Du arbeitest sachlich, ohne Hype,
mit klarem Fokus auf Risiken, Nutzen und Umsetzbarkeit.

ACTION: Erstelle eine einseitige Entscheidungsvorlage für die
Geschäftsführung. Die Vorlage soll enthalten:
1. Ausgangssituation (2–3 Sätze)
2. Vorgeschlagener Lösungsansatz (ML-basierte Anomalieerkennung)
3. Erwarteter Nutzen (quantifiziert, wo möglich)
4. Wesentliche Risiken und Gegenmaßnahmen
5. Empfohlene nächste Schritte (Pilot, Zeitrahmen, Budgetrahmen)

FORMAT: Strukturiertes Dokument mit nummerierten Abschnitten,
max. 400 Wörter, eine tabellarische Risiko-/Nutzen-Übersicht,
professionelles Deutsch, Sie-Form.

TARGET: Zwei Geschäftsführer — kaufmännisch und technisch. Der
kaufmännische GF denkt in Kosten und Amortisation, der technische
GF fragt nach Datensicherheit und Integrationsaufwand. Beide haben
wenig Zeit und erwarten eine klare Empfehlung, keine Abhandlung.
```

---

## CRAFT-Checkliste

Bevor du deinen Prompt absendest, prüfe:

- [ ] **C (Context):** Habe ich den relevanten Hintergrund beschrieben?
- [ ] **R (Role):** Habe ich der KI eine klare, spezifische Rolle gegeben?
- [ ] **A (Action):** Ist die Aufgabe konkret und handlungsorientiert formuliert?
- [ ] **F (Format):** Habe ich Format, Länge und Stil angegeben?
- [ ] **T (Target):** Weiß die KI, für wen die Ausgabe bestimmt ist?

---

*© PROMETO GmbH 2026 | www.prometo.ai | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/deed.de)*
