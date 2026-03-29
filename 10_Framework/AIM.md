# AIM Framework – Vollständige Dokumentation

**AIM** ist ein kompaktes Framework für präzises Prompt Engineering, wenn Geschwindigkeit und Fokus gefragt sind. Es eignet sich besonders für klar abgegrenzte Aufgaben.

---

## Die drei Elemente

### A – Actor (Akteur)
*Wer ist die KI in diesem Szenario?*

Der Actor definiert die Identität und Perspektive der KI. Im Unterschied zur CRAFT-Rolle ist der Actor enger gefasst und oft stärker an ein konkretes Szenario gebunden.

**Schlecht:**
```
Spiele einen Berater.
```

**Gut:**
```
ACTOR: Du bist ein erfahrener Einkaufsleiter eines deutschen
Automobilzulieferers mit 20 Jahren Verhandlungserfahrung. Du
vertrittst die Interessen eines Unternehmens mit hohem Kostendruck
und langen Lieferketten.
```

**Wann ist ein guter Actor entscheidend?**
- Rollenspiele (Verhandlungen, Interviews, Kundengespräche)
- Simulationen (Was würde X sagen/denken?)
- Perspektivwechsel (Wie sieht das ein Kritiker/Investor/Kunde?)

---

### I – Input (Eingabe)
*Welche Informationen bekommt die KI?*

Der Input beschreibt alle relevanten Daten, Dokumente oder Ausgangsinformationen, die die KI für die Aufgabe benötigt. Das können sein:
- Texte, Dokumente, Daten
- Spezifische Rahmenbedingungen
- Einschränkungen und Anforderungen
- Referenzmaterialien

**Schlecht:**
```
Hier sind einige Informationen über unser Produkt.
```

**Gut:**
```
INPUT:
- Unternehmen: SaaS-Anbieter für Qualitätsmanagement (QM)
- Produkt: Cloud-basierte QM-Software für produzierende Betriebe
- Zielkunde: Produktionsleiter, 50–500 MA, DACH
- Alleinstellungsmerkmal: Integration in bestehende ERP-Systeme ohne IT-Projekt
- Preisrahmen: 299–899 € / Monat (je nach Unternehmensgröße)
- Verfügbare Unterlagen: [Produktbeschreibung einfügen]
- Budget für Maßnahme: 5.000 €
- Zeitrahmen: Ergebnis wird am 15. April präsentiert
```

**Tipp:** Je mehr relevante Informationen im Input, desto weniger muss die KI erraten oder allgemein antworten.

---

### M – Mission (Auftrag)
*Was ist das konkrete Ziel?*

Die Mission ist der Kernauftrag – was die KI am Ende produzieren oder erreichen soll. Sie unterscheidet sich von der Action in CRAFT dadurch, dass sie stärker auf das **Ergebnis** fokussiert, nicht auf den Prozess.

**Schlecht:**
```
Hilf mir bei der Vorbereitung.
```

**Gut:**
```
MISSION: Erstelle ein 5-seitiges Verkaufsskript für ein Erstgespräch
mit einem Produktionsleiter. Das Skript soll:
- Mit einer offenen Qualifikationsfrage beginnen
- Die Top-3-Einwände (Kosten, Integrationsaufwand, Datensicherheit)
  mit überzeugenden Antworten behandeln
- Mit einem konkreten nächsten Schritt (Demo-Termin) enden
- In einem professionellen, aber nicht steif-formalen Ton geschrieben sein
```

---

## CRAFT vs. AIM – Wann welches Framework?

| Kriterium | CRAFT | AIM |
|-----------|-------|-----|
| Aufgaben-Komplexität | Hoch | Mittel |
| Benötigte Zeit zum Formulieren | 5–10 Min. | 2–5 Min. |
| Am besten für | Strategiepapiere, Kampagnen, komplexe Analysen | Rollenspiele, Simulationen, fokussierte Outputs |
| Stärke | Maximale Präzision durch 5 Dimensionen | Schnelle Fokussierung auf Kern-Szenario |
| Schwäche | Kann bei einfachen Aufgaben überdimensioniert sein | Weniger Kontrolle über Format und Stil |

**Empfehlung:** Starte mit AIM für schnelle Aufgaben. Nutze CRAFT, wenn das Ergebnis präsentiert werden soll oder hohe Qualitätsanforderungen bestehen.

---

## Vollständiges AIM-Beispiel 1: Verhandlungsvorbereitung

```
ACTOR: Du bist ein erfahrener Einkaufsleiter eines deutschen
Automobilzulieferers. Deine Prioritäten sind: Kostensenkung um
mindestens 8%, Liefersicherheit und langfristige Partnerschaft.
Du bist direkt, sachlich und lässt dich nicht durch Emotionen
beeinflussen.

INPUT:
- Zulieferer: Chinesischer Anbieter für Elektronikkomponenten
- Aktuelle Konditionen: 45 € / Einheit, Lieferzeit 6 Wochen, MOQ 500
- Unser Ziel: 41 € / Einheit, Lieferzeit 4 Wochen, MOQ 300
- Druckmittel: Wir haben zwei alternative Angebote zu 42 € / Einheit
- Beziehungshistorie: 2 Jahre, bisher keine größeren Probleme

MISSION: Führe ein realistisches Verhandlungsgespräch mit mir.
Ich spiele den Vertreter des Zulieferers. Starte mit einer kurzen
Eröffnung und reagiere authentisch auf meine Argumente. Weise darauf
hin, wenn meine Verhandlungsführung Schwächen hat.
```

---

## Vollständiges AIM-Beispiel 2: Technologieentscheidung vorbereiten

```
ACTOR: Du bist ein erfahrener Software-Architekt mit tiefem Wissen
in AUTOSAR Classic und AUTOSAR Adaptive. Du kennst die Abwaegungen
zwischen beiden Architekturen aus realen Fahrzeugprojekten und
sprichst die Sprache von Entwicklungsleitern und Chief Engineers.

INPUT:
- Unternehmen: Tier-1-Zulieferer fuer Antriebssysteme
- Produkt: Neues Steuergeraet fuer elektrische Achsantriebe (eAxle)
- Rahmenbedingungen: Serienstart 2027, ISO 26262 ASIL-C, OEM-Vorgabe
  zu Over-the-Air-Updates ab 2026
- Aktueller Stand: Entwicklungsteam hat Erfahrung mit AUTOSAR Classic,
  kein produktives Adaptive-Projekt bisher abgeschlossen
- Offene Frage: Entscheidung zwischen AUTOSAR Classic und Adaptive
  muss in 4 Wochen dem OEM praesentiert werden

MISSION: Erstelle eine strukturierte Entscheidungsvorlage mit den
zentralen Abwaegungskriterien, einer klaren Empfehlung und den
drei staerksten Gegenargumenten zur empfohlenen Option. Umfang:
maximal eine DIN-A4-Seite, geeignet fuer die Vorstandsebene.
```

---

## AIM-Checkliste

Bevor du deinen Prompt absendest, prüfe:

- [ ] **A:** Ist die KI-Persona spezifisch genug (Rolle, Erfahrung, Haltung)?
- [ ] **I:** Habe ich alle relevanten Informationen und Rahmenbedingungen angegeben?
- [ ] **M:** Ist der Auftrag klar, messbar und ergebnisorientiert formuliert?

---

*© PROMETO GmbH 2026 | www.prometo.ai | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/deed.de)*
