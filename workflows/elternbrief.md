# Workflow: Elternbrief

## Zweck
Erstellt einen versandfertigen Elternbrief zu einem konkreten Anlass (z. B. Klassenfahrt, Elternabend-Einladung, Leistungsstand, Verhaltensauffälligkeit, organisatorische Mitteilung). Sachlicher Ton, klare Handlungsaufforderung, korrekte Fristen, Datenschutz gewahrt.

## Eingaben
Pflicht:
- Anlass des Briefs (Stichwort oder Kurzbeschreibung reicht)
- Klasse
- Adressatenkreis: gesamte Klasse oder einzelne Erziehungsberechtigte

Optional:
- Datum/Frist, bis wann reagiert werden soll
- Konkrete Handlungsaufforderung (Unterschrift, Rückmeldung, Geld, Material mitbringen)
- Kontaktmöglichkeit (Sprechzeit, Mail, Telefon) — falls fehlend: Platzhalter "[Kontaktmöglichkeit ergänzen]" setzen
- Tonvariante (siehe Vorgehen Schritt 2)
- Absenderangaben (Name, Funktion, Schule)

Fehlt die Frist bei einem fristgebundenen Anlass, wird das als "noch zu prüfen" (Ebene 4) markiert und ein Platzhalter gesetzt statt eine Frist zu erfinden.

**Datenschutz-Pflicht:** Bei Briefen zu einzelnen Schülern (z. B. Verhaltens- oder Leistungsanlass) wird das Kind im Brief direkt angesprochen ("Ihr Sohn/Ihre Tochter") oder mit Vornamen der Familie — keine Klassenlisten, keine Vergleiche mit anderen Kindern, keine Diagnosen. Warnhinweis ausgeben, wenn sensible personenbezogene Angaben (Gesundheit, Diagnosen, familiäre Situation) im Anlass mitgegeben wurden.

## Vorgehen
1. Anlass klassifizieren: organisatorisch / pädagogisch-neutral / sensibel (Verhalten, Leistung, Konflikt).
2. Tonvariante festlegen — entweder vom User vorgegeben oder aus dem Anlass abgeleitet, sichtbar benennen:
   - neutral (Standard für organisatorische Mitteilungen)
   - freundlich (Einladungen, positive Anlässe)
   - dringlich (Fristen, wichtige Rückmeldungen, unentschuldigte Fehltage)
   - kurz (reine Information ohne Handlungsbedarf)
   - ausführlich (komplexe Sachverhalte, z. B. Klassenfahrt mit vielen Details)
   - leichte Sprache (bei Bedarf für Familien mit Sprachbarriere — kurze Sätze, keine Fachbegriffe, aktiv statt passiv)
3. Struktur aufbauen: Anrede → Anlass in 1–2 Sätzen → Kernaussage/Handlungsaufforderung → Frist → Kontaktmöglichkeit → Grußformel.
4. Sensible Anlässe: Formulierungen auf Neutralität prüfen, keine Schuldzuweisung, Lösungsorientierung statt Problemfokus.
5. Fristen und Daten aus den Eingaben übernehmen; keine erfundenen Termine.
6. Brief vollständig ausformulieren (kein Stichwortgerüst).
7. Qualitätscheck durchführen.

## Bildungsgang-Prüfung
Für Elternbriefe im Regelfall irrelevant, da organisatorisch/administrativ und nicht lehrplangebunden. Ausnahme: Briefe mit Bezug auf Bildungsgangentscheidungen (z. B. Wechsel Sekundarschulabschluss ↔ gymnasialer Bildungsgang in Klasse 9/10, Übergang in die Einführungsphase). In diesen Fällen: Bildungsgang laut `routing_rules.json` klären bzw. beim User erfragen, da die Formulierung ("Ihr Kind wechselt in den gymnasialen Bildungsgang / bleibt im Sekundarschulabschluss-Bildungsgang") fachlich korrekt sein muss. Bei Unklarheit lieber neutral formulieren ("die Bildungsgang-Entscheidung für Ihr Kind steht an") und Rückfrage stellen, statt eine falsche Schulform zu benennen.

## Lehrplanbezug
In der Regel kein Lehrplanbezug. `data/curriculum/`-Dateien werden nur herangezogen, wenn der Brief inhaltlich auf ein Lehrplanthema verweist (z. B. "im Rahmen der Unterrichtsreihe zu Thema X"). In diesem Fall genügt ein knapper, unbequellter Hinweis im Fließtext — keine formale Quellenangabe und keine Vier-Ebenen-Kennzeichnung, da ein Elternbrief kein fachdidaktisches Arbeitsmittel ist.

## Ausgabeformat
Kein dediziertes Template in `templates/` vorhanden — Ausgabe als fertiger Brieftext:

1. Kopf (nicht Teil des Briefs, nur Meta-Info für die Lehrkraft): Anlass, Klasse, Tonvariante, ggf. Bildungsgang-Hinweis.
2. Vollständiger Brieftext:
   - Betreffzeile
   - Anrede
   - Fließtext (Anlass, Kernaussage, ggf. Handlungsaufforderung mit Frist)
   - Kontaktmöglichkeit
   - Grußformel + Platzhalter für Namen/Funktion
3. Bei "leichte Sprache": zusätzlich kurzer Hinweis, dass Sätze bewusst vereinfacht wurden.

## Qualitätscheck
- Anlass klar und in 1–2 Sätzen erkennbar
- Handlungsaufforderung eindeutig (was, bis wann, wie)
- Frist nur übernommen, nicht erfunden — sonst Platzhalter gesetzt
- Kontaktmöglichkeit vorhanden oder als Platzhalter markiert
- Ton konsistent mit gewählter Variante durchgehalten
- Bei sensiblen Anlässen: keine Schuldzuweisung, keine Diagnosebegriffe, keine Vergleiche mit anderen Kindern
- Datenschutz-Warnhinweis ausgegeben, falls sensible Angaben übergeben wurden
- Bildungsgang korrekt benannt oder bewusst neutral gehalten (bei Klasse 9/10-Bezug)
- Kein Lehrplanbezug-Fall korrekt vermerkt, falls zutreffend

## Beispielprompt
"Schreib einen Elternbrief an die 6a: Die Klassenfahrt nach Wernigerode findet vom 14.–16.10. statt, Anzahlung von 50 Euro bis zum 20.08. fällig, Rückmeldung per Unterschrift auf dem beiliegenden Zettel. Ton: freundlich."
