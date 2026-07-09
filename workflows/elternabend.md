# Workflow: Elternabend

## Zweck
Plant einen Klassenelternabend: Ablaufplan mit Zeitrahmen, Themenliste, Moderationshinweise. Verweist für Einladung auf `elternbrief.md` und für Nachbereitung auf `gespraechsprotokoll.md`, statt diese Inhalte zu duplizieren.

## Eingaben
Pflicht:
- Klasse
- Anlass/Hauptthema (z. B. "Klassenfahrt planen", "Übergang Klasse 8→9", "regulärer Jahres-Elternabend")

Optional:
- Datum/Uhrzeit, verfügbarer Zeitrahmen (Standardannahme: 90 Minuten, falls nicht angegeben — als Annahme kennzeichnen)
- Zusätzliche Tagesordnungspunkte (TOPs) vom User
- Beteiligte Personen (Elternvertretung, Fachlehrkräfte, Schulleitung) — nur mit Rolle benennen, keine Klarnamen nötig
- Ob ein Protokoll angefertigt werden soll (Standard: ja)

Fehlt der Zeitrahmen, wird mit 90 Minuten und 5 TOPs geplant; das wird im Kopf der Ausgabe als Annahme markiert.

## Vorgehen
1. Hauptthema und Pflicht-TOPs festlegen (Begrüßung, Hauptthema, sonstiges, Verabschiedung sind Standard-Rahmen).
2. Zeitrahmen auf TOPs verteilen, realistische Minutenangaben (Begrüßung kurz, Hauptthema größter Block, Zeitpuffer für Fragen einplanen).
3. Moderationshinweise pro TOP formulieren: Wie eröffnen, wie strukturieren, wie zu Wortmeldungen überleiten, wie abschließen.
4. Einladungstext nicht selbst erzeugen, sondern auf `elternbrief.md` (Anlass: "Einladung Elternabend", Tonvariante: freundlich) verweisen.
5. Protokollführung ankündigen und auf `gespraechsprotokoll.md` verweisen, sofern gewünscht.
6. Datenschutz-Hinweis zu Wortmeldungen ergänzen (siehe unten).
7. Ablaufplan als Tabelle ausgeben, Qualitätscheck durchführen.

## Bildungsgang-Prüfung
Für Elternabende in Klasse 5–8 im Regelfall irrelevant. Relevant wird der Bildungsgang bei Themen wie "Übergangsberatung Klasse 9/10" oder "Wahl des Bildungsgangs" — hier ist laut `routing_rules.json` zu klären, ob der Elternabend klassenweit (gemischte Bildungsgänge) oder bildungsgangspezifisch (z. B. nur E-Kurs-Eltern) stattfindet. Bei gemischten Bildungsgängen im TOP "Bildungsgang/Abschluss" explizit beide Wege (Sekundarschulabschluss und gymnasialer Bildungsgang) neutral darstellen, keinen Weg bevorzugen. Für Klasse 11–12 gilt automatisch Gymnasium/Qualifikationsphase — Themen wie Abiturvorbereitung, Kurswahl, Facharbeit sind dort einschlägig.

## Lehrplanbezug
Kein Lehrplanbezug. `data/curriculum/`-Dateien werden nicht herangezogen, da ein Elternabend eine organisatorische Veranstaltung ist. Ausnahme: Enthält der Elternabend einen fachlichen TOP (z. B. "Vorstellung der Lektüreauswahl Deutsch Kl. 8"), kann dieser TOP knapp mit dem betroffenen Fach/Thema benannt werden — ohne formale Quellenangabe oder Vier-Ebenen-Kennzeichnung, da die inhaltliche Ausarbeitung selbst nicht Teil dieses Workflows ist.

## Ausgabeformat
Kein dediziertes Template in `templates/` vorhanden — Ausgabe als strukturierter Ablaufplan:

1. Kopf: Klasse, Anlass, Datum/Uhrzeit (oder Platzhalter), Zeitrahmen, Hinweis auf Annahmen.
2. Tabelle Ablaufplan: TOP | Zeit (Start–Ende, Dauer) | Inhalt | Moderationshinweis
3. Abschnitt "Vorbereitung": Materialien, Raumbedarf, wer lädt ein (Verweis auf `elternbrief.md`).
4. Abschnitt "Nachbereitung": Protokollpflicht, Verweis auf `gespraechsprotokoll.md`, Verteilung des Protokolls.
5. Datenschutz-Hinweis als eigener kurzer Absatz.

## Qualitätscheck
- Zeitrahmen realistisch verteilt, Summe der TOP-Zeiten passt zum Gesamtrahmen
- Zeitpuffer für Fragen/Diskussion vorhanden
- Moderationshinweise konkret, keine Floskeln
- Einladung nicht dupliziert, sondern korrekt auf `elternbrief.md` verwiesen
- Protokoll nicht dupliziert, sondern korrekt auf `gespraechsprotokoll.md` verwiesen
- Datenschutz-Hinweis zu Wortmeldungen enthalten (keine Zitate mit Namen im späteren Protokoll ohne Zustimmung)
- Bildungsgang-TOP neutral formuliert, falls einschlägig (Klasse 9–10)
- Kein Lehrplanbezug-Fall korrekt vermerkt

## Beispielprompt
"Plan mir den Elternabend für die 9c, Hauptthema ist die Bildungsgang-Entscheidung Sekundarschulabschluss vs. gymnasialer Bildungsgang, 90 Minuten, Termin steht noch nicht fest."
