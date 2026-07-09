# Workflow: Stundenentwurf

## Zweck
Erstellt einen detaillierten Entwurf für eine Einzelstunde: Lernziel, Kompetenzbezug, Phasenmodell mit Lehrer- und Schülerhandeln, Sozialformen, Material, Zeitangaben, Tafelbild/Sicherung, Differenzierung und Reserve. Geeignet für eigene Vorbereitung wie für Unterrichtsbesuche.

## Eingaben
Pflicht:
- Thema der Stunde
- Klassenstufe (5–12)
- Fach (Deutsch oder Evangelische Religion)
- Dauer (i. d. R. 45 oder 90 Minuten)

Optional (mit Annahme-Kennzeichnung bei Fehlen):
- Bildungsgang (bei Klasse 9–12 zu klären, siehe Bildungsgang-Prüfung)
- Einordnung in eine Unterrichtsreihe (falls unbekannt: Annahme „Einzelstunde ohne bekannten Reihenkontext, Lernziel eigenständig formuliert")
- Lerngruppenmerkmale (Größe, Zusammensetzung) — nur funktional, keine Diagnosen
- Verfügbare Medien/Ausstattung (Standardannahme bei Fehlen: Tafel/Whiteboard, Kopiergerät)
- Anlass (Unterrichtsbesuch, reguläre Stunde) — beeinflusst Detailtiefe der Reflexion

Bei unklarem Bildungsgang in Klasse 9/10: Rückfrage oder sichtbar markierte Annahme.

## Vorgehen
1. Bildungsgang klären/Annahme setzen (siehe Bildungsgang-Prüfung).
2. Passende Lehrplandatei laden, Kompetenzbezug für das Thema bestimmen.
3. Stundenlernziel präzise und überprüfbar formulieren (ein Hauptziel, ggf. Teilziele).
4. Phasenmodell festlegen: Einstieg, Erarbeitung (ggf. in mehrere Schritte), Sicherung, Abschluss/Ausblick — bei 90 Minuten zusätzlich Phasenwechsel/Bewegungspause einplanen.
5. Je Phase ausformulieren: Zeit, Lehrerhandeln, Schülerhandeln, Sozialform (Einzel-, Partner-, Gruppenarbeit, Plenum), Material.
6. Sicherung/Tafelbild konkret skizzieren (Stichpunkte oder Tafelbild-Beschreibung, kein bloßer Verweis „wird gesichert").
7. Differenzierungsmaßnahmen je Phase benennen, wo sinnvoll (z. B. gestufte Hilfen, Zusatzaufgaben) — funktional, keine Diagnosen.
8. Reservephase/-aufgabe für den Fall von Zeitüberschuss einplanen.
9. Kurzreflexion zu möglichen Störquellen oder Stolperstellen ergänzen (didaktische Ebene, keine Schülerbewertung).
10. Quellenbezug für Kompetenzen/Lernziel dokumentieren.
11. Vier-Ebenen-Kennzeichnung anwenden, Qualitätscheck durchlaufen, Ausgabe erzeugen.

## Bildungsgang-Prüfung
- Klasse 5–8: Sekundarschule, keine Rückfrage.
- Klasse 9–10: klären. Sekundarschulabschluss/mittlerer Schulabschluss → Sekundarschule; gymnasialer Bildungsgang → Gymnasium, Klasse 10 = Einführungsphase (höheres Abstraktionsniveau in Erarbeitung und Sicherung berücksichtigen).
- Klasse 11–12: nur Gymnasium, Qualifikationsphase/Abiturbezug — Anforderungsniveau der Aufgaben entsprechend anheben (AFB II/III-Schwerpunkt).
- Unklare Fälle nach `routing_rules.json` auflösen, Grenzfälle gegen `bildungsgang_guardrails.md` prüfen.
- Ausgabekopf trägt „Bildungsgang: <…>".

## Lehrplanbezug
- Herangezogen wird `data/curriculum/<fach>/<bildungsgang>/klasse_<nn>.md` der betreffenden Klassenstufe.
- Kopfzeile weist aus: Schulform, Bildungsgang, Lehrplanbasis (Sekundarschule/Gymnasium/kombiniert/unklar).
- Lernziel und Kompetenzbezug erhalten Quellenangabe (Datei, Abschnitt/Fundstelle).
- Fehlt eine passende Lehrplandatei, Kompetenzbezug als Ebene 4 „noch zu prüfen" kennzeichnen statt zu improvisieren.

## Ausgabeformat
- Kopfzeile: Thema | Klasse | Bildungsgang | Lehrplanbasis | Fach | Dauer
- Lernziel und Kompetenzbezug als eigener Block
- Tabelle Phasenverlauf: Zeit | Phase | Lehrerhandeln | Schülerhandeln | Sozialform | Material
- Abschnitt Tafelbild/Sicherung, Abschnitt Differenzierung, Abschnitt Reserve, Abschnitt Reflexion
- Nutzt `templates/stundenentwurf.md`, falls vorhanden, sonst orientiert sich die Ausgabe an dieser Workflow-Struktur.
- Abschließend: Quellenverzeichnis.

## Qualitätscheck
- Lehrplanbasis im Kopf ausgewiesen?
- Bildungsgang geklärt oder Annahme markiert?
- Zeitplan der Phasen summiert exakt auf die vorgegebene Dauer?
- Lernziel überprüfbar formuliert und mit Quelle belegt?
- Differenzierung funktional, keine Diagnosen, keine Schülernamen?
- Sicherung/Tafelbild konkret statt pauschal?
- Reserve vorhanden?
- Vier-Ebenen-Kennzeichnung konsequent angewendet?
- Nur Deutsch oder Ev. Religion abgedeckt?

## Beispielprompt
„Erstelle einen Stundenentwurf für Evangelische Religion, Klasse 6, Thema Schöpfungsgeschichte, 45 Minuten, für einen Unterrichtsbesuch."
