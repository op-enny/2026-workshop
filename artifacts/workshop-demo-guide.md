# AI Workshop — Build Session

Datum: 2026-05-23
Ort: SAALBAU Bornheim, Frankfurt am Main

## Block 1: Opening Demo

Dateien:
- demo-kontoauszug.csv
- demo_data/ (Rechnungs-PDFs als Quelle fur die Liste)

Ziel:
- aus den Rechnungs-PDFs erst eine Rechnungsliste ableiten
- Zahlungen matchen
- fehlende Zahlungen erkennen
- unscharfe Treffer und Anomalien markieren

Schritte mit Claude:
1. Ordner demo_data mit den Rechnungs-PDFs oeffnen.
2. Claude anweisen, alle PDFs im Ordner zu lesen und daraus eine CSV mit Rechnungsnummer, Kunde, Datum, Betrag, Falligkeitsdatum und Zahlungsstatus zu erstellen.
3. Diese CSV danach fuer den Abgleich mit dem Kontoauszug verwenden.

Prompt DE:
Ich habe meine Rechnungen bereits erstellt. Sie liegen als PDF-Dateien im Ordner demo_data.
Lies alle PDFs in diesem Ordner und erstelle daraus eine CSV-Datei mit Rechnungsnummer, Kunde, Datum, Betrag, Falligkeitsdatum und Zahlungsstatus.
Gleiche danach die eingehenden Zahlungen aus diesem Kontoauszug mit dieser CSV ab. Erstelle drei Tabellen: (1) ubereinstimmende Zahlungen, (2) Zahlungen ohne passende Rechnung, (3) Rechnungen ohne Zahlungseingang. Markiere unklare Ubereinstimmungen.

## Block 4: Backup-Szenarien

Vertrag: demo-vertrag.pdf
Lies diesen Vertrag aus der Perspektive eines Freelancers. Fasse die wichtigsten Klauseln in einfachem Deutsch zusammen: Zahlungsbedingungen, Kündigungsfristen, Haftung und geistiges Eigentum. Markiere ungewöhnliche oder nachteilige Klauseln.

Posteingang: demo-posteingang.txt
Kategorisiere diese E-Mails nach Priorität: Heute antworten / Diese Woche / Keine Aktion nötig. Gib für jede E-Mail auch den empfohlenen Antwortton und den geschätzten Aufwand an.

Offene Rechnungen: demo-offene-rechnungen.xlsx
Diese Liste enthält Kunden mit überfälligen Zahlungen. Schreibe für jeden Kunden eine Zahlungserinnerung in dem zur Verzugsdauer passenden Ton: 1–14 Tage: freundlich und erinnernd; 15–30 Tage: bestimmt und klar; 30+ Tage: formell und ergebnisorientiert.

## Hinweis

Alle Daten sind fiktiv. Namen und Beträge sind absichtlich realistisch gewählt.
