# Workflow: Unterrichtsreihe

## Zweck
Plant eine mehrstündige Unterrichtsreihe zu einem Thema: Kompetenzen, Lernziele, Stundenübersicht, Material, Methoden, Differenzierung, Leistungsüberprüfung und Hausaufgaben. Bindeglied zwischen Jahresplanung/Stoffverteilungsplan (grobe Ebene) und Stundenentwurf (Einzelstunde).

## Eingaben
Pflicht:
- Thema der Reihe
- Klassenstufe (5–12)
- Fach (Deutsch oder Evangelische Religion)
- Ungefähre Stundenzahl der Reihe

Optional (mit Annahme-Kennzeichnung bei Fehlen):
- Bildungsgang (bei Klasse 9–12 zu klären, siehe Bildungsgang-Prüfung)
- Vorwissen/Anschluss an vorherige Reihe (falls unbekannt: Annahme „Reihe steht am Anfang eines neuen Themenblocks, kein spezifisches Vorwissen vorausgesetzt")
- Differenzierungsbedarf der Klasse (nur funktional beschrieben, keine Diagnosen)
- Verfügbare Medien/Ausstattung (Whiteboard, Tablets, Bibliothek) — bei Fehlen: Standardannahme „klassische Ausstattung: Tafel/Whiteboard, Kopiergerät"
- Geplanter Leistungsnachweis am Ende der Reihe (Klassenarbeit, Test, Projektbewertung)

Bei unklarem Bildungsgang in Klasse 9/10: Rückfrage oder sichtbar markierte Annahme.

## Vorgehen
1. Bildungsgang klären/Annahme setzen (siehe Bildungsgang-Prüfung).
2. Passende Lehrplandatei(en) laden und relevanten Kompetenzbereich zum Thema identifizieren.
3. Groblernziele der Reihe formulieren (was können die Schüler am Ende, kompetenzorientiert).
4. Reihe in Einzelstunden gliedern (Anzahl passend zur vorgegebenen Stundenzahl), jeder Stunde ein Kernthema/Teilziel zuordnen.
5. Methodische Grundentscheidungen treffen (z. B. handlungsorientiert, textanalytisch, projektorientiert bei Deutsch; symboldidaktisch, dialogisch bei Religion) und pro Stunde grob vermerken.
6. Materialbedarf für die gesamte Reihe zusammenstellen (Texte, Arbeitsblätter, Medien), Bezug zu vorhandenen Vorlagen aus `templates/` prüfen.
7. Differenzierungsansatz für die Reihe festlegen (z. B. gestufte Aufgaben, Wahlaufgaben, Sockelaufgaben) — Ebene 2/3 kennzeichnen.
8. Leistungsüberprüfung planen: Form, Zeitpunkt innerhalb/am Ende der Reihe, Bezug zu `klassenarbeit.md`, falls eine Klassenarbeit folgt.
9. Hausaufgaben pro Stundenblock grob skizzieren, keine Detailausformulierung (das leistet der Stundenentwurf).
10. Quellenbezug für Kompetenzen und Inhalte dokumentieren.
11. Vier-Ebenen-Kennzeichnung anwenden, Qualitätscheck durchlaufen, Ausgabe erzeugen.

## Bildungsgang-Prüfung
- Klasse 5–8: Sekundarschule, keine Rückfrage.
- Klasse 9–10: klären. Sekundarschulabschluss/mittlerer Schulabschluss → Sekundarschule; gymnasialer Bildungsgang → Gymnasium, Klasse 10 = Einführungsphase.
- Klasse 11–12: nur Gymnasium, Qualifikationsphase/Abiturbezug prüfen — bei Abiturrelevanz Methoden und Anforderungsniveau entsprechend heben (stärkerer Textanalyse-/Diskursanspruch).
- Bei Unklarheit: Auflösung nach `routing_rules.json`, Grenzfälle gegen `bildungsgang_guardrails.md` prüfen.
- Ausgabekopf trägt „Bildungsgang: <…>".

## Lehrplanbezug
- Herangezogen wird die Datei `data/curriculum/<fach>/<bildungsgang>/klasse_<nn>.md` der betreffenden Klassenstufe; bei thematischer Überschneidung mit Nachbarklassen (z. B. Reihe zieht sich über Halbjahresgrenze) auch diese Datei prüfen.
- Kopfzeile weist aus: Schulform, Bildungsgang, Lehrplanbasis (Sekundarschule/Gymnasium/kombiniert/unklar).
- Jeder benannte Kompetenzbereich erhält Quellenangabe (Datei, Abschnitt/Fundstelle).
- Fehlt eine passende Lehrplandatei, Thema als Ebene 4 „noch zu prüfen" markieren statt Kompetenzen zu erfinden.

## Ausgabeformat
- Kopfzeile: Thema | Klasse | Bildungsgang | Lehrplanbasis | Fach | Dauer (Stundenzahl)
- Abschnitt Kompetenzen/Lernziele (Fließtext oder Liste, mit Quellenbezug)
- Tabelle Stundenübersicht: Std.-Nr. | Kernthema | Kompetenzbezug | Methode | Material
- Abschnitt Differenzierung, Abschnitt Leistungsüberprüfung, Abschnitt Hausaufgaben (grob, stundenweise)
- Nutzt `templates/unterrichtsreihe.md` als Strukturvorlage.
- Abschließend: Quellenverzeichnis.

## Qualitätscheck
- Lehrplanbasis im Kopf ausgewiesen?
- Bildungsgang geklärt oder Annahme markiert?
- Stundenübersicht deckt die vorgegebene Stundenzahl vollständig und plausibel ab?
- Kompetenzen mit Quelle belegt?
- Differenzierung funktional beschrieben, keine Diagnosen, keine Schülernamen?
- Vier-Ebenen-Kennzeichnung konsequent angewendet?
- Leistungsüberprüfung sinnvoll in Reihe eingebettet?
- Nur Deutsch oder Ev. Religion abgedeckt?

## Beispielprompt
„Plane eine Unterrichtsreihe zum Thema Kurzgeschichten für Deutsch, Klasse 8, Sekundarschule, ca. 8 Stunden, mit abschließender Klassenarbeit."
