# Template: Bewertung von KI-Diensten auf Cybersecurity- und Datenschutzrisiken

**Framework:** CRAFT | **Level:** 4 | **Bereich:** IT & Sicherheit

---

## Kontext

Unternehmen in der Embedded-Systems-Branche prüfen zunehmend den Einsatz cloudbasierter KI-Dienste (z.B. für Code-Analyse, Anforderungsverarbeitung oder Dokumentation). Dabei entstehen Fragen zu Datenschutz (DSGVO), Informationssicherheit (TISAX, ISO 27001) und regulatorischen Anforderungen (EU AI Act). Dieses Template unterstützt die strukturierte Bewertung vor einer Freigabeentscheidung.

---

## Template (zum Ausfüllen)

```
CONTEXT: Unser Unternehmen entwickelt [Produkt/System, z.B. "Steuergeraete
fuer Antriebssysteme"] und prueft den Einsatz des KI-Dienstes [Name des
Dienstes, z.B. "GitHub Copilot / ChatGPT Enterprise / Claude for Work"].
Wir sind zertifiziert nach [z.B. TISAX, ISO 27001] und verarbeiten
regelmaessig [Art der Daten, z.B. "proprietaeren Quellcode, technische
Spezifikationen, Kundendaten"]. Unser Rechtsrahmen umfasst DSGVO,
[ggf. branchenspezifische Anforderungen, z.B. UN R155 / UNECE WP.29].

ROLE: Du bist ein erfahrener CISO mit Spezialisierung auf Cybersecurity
und Datenschutz in regulierten Industrieunternehmen. Du kennst die
Anforderungen der DSGVO, des EU AI Acts und gaengiger
Industriestandards (TISAX, ISO 27001, IEC 62443) aus der Praxis.

ACTION: Bewerte den Einsatz des genannten KI-Dienstes anhand der
folgenden Kriterien:
1. Datenschutzrisiken (Datenverarbeitung, Speicherort, Drittlandtransfer)
2. Informationssicherheitsrisiken (Datenlecks, Modelltraining auf Eingaben)
3. Konformitaet mit DSGVO und EU AI Act (Risikokategorie des Dienstes)
4. TISAX-Relevanz (Auswirkung auf bestehende Zertifizierung)
5. Handlungsempfehlung: Freigabe, bedingte Freigabe oder Ablehnung

FORMAT: Strukturierte Bewertung mit Ampel-System (gruen/gelb/rot) pro
Kriterium, abschliessender Gesamtbewertung und maximal 5 konkreten
Massnahmen bei bedingter Freigabe. Umfang: maximal 1 DIN-A4-Seite,
geeignet fuer die Entscheidungsvorlage an die Geschaeftsfuehrung.

TARGET: Geschaeftsfuehrung und IT-Leitung eines mittelstaendischen
Zulieferers. Technisches Grundverstaendnis vorhanden, aber keine
Tiefenexpertise in Datenschutzrecht oder KI-Regulierung.
```

---

## Ausgefuelltes Beispiel: Bewertung von ChatGPT Enterprise

```
CONTEXT: Unser Unternehmen entwickelt Embedded-Software fuer
Fahrerassistenzsysteme und prueft den Einsatz von ChatGPT Enterprise
fuer die interne Dokumentation und Code-Review-Vorbereitung. Wir sind
TISAX-zertifiziert (Label 2) und verarbeiten proprietaeren C/C++-Code
sowie technische Kundenspezifikationen. Unser Rechtsrahmen umfasst
DSGVO und UN R155.

ROLE: Du bist ein erfahrener CISO mit Spezialisierung auf Cybersecurity
und Datenschutz in regulierten Industrieunternehmen. Du kennst DSGVO,
EU AI Act, TISAX und ISO 27001 aus der Praxis.

ACTION: Bewerte den Einsatz von ChatGPT Enterprise anhand der fuenf
genannten Kriterien: Datenschutzrisiken, Informationssicherheitsrisiken,
DSGVO/EU AI Act, TISAX-Relevanz, Handlungsempfehlung.

FORMAT: Ampel-Bewertung pro Kriterium, Gesamtbewertung,
maximal 5 Massnahmen bei bedingter Freigabe. Maximal 1 DIN-A4-Seite,
Entscheidungsvorlage fuer Geschaeftsfuehrung.

TARGET: Geschaeftsfuehrung und IT-Leitung, technisches
Grundverstaendnis vorhanden, keine Tiefenexpertise in KI-Regulierung.
```

---

## Typische Risikobereiche bei KI-Diensten im Industrieumfeld

| Risiko | Beispiel | Relevante Anforderung |
|--------|---------|----------------------|
| Drittlandtransfer | US-amerikanische KI-Dienste, Serverstandort ausserhalb EU | DSGVO Art. 44 ff. |
| Modelltraining auf Eingaben | Quellcode fliesst in Trainingsdaten ein | TISAX, Geheimhaltung |
| Hochrisiko-KI-System | KI unterstuetzt sicherheitsrelevante Entscheidungen | EU AI Act Art. 6 |
| Protokollierungspflichten | Fehlende Nachvollziehbarkeit von KI-Ausgaben | EU AI Act Art. 12 |
| Lieferantenabhaengigkeit | Keine Exit-Strategie bei Dienstausfall | ISO 27001 A.15 |

---

*© PROMETO GmbH 2026 | www.prometo.ai | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/deed.de)*
