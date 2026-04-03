# Template: Arbeitsanweisung / SOP erstellen

**Framework:** CRAFT | **Level:** 3 | **Bereich:** Produktion

---

## Kontext

Arbeitsanweisungen (AA) und Standard Operating Procedures (SOP) sind das Rückgrat der Fertigungsqualität: Sie sichern reproduzierbare Prozesse, reduzieren Einarbeitungszeiten und sind Nachweisdokument bei Audits (IATF 16949, ISO 9001, VDA 6.3). Gleichzeitig sind sie zeitaufwendig zu erstellen und veralten schnell. Dieses Template nutzt KI, um aus Prozessbeschreibungen, Zeichnungen und Erfahrungswissen strukturierte, normgerechte Arbeitsanweisungen zu erzeugen, die direkt am Shopfloor einsetzbar sind.

---

## Template (zum Ausfüllen)

```
CONTEXT: Wir erstellen eine Arbeitsanweisung für den Prozessschritt
[Prozessbezeichnung, z.B. "manuelle Endmontage des Getriebedeckels
an Baugruppe XY-4711"] in der Fertigung bei [Unternehmen/Werk/Linie].

Produktionssystem: [z.B. "Fließmontage, Taktzeit 45 s,
Schichtbetrieb 3 Schichten, Losgröße 800 Stück/Tag"]

Qualitätsanforderungen und Normbezug:
- [z.B. "IATF 16949, Kundenvorgabe: Anzugsdrehmoment dokumentiert,
  Nullfehler-Strategie für Sicherheitsteile nach PPAP-Freigabe"]
- [z.B. "Fehlerproofing (Poka-Yoke): Drehmomentwerkzeug mit
  elektronischer Quittierung, Barcode-Scan vor Ablage"]

Prozessschritte (Rohbeschreibung aus Werkeraussage oder Zeichnung):
1. [Schritt, z.B. "Bauteil aus Bereitstellungsregal entnehmen,
   Sachnummer prüfen"]
2. [Schritt]
3. [weiterer Schritt]
[beliebig viele Schritte einfügen]

Sicherheitsrelevante Aspekte:
- [z.B. "scharfe Kanten am Stanzgrat, Schnittschutzhandschuhe
  Kategorie B erforderlich"]
- [z.B. "Druckluftbetrieb 6 bar, Gehörschutz Pflicht"]
- [z.B. "keine sicherheitsrelevanten Aspekte bekannt"]

Hilfsmittel und Betriebsmittel:
- [z.B. "Drehmomentschlüssel Typ XY, kalibriert bis [Datum]"]
- [z.B. "Montageschablone Zeichnung Nr. 4711-REV3"]
- [z.B. "Prüflehre, Sichtprüfung nach Prüfplan QP-0815"]

Zielgruppe der Anweisung: [z.B. "Werker ohne Vorkenntnisse
(Anlernzeit < 4 h), Deutsch und Türkisch als Arbeitssprachen"]

ROLE: Du bist ein erfahrener Fertigungsingenieur und Qualitätsmanager
mit Kenntnissen in Lean Production, IATF 16949 und VDA 6.3.
Du weißt, welche Informationen eine Arbeitsanweisung am Shopfloor
tatsächlich braucht, damit Werker ohne Rückfragen korrekt arbeiten können.
Du achtest auf eindeutige Sprache (kurze Sätze, Aktivform, Verben
am Satzanfang), vermeidest Fachbegriffe ohne Erklärung und schlägst
Poka-Yoke-Maßnahmen vor, wo sie sinnvoll sind.

ACTION: Erstelle die Arbeitsanweisung in vier Schritten.
Präsentiere jeden Schritt einzeln und warte auf Bestätigung:

Schritt 1: Dokumentenkopf und Geltungsbereich
  - Titel, Dokumentennummer (Vorschlag), Revision, Datum, Ersteller
  - Geltungsbereich: Linie, Produkt, Sachnummer, Varianten
  - Normbezug und Verweise auf übergeordnete Dokumente
    (Zeichnung, Prüfplan, Sicherheitsdatenblatt)
  - Qualifikationsanforderung: Welche Unterweisung/Schulung
    ist Voraussetzung für diesen Arbeitsplatz?

Schritt 2: Sicherheitshinweise (vor dem Prozess)
  - Persönliche Schutzausrüstung (PSA) in Tabellenform:
    Schutzausrüstung, Norm, Begründung
  - Gefährdungen mit Ampelkennzeichnung: Grün/Gelb/Rot
  - Verhalten im Fehlerfall (Notstopp, Meldekette)

Schritt 3: Prozessschritte (Hauptteil)
  - Nummerierte Schrittliste: Schritt | Tätigkeit | Hilfsmittel |
    Qualitätskriterium / i.O.-Merkmal
  - Für jeden Schritt: Was ist zu tun? Wie ist Gut von Schlecht
    zu unterscheiden? Was passiert bei Abweichung?
  - Poka-Yoke-Hinweise: wo kann die KI sinnvolle Fehlervermeidung
    ergänzen (Scan, Lehre, Signalton, Zwangsfolge)?
  - Taktzeit-relevante Hinweise markieren (kritischer Pfad)

Schritt 4: Qualitätssicherung und Freigabe
  - Prüfmerkmale nach Prozessabschluss: Maß, Drehmoment,
    Sichtmerkmal, Funktionstest
  - Dokumentationspflicht: Was wird unterschrieben, gescannt,
    ins MES eingetragen?
  - Änderungshistorie (Tabelle: Rev. | Datum | Änderung | Freigabe)
  - Hinweis auf nächste Überprüfung (Revisionsintervall)

FORMAT: Tabellen für PSA, Prozessschritte und Prüfmerkmale.
Fließtext nur für Geltungsbereich und Sicherheitshinweise.
Sprache: kurze Sätze (max. 15 Wörter), Aktivform, Verben am Satzanfang.
Keine Abkürzungen ohne Auflösung. Ausgabe in Deutsch,
Hinweis geben falls Übersetzung in weitere Sprachen sinnvoll ist.

TARGET: Werker am Shopfloor, direkte Vorgesetzte (Schichtführer,
Meister) und Qualitätsauditoren. Das Dokument muss ohne Rückfragen
verständlich sein und Audits nach IATF 16949 / VDA 6.3 standhalten.
```

---

## Ausgefülltes Beispiel: Einbau einer Steuergeräte-Platine in ein Gehäuse

```
CONTEXT: Wir erstellen eine Arbeitsanweisung für den Prozessschritt
"Einbau und Verschraubung einer ECU-Platine (Motorsteuergerät)
in das Aluminiumgehäuse, Baureihe MCU-4x" bei
Automobilzulieferer Fischer Electronic, Werk Schweinfurt, Linie 3.

Produktionssystem: Fließmontage, Taktzeit 60 s,
2-Schicht-Betrieb, Losgröße 1.200 Stück/Tag,
PPAP-Freigabe liegt vor (Level 3).

Qualitätsanforderungen und Normbezug:
- IATF 16949, Kundenspezifikation OEM-Q-4711 (Null-Fehler
  für sicherheitsrelevante Schraubverbindungen)
- 4 Schrauben M4 x 10, Anzugsmoment 2.5 Nm +/- 0.2 Nm,
  elektronisch gesteuerter Schrauber mit OK/NOK-Quittierung
- ESD-geschützter Arbeitsplatz erforderlich (IEC 61340-5-1)
- Seriennummern-Scan vor und nach Montage (MES-Anbindung)

Prozessschritte (aus Werkerunterweisung):
1. Seriennummer Platine scannen, MES-Freigabe abwarten
2. Platine aus ESD-Tray entnehmen, Sichtprüfung auf
   Transportschäden
3. Platine in Gehäuse einlegen, Positionierung über
   zwei Führungsstifte
4. Vier Schrauben M4 handfest eindrehen (Kreuzreihenfolge)
5. Schrauber ansetzen, Anzugsmoment 2.5 Nm, Reihenfolge
   lt. Anzugsplan (1-3-2-4)
6. Schrauber-OK-Signal abwarten, NOK stoppt Linie
7. Seriennummer Gehäuse scannen, Verbindung im MES buchen
8. Baugruppe in nächsten Puffer ablegen

Sicherheitsrelevante Aspekte:
- ESD-empfindliche Baugruppe: Erdungsarmband Pflicht,
  ESD-Kittel, keine Kunstfaserbekleidung
- Scharfe Aluminiumkanten am Gehäuse: Schnittschutzhandschuhe
  Kategorie B (nur beim Handling des Rohgehäuses, nicht
  beim Einbau der Platine wegen ESD)

Hilfsmittel und Betriebsmittel:
- Elektronischer Schrauber Typ Atlas Copco QST 4 MT,
  kalibriert, Kalibriernachweis Arbeitsplatz-Aushang
- ESD-Tray für Platinenbereitstellung
- MES-Scanner Datalogic Gryphon GD4590
- Anzugsplan Zeichnung 4711-AN-REV2 (Aushang am Arbeitsplatz)

Zielgruppe: Werker mit ESD-Grundunterweisung (4 h),
Einarbeitungszeit an diesem Platz ca. 2 h.
Arbeitssprachen: Deutsch und Rumänisch.

ROLE: Erfahrener Fertigungsingenieur und Qualitätsmanager,
IATF 16949, ESD-Schutz, Lean Production.

ACTION: Vier Schritte mit Bestätigung zwischen den Schritten.

FORMAT: Tabellen für PSA, Prozessschritte, Prüfmerkmale.
Kurze Sätze, Aktivform, Verben am Satzanfang, keine ungeklärten
Abkürzungen. Ausgabe Deutsch, Hinweis für Rumänisch-Übersetzung.

TARGET: Werker, Schichtführer, IATF-Auditor.
```

---

## Ergänzende Hinweise

**Poka-Yoke aktiv einfordern:** Die KI schlägt von sich aus Fehlervermeidungsmaßnahmen vor, wenn der Prozess es zulässt (z.B. Scan-Zwang, Drehmomentrückmeldung, Schablonen). Wer explizit fragt "Welche Poka-Yoke-Maßnahmen fehlen noch?", bekommt eine priorisierte Liste mit Umsetzungsaufwand.

**Mehrsprachige Ausgabe:** Im Context die Zielsprachen benennen. Die KI kann die Arbeitsanweisung parallel auf Deutsch und in einer weiteren Sprache ausgeben oder einen Übersetzungsschritt als Folge-Prompt vorschlagen.

**Revisionsmanagement:** Die KI trägt Änderungen automatisch in die Historientabelle ein, wenn beim Folge-Prompt steht: "Aktualisiere die AA wegen [Änderungsgrund], neue Revision [Nummer]."

**ESD und Sicherheitsrelevanz:** Bei ESD-empfindlichen Baugruppen immer IEC 61340-5-1 als Normbezug im Context nennen. Bei sicherheitsrelevanten Verschraubungen (ASIL, SIL) stets den Anzugsplan und die Dokumentationspflicht explizit angeben, da die KI sonst allgemeine Empfehlungen gibt.

---

*© PROMETO GmbH 2026 | www.prometo.ai | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/deed.de)*
