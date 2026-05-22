# Demo 1: Kontoauszug + Rechnungsliste aufbauen

[Zur Übersicht](README.de.md) | [Weiter zu Demo 2](demo-2.de.md)

## Ziel

- aus Rechnungs-PDFs zuerst eine einfache Rechnungsliste erstellen
- Zahlungen mit Rechnungen abgleichen
- offene Rechnungen finden
- Teilzahlungen erkennen
- Namensabweichungen und Fremdzahlungen markieren

## Dateien

- [artifacts/demo-kontoauszug.csv](artifacts/demo-kontoauszug.csv)
- [artifacts/demo_data](artifacts/demo_data)

## Schritte mit Claude Web

1. Öffne die Beispiel-Rechnungen aus [artifacts/demo_data](artifacts/demo_data).
2. Lade die PDF-Dateien einzeln in Claude hoch oder sende direkte Dateilinks zu den PDFs.
3. Lass daraus eine CSV-Datei mit den Spalten Rechnungsnummer, Kunde, Datum, Betrag, Fälligkeitsdatum und Zahlungsstatus erstellen.
4. Nutze diese CSV danach zusammen mit [artifacts/demo-kontoauszug.csv](artifacts/demo-kontoauszug.csv) für den Zahlungsabgleich.

## Beispielprompt

```text
Ich lade dir jetzt mehrere Rechnungen als PDF hoch. Alternativ sende ich dir direkte GitHub-Dateilinks zu diesen PDFs. Lies alle Rechnungen und erstelle daraus eine CSV-Datei mit den Spalten Rechnungsnummer, Kunde, Datum, Betrag, Fälligkeitsdatum und Zahlungsstatus. Nutze diese CSV anschließend zusammen mit dem Kontoauszug für den Abgleich. Erstelle drei Tabellen: (1) übereinstimmende Zahlungen, (2) Zahlungen ohne passende Rechnung, (3) Rechnungen ohne Zahlungseingang. Markiere unklare Übereinstimmungen.
```

## Worauf man achten sollte

- In Claude Web ist Datei-Upload meist verlässlicher als nur ein Ordnerpfad.
- Wenn Links genutzt werden, dann einzelne PDF-Dateilinks statt nur ein Repo-Ordner.
- Müller GmbH und K. Müller sind absichtlich kein exakter Match.
- Innovate GmbH ist nur teilweise bezahlt.
- Fiverr und Ref. 2024-123 gehören nicht sauber zur Rechnungsliste.
- Adobe, Slack, Notion und Bankgebühren sind Ausgaben, keine Rechnungszahlungen.

## Erwartete Haupterkenntnisse

- Offen oder nicht vollständig bezahlt: 2025-053, 2025-055, 2025-056
- Spät bezahlt: 2025-050
- Unklare oder nicht zugeordnete Buchungen: Ref. 2024-123, Fiverr Auszahlung

## Referenz

- [artifacts/demo-answer-key.md](artifacts/demo-answer-key.md)

[Zur Übersicht](README.de.md) | [Weiter zu Demo 2](demo-2.de.md)