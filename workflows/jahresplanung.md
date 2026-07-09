# Workflow: Jahresplanung

## Zweck
Erstellt einen Gesamtjahresüberblick für ein Fach und eine Klassenstufe, weniger granular als der Stoffverteilungsplan. Zeigt, wie mehrere Unterrichtsreihen über zwei Halbjahre verzahnt sind, wann Klassenarbeiten liegen, wie sich die Ferienstruktur auf die Planung auswirkt, und macht Bildungsgang-Übergänge (insbesondere Klasse 9/10) sichtbar. Zielgruppe: Fachkonferenz, Jahresplanungsgespräch, eigene Orientierung.

## Eingaben
Pflicht:
- Fach (Deutsch oder Evangelische Religion)
- Klassenstufe (5–12)
- Schuljahr

Optional (mit Annahme-Kennzeichnung bei Fehlen):
- Bildungsgang (bei Klasse 9–12 zwingend zu klären, siehe Bildungsgang-Prüfung)
- Anzahl Halbjahre/Kurshalbjahre (bei Oberstufe relevant)
- Zahl und grobe Lage der Klassenarbeiten/Leistungsnachweise laut Schulvorgabe
- Bereits feststehende schulische Großereignisse (Praktika, Projekttage, Exkursionen) — falls nicht angegeben: Platzhalter „[ggf. Praktikum/Projektwoche einplanen]"
- Ferienstruktur Sachsen-Anhalt für das Schuljahr (falls nicht angegeben: Platzhalter statt erfundener Daten)

Bei unklarem Bildungsgang in Klasse 9/10: Rückfrage stellen oder mit sichtbar markierter Annahme arbeiten und Klärungsbedarf voranstellen. Bei Klasse 11/12 ist Gymnasium gesetzt, keine Rückfrage nötig, aber Kurshalbjahr (falls relevant) erfragen.

## Vorgehen
1. Bildungsgang klären bzw. Annahme setzen (siehe Bildungsgang-Prüfung).
2. Lehrplanbasis bestimmen, relevante `data/curriculum/`-Dateien für die gesamte Klassenstufe sichten (nicht nur einzelne Wochenthemen).
3. Schuljahr in zwei Halbjahre gliedern, grobe Zeitfenster für Ferien/Feiertage markieren (Platzhalter, falls keine Termine vorliegen).
4. Lehrplaninhalte zu 4–7 großen Unterrichtsreihen pro Halbjahr bündeln (deutlich gröber als im Stoffverteilungsplan, keine Wochenebene).
5. Reihenfolge und Verzahnung prüfen: Aufbau aufeinander, thematische Klammern, Wiederholungsschleifen vor Prüfungsphasen.
6. Klassenarbeitstermine grob im Halbjahresraster verorten, Abstand zu Ferien und zu anderen Fächern (soweit bekannt) plausibel halten.
7. Bei Klasse 9/10: Übergang im Bildungsgang explizit thematisieren — z. B. Wechsel von Sekundarschule zu gymnasialem Bildungsgang, unterschiedliche Anforderungsniveaus, ggf. Anschlussfähigkeit der Reihen an Klasse 10/Einführungsphase prüfen.
8. Bei Klasse 11/12: Bezug zur Qualifikationsphase und zum Abitur herstellen (Kurshalbjahre, Themenschwerpunkte laut Abiturvorgaben, falls in den Lehrplandaten vorhanden).
9. Differenzierungs- und Pufferzeiten auf Halbjahresebene benennen (kein Wochendetail).
10. Quellenbezug je Reihe dokumentieren, Vier-Ebenen-Kennzeichnung anwenden.
11. Qualitätscheck durchlaufen, Ausgabe erzeugen.

## Bildungsgang-Prüfung
- Klasse 5–8: Sekundarschule, keine Rückfrage.
- Klasse 9–10: zwingend klären. Sekundarschulabschluss/mittlerer Schulabschluss → Sekundarschule; gymnasialer Bildungsgang → Gymnasium. Klasse 10 gymnasial = Einführungsphase, nicht mit Sekundarschule Klasse 10 gleichsetzen — die Jahresplanung muss diesen Unterschied im Aufbau der Reihen widerspiegeln.
- Klasse 11–12: nur Gymnasium, Qualifikationsphase, Abiturbezug prüfen.
- Auflösung unklarer Fälle laut `routing_rules.json`; Grenzfälle (z. B. Wechsel während des Schuljahres) gegen `bildungsgang_guardrails.md` prüfen.
- Ausgabekopf trägt „Bildungsgang: <…>", bei Übergangsjahrgängen zusätzlich Hinweis auf den Übergang.

## Lehrplanbezug
- Grundlage sind alle einschlägigen Dateien aus `data/curriculum/<fach>/<bildungsgang>/klasse_<nn>.md` der betroffenen Klassenstufe; bei Übergangsbetrachtung (Kl. 9/10) zusätzlich die Nachbarklasse zur Anschlussprüfung heranziehen.
- Lehrplanbasis wird im Kopf ausgewiesen: Schulform, Bildungsgang, Lehrplanbasis (Sekundarschule/Gymnasium/kombiniert/unklar) — „kombiniert", wenn im selben Schuljahr zwei Bildungsgänge relevant sind (z. B. Parallelklassen unterschiedlicher Ausrichtung).
- Fehlt eine Klassenstufen-Datei (z. B. Gymnasium Klasse 10/Einführungsphase), dies als Ebene 4 „noch zu prüfen" kennzeichnen statt zu improvisieren.

## Ausgabeformat
- Kopfzeile: Fach | Klasse | Schuljahr | Bildungsgang | Lehrplanbasis
- Zwei Blöcke (1. und 2. Halbjahr), je mit Tabelle: Reihen-Nr. | Thema | Zeitraum (grob, in Wochen oder Monaten) | Kompetenzschwerpunkt | Leistungsnachweis (falls in diesem Zeitraum)
- Nutzt `templates/jahresplanung.md` als Strukturvorlage.
- Eigener Abschnitt „Bildungsgang-Übergänge" bei Klasse 9/10, sonst entfällt er.
- Abschließend: Quellenverzeichnis, offene Punkte.

## Qualitätscheck
- Lehrplanbasis im Kopf ausgewiesen?
- Bildungsgang geklärt bzw. Annahme markiert, Übergang bei Klasse 9/10 thematisiert?
- Granularität auf Halbjahres-/Reihenebene eingehalten (keine Wochendetails, das ist Aufgabe des Stoffverteilungsplans)?
- Klassenarbeitstermine plausibel verteilt, nicht in Ferien?
- Quellen je Reihe genannt?
- Vier-Ebenen-Kennzeichnung vorhanden?
- Keine Schülernamen/Diagnosen, Datenschutz-Warnhinweis bei Bedarf?
- Nur Deutsch oder Ev. Religion abgedeckt?

## Beispielprompt
„Erstelle eine Jahresplanung für Evangelische Religion, Klasse 10, gymnasialer Bildungsgang, Schuljahr 2026/27. Bitte den Übergang aus Klasse 9 berücksichtigen."
