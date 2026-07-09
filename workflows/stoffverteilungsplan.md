# Workflow: Stoffverteilungsplan

## Zweck
Erstellt einen granularen, wochenbasierten Stoffverteilungsplan für ein Schuljahr (Fach Deutsch oder Evangelische Religion, Klasse 5–12 an der Gemeinschaftsschule Sachsen-Anhalt). Der Plan ordnet Themen, Kompetenzen, Materialideen und Leistungsnachweise den Kalenderwochen zu und bildet Ferien/Feiertage sowie Pufferzeit ab. Dient als verbindliches Arbeitsdokument für Fachkonferenz und Unterrichtsvorbereitung.

## Eingaben
Pflicht:
- Fach (Deutsch oder Evangelische Religion)
- Klassenstufe (5–12)
- Schuljahr (z. B. 2026/27)
- Wochenstundenzahl laut Stundentafel

Optional (mit Annahme-Kennzeichnung bei Fehlen):
- Bildungsgang (bei Klasse 9–12 zwingend zu klären, siehe Bildungsgang-Prüfung)
- Ferientermine/Feiertage Sachsen-Anhalt für das Schuljahr (falls nicht angegeben: Platzhalter „[Ferienwoche einsetzen]" statt konkreter Daten, kein Erfinden von Terminen)
- Zahl der Klassenarbeiten laut schulinterner Vorgabe
- Vorkenntnisse/Lernstand der Klasse (falls unbekannt: Annahme „durchschnittlicher Kenntnisstand laut Lehrplanprogression" markieren)
- Differenzierungsbedarf (z. B. LRS, DaZ) — nur funktional/beobachtungsbasiert, keine Diagnosen

Wenn Bildungsgang bei Klasse 9–10 unklar bleibt: Rückfrage stellen, ersatzweise Plan mit sichtbar markierter Annahme „Sekundarschule (Regelannahme, da nicht angegeben)" erstellen und Hinweis auf Klärungsbedarf voranstellen.

## Vorgehen
1. Eingaben validieren, insbesondere Bildungsgang-Status (siehe Bildungsgang-Prüfung) klären oder Annahme setzen.
2. Lehrplanbasis bestimmen und passende Dateien aus `data/curriculum/` laden (siehe Lehrplanbezug).
3. Schuljahreswochen grob strukturieren: Gesamtwochenzahl abzüglich Ferien, Feiertage, Prüfungswochen ermitteln; Pufferwochen einplanen (mind. 2–3 pro Halbjahr, je nach Klassenstufe mehr bei Klasse 9/10 wegen Prüfungsvorbereitung).
4. Themenfolge aus dem Lehrplan in Unterrichtsreihen bündeln, chronologisch anordnen (thematische Progression, Jahreszeitenbezug bei Religion beachten, Textsortenprogression bei Deutsch beachten).
5. Jeder Woche zuordnen: Thema/Unterrichtsreihe, Kompetenzbereich(e) laut Lehrplan, grobe Materialidee, ggf. Leistungsnachweis-Termin.
6. Klassenarbeiten/Leistungsnachweise auf sinnvolle Abstände verteilen (nicht in Ferienwochen, nicht in ersten/letzten Schulwochen ballen).
7. Differenzierungshinweise pro Reihe ergänzen (Ebene 2: didaktisch ergänzt), keine schülerbezogenen Daten.
8. Pufferstunden explizit ausweisen (für Wiederholung, Vertretung, aktuelle Anlässe).
9. Quellenbezug für jede Lehrplanaussage dokumentieren.
10. Vier-Ebenen-Kennzeichnung pro Abschnitt prüfen und ergänzen.
11. Qualitätscheck durchlaufen, dann Ausgabe im Zielformat erzeugen.

## Bildungsgang-Prüfung
- Klasse 5–8: Lehrplanbasis Sekundarschule, keine Rückfrage nötig.
- Klasse 9–10: Bildungsgang muss geklärt sein (Sekundarschulabschluss/mittlerer Schulabschluss vs. gymnasialer Bildungsgang). Klasse 10 im gymnasialen Bildungsgang zählt als Einführungsphase (Oberstufe) — eigene Lehrplanlogik, nicht mit Sekundarschule Klasse 10 verwechseln.
- Klasse 11–12: nur Gymnasium, Qualifikationsphase, Abiturbezug prüfen (Kurshalbjahr, ggf. Leistungs-/Grundkurs falls relevant).
- Bei fehlender Angabe: siehe `routing_rules.json` für die Standardauflösung je Klassenstufe; bei Widersprüchen oder Unklarheit an `bildungsgang_guardrails.md` prüfen, ob Rückfrage zwingend ist (Klasse 9/10) oder Annahme zulässig (Klasse 5–8).
- Ergebnis der Prüfung im Ausgabekopf als „Bildungsgang: <…>" ausweisen.

## Lehrplanbezug
- Herangezogen werden die passenden Dateien aus `data/curriculum/<fach>/<bildungsgang>/klasse_<nn>.md` (z. B. `data/curriculum/deutsch/sekundarschule/klasse_05.md`, `data/curriculum/religion/gymnasium/klasse_09.md`).
- Bei gymnasialem Bildungsgang Klasse 10 (Einführungsphase) prüfen, ob eine eigene Datei existiert oder auf Qualifikationsphase-Vorstufe verwiesen wird; fehlt die Datei, als „Lehrplanbasis: unklar, Quelle unvollständig" (Ebene 4) kennzeichnen.
- Lehrplanbasis wird im Kopf jeder Ausgabe ausgewiesen: Schulform, Bildungsgang, Lehrplanbasis (Sekundarschule/Gymnasium/kombiniert/unklar).
- Jede Themenzeile erhält, wo möglich, einen Quellenverweis (Datei, Abschnitt/Kompetenzbereich, Klasse).

## Ausgabeformat
- Kopfzeile: Fach | Klasse | Schuljahr | Bildungsgang | Lehrplanbasis
- Tabelle je Woche: KW | Zeitraum (Platzhalter falls kein Kalender vorliegt) | Thema/Reihe | Kompetenzen | Material | Leistungsnachweis | Anmerkung
- Nutzt `templates/stoffverteilungsplan.md` als Strukturvorlage; Abweichungen vom Template nur begründet.
- Abschließender Block: Pufferstunden-Übersicht, Differenzierungshinweise, Quellenverzeichnis.

## Qualitätscheck
- Lehrplanbasis im Kopf ausgewiesen?
- Bildungsgang bei Klasse 9–10 geklärt oder Annahme sichtbar markiert?
- Jede Themenzeile mit Quelle belegt (Datei + Abschnitt)?
- Vier-Ebenen-Kennzeichnung bei allen nicht direkt aus dem Lehrplan ableitbaren Aussagen vorhanden?
- Keine echten Schülernamen, keine Diagnosen, Datenschutz-Warnhinweis bei personenbezogenen Angaben gesetzt?
- Ferien/Feiertage als Platzhalter statt erfundener Daten?
- Pufferstunden ausgewiesen?
- Nur Deutsch oder Ev. Religion abgedeckt (kein kath. RU/Ethik)?

## Beispielprompt
„Erstelle einen Stoffverteilungsplan für Deutsch, Klasse 9, Schuljahr 2026/27. Bildungsgang noch unklar, bitte prüfen. Vier Klassenarbeiten sind vorgesehen."
