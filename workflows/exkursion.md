# Workflow: Exkursion / Unterrichtsgang

## Zweck
Plant einen Unterrichtsgang oder eine Exkursion für Deutsch oder Ev. Religion (z. B. Theaterbesuch, Autorenlesung, Kirchenbesuch, Gedenkstättenfahrt) mit Lernzielen, Zeitplan, organisatorischen Eckpunkten und Nachbereitung. Keine Rechtsberatung: Aufsichtspflicht, Genehmigungsverfahren und Kostenregelungen werden als Hinweise/Platzhalter behandelt, nicht als verbindliche Rechtsauskunft.

## Eingaben
Pflicht:
- Fach (Deutsch oder Ev. Religion)
- Klassenstufe
- Ziel/Ort der Exkursion (z. B. Theater, Kirche, Gedenkstätte, Bibliothek, Ausstellung)
- Bezug zur laufenden Unterrichtsreihe

Optional (mit Annahme bei Fehlen):
- Dauer (Unterrichtsstunde, Halbtag, Ganztag, mehrtägig) — ohne Angabe: Halbtagsexkursion annehmen, sichtbar markiert
- Anzahl Begleitpersonen — ohne Angabe: Hinweis ausgeben, dass Aufsichtsschlüssel nach schulinterner Regelung/Erlasslage zu klären ist, keine Zahl annehmen
- Kostenrahmen — ohne Angabe: Platzhalter „Kosten schulintern/mit Elternbeitrag klären" einsetzen
- Nachbereitungsformat (Reflexionsrunde, schriftliche Auswertung, Portfolio) — ohne Angabe: kurze schriftliche Reflexion als Standard annehmen

Fehlt das Exkursionsziel, RÜCKFRAGE stellen — ohne Ziel keine sinnvolle Lernzielformulierung möglich.

## Vorgehen
1. Bildungsgang-Prüfung durchführen (siehe unten) und Kopf-Kennzeichnung festlegen.
2. Bezug zur Unterrichtsreihe herstellen: Welche Lehrplaneinheit wird durch die Exkursion vertieft oder eingeleitet.
3. Lernziele formulieren (fachlich und ggf. überfachlich, z. B. Kulturteilhabe, Perspektivwechsel bei Religion).
4. Zeitplan erstellen: Anreise, Programm vor Ort, Rückreise, Pufferzeiten.
5. Organisatorische Eckpunkte als Checkliste ausgeben: Genehmigung durch Schulleitung (Hinweis, kein Formular), Information/Einverständnis der Erziehungsberechtigten, Aufsichtsschlüssel klären, Kostenrahmen/Elternbeitrag klären, Anfahrt/Transportmittel, Ansprechpartner vor Ort.
6. Sicherheitsaspekte benennen: Verhaltensregeln, Notfallkontakte, besondere Risiken je nach Zielort (z. B. Verkehr, Gedenkstätten-Sensibilität), Vorgehen bei Programmänderung.
7. Vorbereitung im Unterricht skizzieren: Was wird vor der Exkursion inhaltlich vermittelt, damit der Besuch anschlussfähig ist.
8. Nachbereitung planen: Reflexionsformat, Verknüpfung mit Bewertung/Kompetenznachweis, falls vorgesehen.
9. Quellenbezug (Lehrplanstelle) anfügen, sofern die Exkursion einer konkreten Lehrplaneinheit zugeordnet ist.
10. Qualitätscheck durchführen, Ausgabe formatieren.

## Bildungsgang-Prüfung
- Klasse 5–8: Lehrplanbasis Sekundarschule, Exkursionsformate meist niedrigschwellig (regionale Ziele).
- Klasse 9–10: Bildungsgang klären, sofern die Exkursion einer bildungsgangspezifischen Unterrichtsreihe zugeordnet ist (z. B. Vorbereitung auf Prüfungsthemen). Ohne klaren Prüfungsbezug ist die Exkursion oft bildungsgangübergreifend planbar — in diesem Fall genügt eine sichtbar markierte Annahme „Sekundarschule/kombiniert" statt zwingender Rückfrage.
- Klasse 11–12: nur Gymnasium, Qualifikationsphase; Exkursionen häufiger mit Abiturbezug (z. B. Pflichtlektüre-Inszenierung, Gedenkstättenfahrt im Rahmen eines Semesterthemas).
- Bei unklarem Bildungsgang in Kl. 9–10 mit erkennbarem Prüfungsbezug: Rückfrage stellen.
- Routing-Details siehe `routing_rules.json` und `bildungsgang_guardrails.md`.

## Lehrplanbezug
Herangezogen werden `data/curriculum/deutsch/` bzw. `data/curriculum/religion/`, Unterordner nach Bildungsgang, für die passende Klassenstufe — nur soweit die Exkursion einer konkreten Unterrichtseinheit zugeordnet wird. Bei rein kulturell-ergänzenden Exkursionen ohne engen Lehrplanbezug (z. B. allgemeiner Museumsbesuch) ist der Lehrplanbezug schwach; dies explizit im Ausgabekopf als „Lehrplanbasis: unklar" oder mit Hinweis „lose Anbindung, kein direkter Lehrplanabschnitt" vermerken statt einen künstlichen Bezug zu konstruieren.

## Ausgabeformat
Kopfzeile: `Schulform: Gemeinschaftsschule | Bildungsgang: <…> | Lehrplanbasis: <…>`
Danach: Ziel, Klassenstufe, Dauer, Bezug zur Unterrichtsreihe.
Abschnitt Lernziele.
Abschnitt Zeitplan (Tabelle: Uhrzeit | Programmpunkt | Hinweis).
Abschnitt Organisatorisches (Checkliste, mit Platzhaltern für Genehmigung/Kosten).
Abschnitt Sicherheitsaspekte.
Abschnitt Vorbereitung im Unterricht.
Abschnitt Nachbereitung.
Abschnitt Quellenbezug (falls vorhanden).
Kein dediziertes Exkursions-Template unter `templates/` vorhanden — Zeitplan-Tabelle an `templates/stundenentwurf.md`, Lernziel-Formulierung an `templates/unterrichtsreihe.md` orientieren.

## Qualitätscheck
- Lehrplanbasis im Kopf ausgewiesen bzw. „unklar/lose Anbindung" korrekt vermerkt?
- Bildungsgang-Klärung bei Kl. 9–10 mit Prüfungsbezug dokumentiert?
- Organisatorische Punkte als Hinweise/Platzhalter gekennzeichnet, keine Rechtsberatung suggeriert (z. B. Aufsichtsschlüssel nicht als feste Zahl behauptet)?
- Vier-Ebenen-Kennzeichnung bei Lernzielen angewandt?
- Sicherheitsaspekte konkret und zielortspezifisch, nicht floskelhaft?
- Quellen genannt, soweit Lehrplanbezug besteht?
- Keine echten Schülernamen, keine personenbezogenen Gesundheitsangaben (z. B. bei Hinweisen zu Begleitbedarf neutral formulieren)?

## Beispielprompt
„Plane einen Unterrichtsgang für Ev. Religion, Klasse 7, zu einer örtlichen Kirche im Rahmen der Unterrichtsreihe zu Kirchenraum und Symbolik, Halbtagsexkursion mit Nachbereitung."
