# Workflow: Klassenarbeit

## Zweck
Erstellt eine vollständige Klassenarbeit inklusive Aufgaben, Operatoren, Anforderungsbereichen (AFB I/II/III), Punkteverteilung, Erwartungshorizont und Bewertungsschlüssel. Deckt Deutsch und Evangelische Religion für Klasse 5–12 ab, mit besonderer Sorgfalt bei Bildungsgang-Zuordnung im Übergangsbereich und in der Oberstufe.

## Eingaben
Pflicht:
- Thema/Themenbereich
- Klassenstufe (5–12)
- Fach (Deutsch oder Evangelische Religion)
- Dauer der Arbeit

Optional (mit Annahme-Kennzeichnung bei Fehlen):
- Bildungsgang (bei Klasse 9–12 zwingend zu klären, siehe Bildungsgang-Prüfung und Zusatzregel)
- Gesamtpunktzahl/Notenschlüssel-Vorgabe der Schule (bei Fehlen: Standard-Bewertungsschlüssel nach gängiger Prozentstaffelung verwenden und als Annahme kennzeichnen)
- Aufgabenanzahl/-struktur (bei Fehlen: 3–4 Aufgaben mit steigendem Anforderungsniveau als Standard)
- Hilfsmittel (Wörterbuch, Bibel, Textausgabe) — bei Fehlen: themenabhängige Standardannahme treffen und kennzeichnen
- Differenzierungshinweis für einzelne Schüler (nur funktional, keine Diagnosen, keine Namen)

Bei unklarem Bildungsgang in Klasse 9/10: zwingende Rückfrage, da die Lehrplanbasis (Sekundarschule vs. Gymnasium/Einführungsphase) direkt die Aufgabenschwierigkeit bestimmt. Ersatzweise nur mit deutlich sichtbarer Annahme und Warnhinweis arbeiten.

## Vorgehen
1. Bildungsgang klären/Annahme setzen (siehe Bildungsgang-Prüfung und Zusatzregel).
2. Passende Lehrplandatei laden, zu prüfende Kompetenzen und Inhalte für das Thema bestimmen.
3. Aufgabenstruktur festlegen (Anzahl, Reihenfolge nach steigendem Anforderungsniveau).
4. Pro Aufgabe: Operator wählen (z. B. „nennen", „erläutern", „analysieren", „beurteilen"), passenden Anforderungsbereich zuordnen (AFB I: Reproduktion, AFB II: Anwendung/Transfer, AFB III: Reflexion/Bewertung).
5. Punkte pro Aufgabe/Teilaufgabe festlegen, Gesamtpunktzahl bilden; AFB-Verteilung grob prüfen (üblich: AFB I ca. 30–40 %, AFB II ca. 40–50 %, AFB III ca. 15–25 %, je nach Klassenstufe und Fach anpassen).
6. Erwartungshorizont je Aufgabe ausformulieren: erwartete Inhalte/Argumente, Bewertungskriterien, Zuordnung der Punkte zu Teilleistungen.
7. Bewertungsschlüssel (Punkte-zu-Note-Tabelle) erstellen oder Schulvorgabe übernehmen.
8. Differenzierungshinweis ergänzen, falls angefragt (z. B. Zeitverlängerung, angepasste Aufgabenmenge) — funktional formuliert, kein Bezug zu einzelnen Schülern per Name.
9. Quellenbezug für geprüfte Kompetenzen dokumentieren.
10. Vier-Ebenen-Kennzeichnung anwenden, Qualitätscheck durchlaufen, Ausgabe erzeugen.

## Bildungsgang-Prüfung
- Klasse 5–8: Sekundarschule, keine Rückfrage.
- Klasse 9–10: zwingend klären. Sekundarschulabschluss/mittlerer Schulabschluss → Sekundarschule; gymnasialer Bildungsgang → Gymnasium, Klasse 10 = Einführungsphase.
- Klasse 11–12: nur Gymnasium, Qualifikationsphase, Abiturbezug prüfen.
- Auflösung unklarer Fälle nach `routing_rules.json`, Grenzfälle gegen `bildungsgang_guardrails.md` prüfen.
- Ausgabekopf trägt „Bildungsgang: <…>".

**Zusatzregel für Klassenarbeiten:** Bei Klasse 11–12 oder erkennbarem Abiturbezug ist zwingend die gymnasiale Lehrplanbasis (Gymnasium-FLP) zu verwenden. Bei Klasse 9–10 im gymnasialen Bildungsgang gilt ebenfalls die Gymnasium-FLP, nicht die Sekundarschul-Lehrplanbasis — dies gilt selbst dann, wenn die Klasse organisatorisch an einer Gemeinschaftsschule unterrichtet wird. Eine Verwechslung führt zu falschem Anforderungsniveau und ist vor Ausgabe der Arbeit auszuschließen.

## Lehrplanbezug
- Herangezogen wird `data/curriculum/<fach>/<bildungsgang>/klasse_<nn>.md` der betreffenden Klassenstufe; bei Abiturbezug zusätzlich vorhandene Hinweise zu Prüfungsschwerpunkten in den Gymnasium-Dateien prüfen.
- Kopfzeile weist aus: Schulform, Bildungsgang, Lehrplanbasis (Sekundarschule/Gymnasium/kombiniert/unklar).
- Jede geprüfte Kompetenz erhält Quellenangabe (Datei, Abschnitt/Fundstelle).
- Fehlt die passende Lehrplandatei (z. B. Gymnasium Klasse 10/Einführungsphase), Thema als Ebene 4 „noch zu prüfen" kennzeichnen statt Anforderungen zu erfinden.

## Ausgabeformat
- Kopfzeile: Thema | Klasse | Bildungsgang | Lehrplanbasis | Fach | Dauer | Gesamtpunktzahl
- Aufgabenteil: nummerierte Aufgaben mit Operator, AFB-Stufe, Punktzahl je Teilaufgabe
- Abschnitt Erwartungshorizont: je Aufgabe erwartete Antwort/Kriterien und Punktzuordnung
- Abschnitt Bewertungsschlüssel: Punkte-Note-Tabelle
- Abschnitt Differenzierungshinweis (falls zutreffend)
- Nutzt vorhandene Vorlagen aus `templates/`, sofern für Klassenarbeiten vorhanden; sonst orientiert sich die Ausgabe an dieser Workflow-Struktur.
- Abschließend: Quellenverzeichnis.

## Qualitätscheck
- Lehrplanbasis im Kopf ausgewiesen, Zusatzregel für Klasse 9–12/Abiturbezug korrekt angewendet (Gymnasium-FLP statt Sekundarschule)?
- Bildungsgang bei Klasse 9–10 geklärt, keine unzulässige Annahme ohne Warnhinweis?
- AFB-Verteilung ausgewogen und ausgewiesen?
- Punktesumme der Aufgaben stimmt mit Gesamtpunktzahl überein?
- Erwartungshorizont vollständig, Bewertungsschlüssel vorhanden?
- Kompetenzbezug mit Quelle belegt?
- Vier-Ebenen-Kennzeichnung konsequent angewendet?
- Keine echten Schülernamen, keine Diagnosen, Differenzierungshinweis funktional formuliert?
- Nur Deutsch oder Ev. Religion abgedeckt?

## Beispielprompt
„Erstelle eine Klassenarbeit für Deutsch, Klasse 10, gymnasialer Bildungsgang (Einführungsphase), Thema Kurzgeschichteninterpretation, 90 Minuten, mit Erwartungshorizont und Bewertungsschlüssel."
