# Workflow: Bewertungsraster

## Zweck
Erstellt ein Kriterienraster für die Leistungsbewertung — für Klassenarbeiten/Klausuren, mündliche Leistungen oder Projektarbeiten — mit Kompetenzbezug, transparenter Punkte-/Notenzuordnung und Anpassbarkeit an den jeweiligen Aufgabentyp. Ziel: für Schüler nachvollziehbare, kriteriengeleitete Bewertung.

## Eingaben
Pflicht:
- Aufgabentyp/Leistungsform (schriftliche Arbeit, mündliche Leistung, Projekt, Präsentation, Portfolio o. ä.)
- Fach und Klassenstufe
- Zu bewertende Kompetenzbereiche (mind. grob benannt, z. B. „Textproduktion", „mündliche Beteiligung")

Optional (mit Annahme bei Fehlen):
- Gewichtung der Kriterien — ohne Angabe: gleichmäßige Gewichtung annehmen und kennzeichnen
- Punktzahl/Skala — ohne Angabe: 15-Punkte-Skala (gymnasiale Tradition) für Klasse 11–12, sonst Notenpunkte 1–6 bzw. Prozent-Punkte-Modell für Klasse 5–10, jeweils als Annahme markieren
- Bildungsgang — ohne Angabe: aus Klassenstufe ableiten, siehe Bildungsgang-Prüfung

## Vorgehen
1. Leistungsform und Kompetenzbereiche klären.
2. Kompetenzbereiche in konkrete, beobachtbare Kriterien herunterbrechen (z. B. „Textproduktion" → Aufbau, Sprachrichtigkeit, Ausdruck, Inhalt).
3. Je Kriterium Anspruchsstufen definieren (z. B. „voll erfüllt / teilweise erfüllt / nicht erfüllt" oder Punktespannen).
4. Gewichtung der Kriterien festlegen, Gesamtpunktzahl berechnen.
5. Punkte-Noten-Umrechnung ergänzen, unter Verweis auf den Leistungsbewertungserlass Sachsen-Anhalt bzw. schulinterne Fachschaftsbeschlüsse (falls letztere nicht vorliegen, Standardschlüssel als Annahme kennzeichnen).
6. Transparenzhinweis formulieren — wie das Raster den Schülern vor der Leistung kommuniziert werden sollte.
7. Anpassungshinweis ergänzen: welche Zeilen bei anderem Aufgabentyp zu verändern sind.
8. Lehrplanbezug und Quellenangabe ergänzen.
9. Qualitätscheck durchführen.

## Bildungsgang-Prüfung
- Klasse 5–8: Sekundarschul-Lehrplanbasis, Kompetenzformulierungen entsprechend.
- Klasse 9–10: Bildungsgang klären (Sekundarschulabschluss/mittlerer Schulabschluss vs. gymnasialer Bildungsgang). Bewertungsraster für Klasse 10 im gymnasialen Bildungsgang (Einführungsphase) orientiert sich bereits stärker an Oberstufenkriterien.
- Klasse 11–12: nur Gymnasium, Qualifikationsphase — 15-Punkte-System üblich, kein Sekundarschulbezug.
- Bei unklarem Bildungsgang: Rückfrage oder sichtbar markierte Annahme. Details in `routing_rules.json` und `bildungsgang_guardrails.md`.

## Lehrplanbezug
Kompetenzbereiche werden, soweit möglich, auf Formulierungen aus `data/curriculum/<fach>/<bildungsgang>/klasse_XX.md` zurückgeführt. Bei fachübergreifenden Kriterien (z. B. Ausdruck, Formalia), die nicht direkt im Lehrplan stehen, erfolgt Kennzeichnung als „didaktisch ergänzt". Bei Ev. Religion gilt: Kompetenzbereiche ausschließlich aus dem evangelischen RU-Lehrplan, kein katholischer RU oder Ethik.

## Ausgabeformat
Kopfzeile: `Schulform: Gemeinschaftsschule | Bildungsgang: <…> | Lehrplanbasis: <…>`
Raster als Tabelle: Kriterium | Kompetenzbezug | Anspruchsstufen/Punktespanne | Gewichtung.
Abschnitt „Punkte-Noten-Schlüssel" (Tabelle).
Abschnitt „Transparenzhinweis" (kurz, wie den Schülern kommuniziert wird).
Abschnitt „Anpassungshinweis" (was bei anderem Aufgabentyp zu ändern ist).
Abschnitt „Quellenbezug" (inkl. Verweis auf Leistungsbewertungserlass Sachsen-Anhalt).
Kein eigenes Template unter `templates/` — Tabellenstruktur an `templates/stoffverteilungsplan.md` anlehnen.

## Qualitätscheck
- Lehrplanbasis ausgewiesen und zur Klassenstufe/Bildungsgang passend?
- Kriterien beobachtbar und nicht diagnostisch formuliert?
- Gewichtung und Gesamtpunktzahl schlüssig, Punkte-Noten-Schlüssel korrekt?
- Verweis auf Leistungsbewertungserlass Sachsen-Anhalt bzw. Kennzeichnung als Annahme, falls kein Fachschaftsbeschluss vorliegt?
- Vier-Ebenen-Kennzeichnung bei nicht direkt lehrplangedeckten Kriterien gesetzt?
- Quellen genannt?
- Für Schüler verständlich und transparent formuliert, keine personenbezogenen Daten?

## Beispielprompt
„Erstelle ein Bewertungsraster für die mündliche Mitarbeit in Ev. Religion, Klasse 8, mit den Kriterien fachliche Beteiligung, Argumentation und Zuhören."
