# Workflow: Gesprächsprotokoll

## Zweck
Erstellt ein sachliches, rechtssicheres Protokoll für Elterngespräche, Beratungsgespräche oder Klassenkonferenzen. Dokumentiert Fakten und Vereinbarungen, keine Bewertungen der beteiligten Personen.

## Eingaben
Pflicht:
- Anlass des Gesprächs (Stichwort reicht, z. B. "Beratungsgespräch Leistungsabfall", "Klassenkonferenz Verhalten")
- Datum (oder Platzhalter, falls unbekannt)
- Teilnehmende, möglichst über Rollen benannt (Klassenlehrkraft, Fachlehrkraft X, Erziehungsberechtigte/r, Schulleitung, Beratungslehrkraft) — Klarnamen nur wenn vom User explizit so übergeben, sonst Rolle+Kürzel

Optional:
- Vorab bekannte Gesprächspunkte/Tagesordnung
- Bereits getroffene Vereinbarungen oder Vorschläge
- Wiedervorlagetermin
- Ob das Protokoll gegengezeichnet werden soll

Fehlen Teilnehmerangaben, wird mit generischen Rollenbezeichnungen ("Klassenlehrkraft", "Erziehungsberechtigte/r") gearbeitet und das als Annahme markiert.

**Datenschutz-Pflicht — prominent:** Dieses Protokoll betrifft in aller Regel personenbezogene, teils sensible Daten. Vor der Ausgabe wird ein sichtbarer Warnhinweis vorangestellt: Protokoll enthält personenbezogene Daten, vertraulich behandeln, nur berechtigten Personen zugänglich machen, Aufbewahrung nach schulrechtlichen Vorgaben prüfen. Keine medizinischen, psychologischen oder rechtlichen Diagnosen im Protokoll — nur beobachtbares Verhalten und vereinbarte Maßnahmen. Keine Bewertung des Charakters der Person, nur Fakten und Vereinbarungen.

## Vorgehen
1. Anlass und Gesprächsart klassifizieren (Elterngespräch / Beratungsgespräch / Klassenkonferenz) — Struktur leicht anpassen (Klassenkonferenz braucht Abstimmungsergebnis, Elterngespräch nicht).
2. Teilnehmende mit Rolle auflisten, Datenschutz-Hinweis voranstellen.
3. Gesprächspunkte chronologisch oder thematisch ordnen, so wie vom User geschildert — keine Punkte erfinden.
4. Aussagen strikt sachlich formulieren: Beobachtung statt Interpretation ("S. hat in den letzten vier Wochen dreimal Hausaufgaben nicht vorgelegt" statt "S. ist unmotiviert").
5. Vereinbarungen klar und überprüfbar formulieren: wer macht was bis wann.
6. Wiedervorlagetermin festhalten oder als offen kennzeichnen.
7. Protokoll auf wertende Formulierungen und Diagnosebegriffe prüfen, ggf. neutralisieren.
8. Qualitätscheck durchführen.

## Bildungsgang-Prüfung
Relevant, wenn das Gespräch eine Bildungsgangentscheidung betrifft (z. B. Beratungsgespräch zur Schullaufbahn in Klasse 9/10, Übergang in die gymnasiale Einführungsphase). In diesem Fall den besprochenen/vereinbarten Bildungsgang exakt und neutral protokollieren, keine Wertung ("besser"/"schwächer") — laut `routing_rules.json` sind Sekundarschulabschluss und gymnasialer Bildungsgang gleichrangige Wege. Für Klasse 11–12 ist nur der gymnasiale Bildungsgang (Qualifikationsphase) einschlägig, das entsprechend benennen, falls das Gespräch Kurswahl/Abitur betrifft.

## Lehrplanbezug
In der Regel kein Lehrplanbezug, da es sich um ein organisatorisch-pädagogisches Dokument handelt. `data/curriculum/`-Dateien werden nur herangezogen, wenn im Gespräch konkrete Lehrplaninhalte thematisiert wurden (z. B. "Leistungsstand bezogen auf Kompetenzbereich X"); dann genügt eine knappe Nennung im Protokolltext, keine formale Quellenangabe und keine Vier-Ebenen-Kennzeichnung, da das Protokoll den Gesprächsverlauf dokumentiert und keine fachdidaktische Aussage trifft.

## Ausgabeformat
Kein dediziertes Template in `templates/` vorhanden — Ausgabe als strukturiertes Protokoll:

1. Datenschutz-Warnhinweis (fett/hervorgehoben, ganz oben).
2. Kopf: Anlass, Datum, Uhrzeit/Dauer (falls bekannt), Ort, Teilnehmende (Rolle).
3. Tagesordnung/Gesprächspunkte als nummerierte Liste.
4. Verlauf: pro Punkt kurzer sachlicher Absatz (Beobachtung/Sachstand, keine Wertung).
5. Vereinbarungen als Tabelle: Maßnahme | Verantwortlich (Rolle) | Frist
6. Wiedervorlage: Datum oder "offen".
7. Unterschriftenzeile (Platzhalter), falls Gegenzeichnung gewünscht.

## Qualitätscheck
- Datenschutz-Warnhinweis vorhanden und an prominenter Stelle
- Nur Rollen/Kürzel, keine unnötigen Klarnamen
- Keine Diagnosebegriffe, keine Bewertung der Person
- Ausschließlich Beobachtungen und Fakten, keine Mutmaßungen
- Vereinbarungen konkret, mit Verantwortlichkeit und Frist
- Wiedervorlage klar benannt oder explizit als offen markiert
- Bildungsgang neutral und korrekt protokolliert, falls einschlägig
- Kein Lehrplanbezug-Fall korrekt vermerkt, falls zutreffend

## Beispielprompt
"Protokolliere ein Beratungsgespräch mit den Eltern von S. (7c) vom 09.07., Thema: gehäufte fehlende Hausaufgaben in Deutsch, Teilnehmer: Klassenlehrkraft und Erziehungsberechtigte. Vereinbart wurde ein Hausaufgabenheft mit Elternunterschrift, Wiedervorlage in vier Wochen."
