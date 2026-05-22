# AI Workshop — Build Session One-Pager

Datum: 2026-05-23
Ort: SAALBAU Bornheim, Frankfurt am Main

## Worum es heute geht

- Mit echten Demo-Dateien typische Admin- und Wissensarbeit schneller erledigen
- Unklare Fälle, Ausnahmen und Risiken sichtbar machen
- Prompts so formulieren, dass sofort nutzbare Ergebnisse entstehen

## Demo 1: Kontoauszug + Rechnungsliste aufbauen

Dateien: demo-kontoauszug.csv, demo_data/
Aufgabe:
- aus den Rechnungs-PDFs erst eine kompakte Rechnungsliste erstellen
- Zahlungen mit Rechnungen abgleichen
- offene und nur teilweise bezahlte Rechnungen finden
- unklare Treffer und fremde Zahlungseingänge markieren

Schritte mit Claude:
- PDFs in Claude Web hochladen oder direkte Dateilinks senden
- daraus eine CSV-Rechnungsliste erzeugen lassen
- die CSV dann mit dem Kontoauszug abgleichen

Beispielprompt:
Ich lade dir jetzt mehrere Rechnungen als PDF hoch. Alternativ sende ich dir direkte Dateilinks zu diesen PDFs. Lies alle Rechnungen und erstelle daraus eine CSV-Rechnungsliste mit Rechnungsnummer, Kunde, Datum, Betrag, Falligkeitsdatum und Zahlungsstatus.
Gleiche danach die eingehenden Zahlungen aus dem Kontoauszug mit dieser CSV-Liste ab und markiere unklare Treffer.

## Backup-Demos

Vertrag: demo-vertrag.pdf
- riskante Klauseln zusammenfassen
Posteingang: demo-posteingang.txt
- E-Mails nach Priorität sortieren
Offene Rechnungen: demo-offene-rechnungen.xlsx
- passende Zahlungserinnerungen formulieren

## Worauf ihr achten solltet

- nicht nur exakte Treffer suchen
- auch Teilzahlungen, Namensvarianten und Ausreißer erkennen
- Ergebnisse immer als Tabelle oder klare Liste zurückgeben lassen

## Hinweis

Alle Daten sind vollständig fiktiv, aber bewusst realistisch gestaltet.
