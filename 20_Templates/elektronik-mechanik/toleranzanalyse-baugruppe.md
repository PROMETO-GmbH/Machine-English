# Template: Toleranzanalyse einer mechanischen Baugruppe

**Framework:** CRAFT | **Level:** 4 | **Bereich:** Elektronik & Mechanik

---

## Kontext

Toleranzanalysen gehören zu den zeitintensivsten Aufgaben in der Konstruktion: Worst-Case-Betrachtungen und RSS-Methode (Root Sum of Squares) müssen für jede relevante Maßkette durchgeführt werden, bevor Prototypen gefertigt werden. Fehler in der Analyse führen zu Montageunverträglichkeiten, Nacharbeit oder Funktionsausfällen im Feld. Dieses Template führt die KI durch eine vollständige Toleranzkettenanalyse auf Basis von Zeichnungsangaben und funktionalen Anforderungen.

---

## Template (zum Ausfüllen)

```
CONTEXT: Wir analysieren die Toleranzkette einer mechanischen Baugruppe
in [Anwendungskontext, z.B. "einem Getriebegehäuse für einen
Industrieroboter-Antriebsstrang, Serienfertigung 50.000 Stück/Jahr"].

Funktionale Anforderung: [z.B. "Axialspiel der Welle muss zwischen
0.05 mm und 0.20 mm liegen, um Lagerverschleiss und Blockierung
zu vermeiden"]

Bauteile der Maßkette (aus Zeichnung):
- Bauteil 1: [Name, Nennmaß ± Toleranz, z.B. "Gehäuse-Innenmaß:
  125.00 mm ± 0.10 mm, IT-Qualität IT8, Fertigungsverfahren: Fräsen"]
- Bauteil 2: [Name, Nennmaß ± Toleranz, z.B. "Welle: 124.80 mm ± 0.05 mm,
  IT7, Schleifen"]
- Bauteil 3: [Name, Nennmaß ± Toleranz, z.B. "Distanzscheibe: 0.10 mm
  ± 0.03 mm, gestanzt"]
- [weitere Bauteile ergänzen]

Fertigungsverfahren und Prozessfähigkeit:
- [Bauteil]: Cpk = [Wert, z.B. 1.33], sigma-Niveau [z.B. 4-sigma]
- [falls keine Cpk-Werte vorliegen: "Annahme Normalverteilung, 3-sigma"]

Temperaturbereich: [z.B. "-20°C bis +85°C Betrieb,
Werkstoffe: Stahl (11.7 ppm/K) und Aluminium (23.1 ppm/K)"]

ROLE: Du bist ein erfahrener Konstrukteur und Fertigungstechniker
mit Schwerpunkt auf Toleranzmanagement und statistischen Analysemethoden.
Du kennst ISO 286 (Passungen), ISO 8015 (Toleranzprinzipien),
GD&T-Grundlagen und die Unterschiede zwischen Worst-Case und RSS-Methode.
Du bewertest, welche Methode für das jeweilige Risikoprofil und die
Seriengröße geeignet ist, und gibst direkte Handlungsempfehlungen.

ACTION: Führe eine vollständige Toleranzanalyse in vier Schritten durch.
Präsentiere jeden Schritt einzeln und warte auf Bestätigung:

Schritt 1: Maßkette aufstellen
  - Stelle die Maßkette grafisch als Gleichung auf
    (Schließmaß = Summe der Teilmaße mit Vorzeichen)
  - Identifiziere alle Einflussgrößen (geschlossene Maße, offene Maße)
  - Benenne Vorzeichen (+/-) für jede Komponente
  - Prüfe auf fehlende oder redundante Glieder

Schritt 2: Worst-Case-Analyse (WC)
  - Berechne obere und untere Grenze des Schließmaßes
    (alle ungünstigsten Toleranzen addiert)
  - Vergleiche mit funktionaler Anforderung
  - Bewerte: erfüllt / nicht erfüllt / grenzwertig (< 10% Reserve)

Schritt 3: Statistische Analyse (RSS)
  - Berechne das Schließmaß nach RSS-Methode
    (Quadratische Addition der Standardabweichungen)
  - Gib Ausschussrate in ppm an (Annahme: Normalverteilung, 3-sigma)
  - Falls Cpk-Werte vorhanden: berechne prozessfähigkeitsbasierte RSS
  - Vergleiche WC und RSS: Empfehle begründet, welche Methode
    für diesen Fall massgeblich sein soll (Sicherheitsrelevanz,
    Seriengröße, Rückrufkosten)

Schritt 4: Optimierungsempfehlung
  - Identifiziere das dominante Toleranzglied (größter Beitrag
    zur Gesamtstreuung)
  - Schlage mindestens zwei Maßnahmen vor:
    a) Engere Toleranz am dominanten Glied: neues Maß, neue IT-Qualität,
       erwartete Auswirkung auf Schließmaß und Fertigungskosten
    b) Konstruktive Maßnahme: z.B. Einstellelement, Ausgleichsscheibe,
       selektive Montage - mit Aufwandsabschätzung
  - Thermische Ausdehnung: Berechne delta-L für Temperaturbereich
    und bewerte Einfluss auf Schließmaß

FORMAT: Pro Schritt: Gleichung oder Formel (kompakte Ingenieurnotation,
keine LaTeX), Zahlenergebnis, kurze Interpretation.
Abschliessend: Zusammenfassung auf einer halben Seite als
Entscheidungsvorlage für das Design-Review.

TARGET: Konstrukteure mit 2-5 Jahren Erfahrung in CAD und
Fertigungstechnik, vertraut mit ISO-Passungen, aber ohne
Spezialisierung auf statistische Toleranzanalyse.
```

---

## Ausgefülltes Beispiel: Lagerpassung in einem Antriebsgehäuse

```
CONTEXT: Wir analysieren die Toleranzkette einer Lageraufnahme
in einem Aluminiumgehäuse für einen bürstenlosen DC-Motor
(Haushaltsgeräte, Serienfertigung 200.000 Stück/Jahr).

Funktionale Anforderung: Radialluft im Lager zwischen 0 µm und 15 µm
(Presspassung ausgeschlossen, Spielpassung mit definiertem Maximalspiel).

Bauteile der Maßkette:
- Gehäuse-Bohrung: Ø 47.000 mm + 0.025 / 0.000 mm
  (ISO H7, Druckguss + Reiben, Cpk = 1.20)
- Lager-Außenring: Ø 47.000 mm - 0.011 / - 0.025 mm
  (ISO j6, Lieferant-Standard, Cpk = 1.67)

Temperaturbereich: 0°C bis +70°C
Werkstoffe: Aluminium-Druckguss (23.1 ppm/K),
Wälzlagerstahl (11.7 ppm/K)

ROLE: Erfahrener Konstrukteur, Toleranzmanagement und statistische
Analysemethoden, ISO 286, GD&T, WC- und RSS-Methode.

ACTION: Vier Schritte mit Bestätigung zwischen den Schritten.

FORMAT: Formel + Zahlenergebnis + Interpretation pro Schritt,
Zusammenfassung als Design-Review-Vorlage.

TARGET: Konstrukteur mit CAD-Erfahrung, ohne Spezialisierung
auf statistische Toleranzanalyse.
```

---

## Ergänzende Hinweise

**Methoden-Wahl WC vs. RSS:** Worst-Case ist zwingend bei sicherheitsrelevanten Baugruppen (ASIL, SIL), Kleinserien (< 1.000 Stück) und Montageumgebungen ohne Sortierung. RSS eignet sich für Großserien mit bekannten Prozessfähigkeiten, wenn ein definiertes Ausschussrisiko akzeptabel ist. Bei der RSS-Methode immer angeben, welche Ausschussrate und welches sigma-Niveau angenommen wurden.

**Thermische Ausdehnung nicht vergessen:** Bei Mischbaugruppen aus Stahl und Aluminium kann delta-L über den Betriebstemperaturbereich die Toleranzkette um denselben Betrag wie eine IT-Qualitätsstufe verändern. Besonders kritisch bei engen Passungen und grossen Temperaturdifferenzen (> 50 K).

**Eingabevorbereitung:** Je vollständiger die Bauteilinformationen (Nennmaß, Toleranz, Fertigungsverfahren, Cpk-Wert, Werkstoff), desto präziser die Analyse. Wenn Cpk-Werte fehlen, verwendet die KI standardmässig 3-sigma für Normalverteilung.

---

*© PROMETO GmbH 2026 | www.prometo.ai | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/deed.de)*
