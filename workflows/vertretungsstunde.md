# Workflow: Vertretungsstunde

## Zweck
Erstellt sofort einsetzbares, materialarmes Vertretungsmaterial für eine kurzfristig zu übernehmende Stunde — durchführbar ohne Fachkenntnis oder Vorwissen der Vertretungslehrkraft.

## Eingaben
Pflicht:
- Klasse
- Dauer der Stunde (Standardannahme: 45 Minuten, falls nicht angegeben)

Optional:
- Fach (falls Vertretung fachgebunden sein soll, sonst fachfrei)
- Bezug zur laufenden Unterrichtsreihe (Stoffverteilungsplan/Thema) — nur nutzen, wenn ausdrücklich gewünscht
- Verfügbare Materialien im Raum (Tafel, Beamer, Kopierer erreichbar oder nicht)
- Anzahl Schüler
- Ob die Vertretungslehrkraft fachfremd ist (Standardannahme: ja, sicherheitshalber)

Fehlt die Angabe zum Fachbezug, wird ein fachfreies Material erstellt — das ist der sicherere Default für Sofort-Einsatz. Fehlt die Materiallage, wird von "nur Tafel, kein Kopierer kurzfristig verfügbar" ausgegangen.

## Vorgehen
1. Sofort-Verfügbarkeit vor Fachtiefe priorisieren: Material muss ohne Vorbereitungszeit der Vertretungslehrkraft einsetzbar sein.
2. Entscheiden: mit Fachbezug (nur wenn Fach + Thema klar angegeben) oder ohne Fachbezug (Standard).
3. Aufgabenformat wählen, das keine Fachexpertise der aufsichtführenden Person voraussetzt: Selbstlernaufgaben mit Lösung, Rätsel/Logikaufgaben, Lesetext mit Fragen, Stillarbeitsblatt mit Selbstkontrolle.
4. Klare, in sich verständliche Arbeitsanweisung formulieren (Schüler müssen ohne Erklärung der Vertretungslehrkraft starten können).
5. Zeitpuffer einplanen: Hauptaufgabe für ca. 70 % der Zeit, Zusatzaufgabe für schnelle Schüler, Cooldown/Aufräumen für die letzten 5 Minuten.
6. Lösungen/Erwartungshorizont beilegen, damit die Vertretungslehrkraft ohne Fachwissen kontrollieren kann.
7. Kurzer Hinweiszettel "für die Vertretungslehrkraft" mit Ablauf in 3–5 Stichpunkten.
8. Qualitätscheck durchführen.

## Bildungsgang-Prüfung
Nur relevant, wenn die Vertretungsstunde fachlich an eine laufende Unterrichtsreihe anknüpft und die Klasse in Klasse 9/10 nach Bildungsgang differenziert unterrichtet wird (z. B. E-/G-Kurs). In diesem Fall den Kurs/Bildungsgang laut `routing_rules.json` benennen, damit das Material zum richtigen Niveau passt. Für fachfreie Vertretungsstunden (Standardfall) ist der Bildungsgang irrelevant — Material funktioniert klassen- und niveauunabhängig. Klasse 11–12: nur Gymnasium/Qualifikationsphase, bei Fachbezug entsprechend kennzeichnen.

## Lehrplanbezug
Im Regelfall kein Lehrplanbezug, da fachfreies Material bevorzugt wird. Bei explizitem Fachbezug werden die passenden Dateien aus `data/curriculum/deutsch/` bzw. `data/curriculum/religion/` für Klasse und Thema herangezogen, mit Kopfzeile (Schulform, Bildungsgang, Lehrplanbasis) und Quellenangabe (Datei, Fach, Klasse, Abschnitt) wie bei regulärem Unterrichtsmaterial. Ohne expliziten Fachbezug wird dieser Abschnitt in der Ausgabe kurz mit "kein Lehrplanbezug — fachfreies Vertretungsmaterial" vermerkt.

## Ausgabeformat
Kein dediziertes Template in `templates/` vorhanden — Ausgabe als sofort druckfertiges Material:

1. Hinweiszettel für die Vertretungslehrkraft (oben, kurz): Klasse, Dauer, Ablauf in Stichpunkten, was bei Problemen zu tun ist (z. B. "bei Fragen: Nachbarklasse/Sekretariat").
2. Arbeitsblatt/Aufgabentext für Schüler, in sich vollständig verständlich.
3. Zusatzaufgabe für schnelle Schüler.
4. Lösungsblatt/Erwartungshorizont, getrennt vom Schülerteil.
5. Bei Fachbezug zusätzlich: Kopfzeile mit Schulform/Bildungsgang/Lehrplanbasis und Quellenangabe.

## Qualitätscheck
- Material ohne Vorbereitungszeit der Vertretungslehrkraft einsetzbar
- Arbeitsanweisung für Schüler eigenständig verständlich
- Zeitpuffer und Zusatzaufgabe vorhanden
- Lösung/Erwartungshorizont beigefügt
- Kein Vorwissen der Vertretungslehrkraft vorausgesetzt (auch nicht fachfremd)
- Bei Fachbezug: Lehrplanbasis ausgewiesen, Quelle genannt, Vier-Ebenen-Kennzeichnung verwendet
- Ohne Fachbezug: "kein Lehrplanbezug"-Vermerk vorhanden
- Datenschutz: keine echten Schülernamen im Material, keine personenbezogenen Beispiele

## Beispielprompt
"Brauche sofort eine Vertretungsstunde für die 8a, 45 Minuten, fachfrei, kein Kopierer verfügbar, nur Tafel."
