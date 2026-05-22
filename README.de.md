# AI Workshop Playbook

Dieses Repository ist so aufgebaut, dass Teilnehmende die Workshop-Demos selbstständig Schritt für Schritt nachgehen können.

## 1. Ziel

In diesem Workshop zeigen wir, wie man mit realistisch wirkenden Arbeitsdateien schneller zu brauchbaren Ergebnissen kommt. Im Fokus stehen Abgleich, Priorisierung, Risikoerkennung und Formulierungshilfe.

## 2. Für Wen

Freelancer, kleine Unternehmen, Agenturen, Office-Teams, Beratungs- und Backoffice-Rollen.

## 3. Repo-Inhalt

- [artifacts/demo-kontoauszug.csv](artifacts/demo-kontoauszug.csv): Kontoauszug
- [artifacts/demo-rechnungsliste.xlsx](artifacts/demo-rechnungsliste.xlsx): Rechnungsliste
- [artifacts/demo-vertrag.pdf](artifacts/demo-vertrag.pdf): Vertragsdemo
- [artifacts/demo-posteingang.txt](artifacts/demo-posteingang.txt): E-Mail-Triage-Demo
- [artifacts/demo-offene-rechnungen.xlsx](artifacts/demo-offene-rechnungen.xlsx): Offene Rechnungen
- [artifacts/demo_data](artifacts/demo_data): Einzelne Rechnungs-PDFs
- [artifacts/workshop-demo-guide.md](artifacts/workshop-demo-guide.md): Moderator-Guide
- [artifacts/demo-answer-key.md](artifacts/demo-answer-key.md): Erwartete Ergebnisse
- [artifacts/workshop-onepager.md](artifacts/workshop-onepager.md): Kurzüberblick
- [artifacts/workshop-onepager.pdf](artifacts/workshop-onepager.pdf): Printable one-pager
- [artifacts/demo-files-spec.json](artifacts/demo-files-spec.json): Zentrale Spezifikation

## 4. Schnellstart

1. Repository öffnen.
2. Mit Demo 1 starten.
3. Danach die Backup-Szenarien einzeln ausprobieren.

## 5. Workshop-Ablauf

### Demo 1: Kontoauszug + Rechnungsliste

Dateien:

- [artifacts/demo-kontoauszug.csv](artifacts/demo-kontoauszug.csv)
- [artifacts/demo-rechnungsliste.xlsx](artifacts/demo-rechnungsliste.xlsx)

Ziel:

- Zahlungen mit Rechnungen abgleichen
- offene Rechnungen finden
- Teilzahlungen erkennen
- Namensabweichungen und Fremdzahlungen markieren

Beispielprompt:

```text
Gleiche die eingehenden Zahlungen aus diesem Kontoauszug mit der beigefügten Rechnungsliste ab. Erstelle drei Tabellen: (1) übereinstimmende Zahlungen, (2) Zahlungen ohne passende Rechnung, (3) Rechnungen ohne Zahlungseingang. Markiere unklare Übereinstimmungen.
```

Worauf man achten sollte:

- Müller GmbH und K. Müller sind absichtlich kein exakter Match.
- Innovate GmbH ist nur teilweise bezahlt.
- Fiverr und Ref. 2024-123 gehören nicht sauber zur Rechnungsliste.
- Adobe, Slack, Notion und Bankgebühren sind Ausgaben, keine Rechnungszahlungen.

Erwartete Haupterkenntnisse:

- Offen oder nicht vollständig bezahlt: 2025-053, 2025-055, 2025-056
- Spät bezahlt: 2025-050
- Unklare oder nicht zugeordnete Buchungen: Ref. 2024-123, Fiverr Auszahlung

Referenz:

- [artifacts/demo-answer-key.md](artifacts/demo-answer-key.md)

### Demo 2: Vertrag prüfen

Datei:

- [artifacts/demo-vertrag.pdf](artifacts/demo-vertrag.pdf)

Ziel:

- riskante Vertragsklauseln erkennen
- Konsequenzen in einfacher Sprache erklären

Beispielprompt:

```text
Lies diesen Vertrag aus der Perspektive eines Freelancers. Fasse die wichtigsten Klauseln in einfachem Deutsch zusammen: Zahlungsbedingungen, Kündigungsfristen, Haftung und geistiges Eigentum. Markiere ungewöhnliche oder nachteilige Klauseln.
```

Erwartete Punkte:

- 90 Tage Zahlungsziel
- 3 Monate Kündigungsfrist plus automatische Verlängerung
- Rechteübergang schon bei Erstellung
- unbeschränkte Haftung
- breites Wettbewerbsverbot

### Demo 3: Posteingang priorisieren

Datei:

- [artifacts/demo-posteingang.txt](artifacts/demo-posteingang.txt)

Ziel:

- E-Mails priorisieren
- heute, diese Woche und später unterscheiden

Beispielprompt:

```text
Kategorisiere diese E-Mails nach Priorität: Heute antworten / Diese Woche / Keine Aktion nötig. Gib für jede E-Mail auch den empfohlenen Antwortton und den geschätzten Aufwand an.
```

### Demo 4: Offene Rechnungen nachverfolgen

Datei:

- [artifacts/demo-offene-rechnungen.xlsx](artifacts/demo-offene-rechnungen.xlsx)

Ziel:

- je nach Überfälligkeit den richtigen Ton treffen
- sanfte, klare und formelle Mahnungen unterscheiden

Beispielprompt:

```text
Diese Liste enthält Kunden mit überfälligen Zahlungen. Schreibe für jeden Kunden eine Zahlungserinnerung in dem zur Verzugsdauer passenden Ton: 1–14 Tage: freundlich und erinnernd; 15–30 Tage: bestimmt und klar; 30+ Tage: formell und ergebnisorientiert.
```

## 6. Selbst Lernen

1. Öffne nur die Dateien für einen Block.
2. Schreibe zuerst einen eigenen Prompt.
3. Vergleiche dein Ergebnis mit [artifacts/demo-answer-key.md](artifacts/demo-answer-key.md).
4. Formuliere den Prompt noch einmal besser.
5. Beobachte, wie sich Struktur und Ergebnisqualität verändern.

## 7. Für Trainer

- Nutze [artifacts/workshop-demo-guide.md](artifacts/workshop-demo-guide.md) als Ablaufhilfe.
- Nutze [artifacts/workshop-onepager.pdf](artifacts/workshop-onepager.pdf) als Handout.
- Nutze [artifacts/demo-answer-key.md](artifacts/demo-answer-key.md) als internen Referenzrahmen.

## 8. Hinweise zur Veröffentlichung

Alle Daten in diesem Repository sind fiktiv. Es gibt keine echten Konten, keine echten Rechnungen und keine echten personenbezogenen Daten.

## 9. Optionaler Nächster Schritt

Wenn du das Repository öffentlich teilst, ist es sinnvoll, Issues oder Discussions für Fragen von Teilnehmenden zu aktivieren.