# Workflow: Arbeitsblatt

## Zweck
Erstellt ein einsatzfertiges Arbeitsblatt mit Aufgaben in mehreren Anforderungsstufen, passend zu Thema, Klasse und Kompetenzbezug. Liefert ein separates Lösungsblatt und Layout-Hinweise für den Druck.

## Eingaben
Pflicht:
- Thema
- Klassenstufe (5–12)
- Fach (Deutsch oder Evangelische Religion)

Optional (mit Annahme-Kennzeichnung bei Fehlen):
- Bildungsgang (bei Klasse 9–12 zu klären, siehe Bildungsgang-Prüfung)
- Einsatzkontext (Einzelstunde, Vertretungsstunde, Hausaufgabe, Übung innerhalb einer Reihe) — bei Fehlen Annahme „Übungsblatt innerhalb einer laufenden Reihe"
- Zeitrahmen für die Bearbeitung (bei Fehlen: Annahme „ca. 20–30 Minuten")
- Differenzierungsbedarf der Klasse (funktional, keine Diagnosen)
- Gewünschte Aufgabentypen (Lückentext, offene Fragen, Textanalyse, kreatives Schreiben etc.) — bei Fehlen: Auswahl passend zum Thema treffen und begründen

Bei unklarem Bildungsgang in Klasse 9/10: Rückfrage oder sichtbar markierte Annahme.

## Vorgehen
1. Bildungsgang klären/Annahme setzen (siehe Bildungsgang-Prüfung).
2. Passende Lehrplandatei laden, Kompetenzbezug für das Thema identifizieren.
3. Aufgabentypen festlegen, die den Kompetenzbezug abdecken (z. B. Textverständnis, Anwendung, Transfer).
4. Grundniveau der Aufgaben entwerfen (Anforderungsbereich I/II als Basis).
5. Mindestens zwei Differenzierungsstufen ergänzen: eine vereinfachte Variante (z. B. mit Hilfestellungen, reduzierter Textmenge) und eine erweiterte Variante (z. B. Transferaufgabe, offene Fragestellung) — als klar gekennzeichnete Zusatz- oder Wahlaufgaben, nicht als separates Parallelblatt, sofern nicht anders gewünscht.
6. Arbeitsanweisungen präzise und altersgerecht formulieren (Operatoren passend zur Klassenstufe wählen).
7. Layout strukturieren: Kopfzeile mit Name/Datum/Klasse-Feld (ohne echten Namen einzutragen), klare Nummerierung, ausreichend Platz für Antworten, sinnvolle Seitenumbrüche.
8. Lösungsblatt separat erstellen: vollständige Musterlösung bzw. Erwartungshorizont je Aufgabe, klar als eigener Abschnitt/eigene Datei gekennzeichnet.
9. Quellenbezug für Kompetenzbereich und ggf. verwendete Textgrundlagen dokumentieren (bei fremden Texten Autor/Quelle angeben, Urheberrecht beachten und ggf. darauf hinweisen).
10. Vier-Ebenen-Kennzeichnung anwenden, Qualitätscheck durchlaufen, Ausgabe erzeugen.

## Bildungsgang-Prüfung
- Klasse 5–8: Sekundarschule, keine Rückfrage.
- Klasse 9–10: klären. Sekundarschulabschluss/mittlerer Schulabschluss → Sekundarschule; gymnasialer Bildungsgang → Gymnasium, Klasse 10 = Einführungsphase (anspruchsvollere Aufgabenformate, stärkerer Textbezug).
- Klasse 11–12: nur Gymnasium, Qualifikationsphase/Abiturbezug — Aufgaben orientieren sich an Anforderungsbereich II/III, ggf. Abituraufgabenformat andeuten.
- Unklare Fälle nach `routing_rules.json` auflösen, Grenzfälle gegen `bildungsgang_guardrails.md` prüfen.
- Ausgabekopf trägt „Bildungsgang: <…>".

## Lehrplanbezug
- Herangezogen wird `data/curriculum/<fach>/<bildungsgang>/klasse_<nn>.md` der betreffenden Klassenstufe.
- Kopfzeile weist aus: Schulform, Bildungsgang, Lehrplanbasis (Sekundarschule/Gymnasium/kombiniert/unklar).
- Kompetenzbezug erhält Quellenangabe (Datei, Abschnitt/Fundstelle).
- Fehlt eine passende Lehrplandatei, Kompetenzbezug als Ebene 4 „noch zu prüfen" kennzeichnen.

## Ausgabeformat
- Kopfzeile Arbeitsblatt: Thema | Klasse | Bildungsgang | Lehrplanbasis | Fach | Kompetenzbezug
- Aufgabenteil: nummerierte Aufgaben, Differenzierungsstufen klar markiert (z. B. „Grundaufgabe", „Zusatzaufgabe *", „Vertiefung **")
- Layout-Hinweise als kurzer Abschnitt (Seitenumbruch, Schriftgröße-Empfehlung, Platzbedarf)
- Lösungsblatt als eigener, klar abgetrennter Abschnitt am Ende oder als separate Ausgabe, mit Hinweis „nur für Lehrkraft"
- Nutzt vorhandene Vorlagen aus `templates/`, sofern für Arbeitsblätter vorhanden; sonst orientiert sich die Ausgabe an dieser Workflow-Struktur.
- Abschließend: Quellenverzeichnis.

## Qualitätscheck
- Lehrplanbasis im Kopf ausgewiesen?
- Bildungsgang geklärt oder Annahme markiert?
- Mindestens zwei Differenzierungsstufen vorhanden und klar gekennzeichnet?
- Lösungsblatt separat und vollständig?
- Aufgabenoperatoren altersgerecht und eindeutig?
- Fremde Textquellen mit Urheberangabe, Urheberrechtshinweis falls nötig?
- Vier-Ebenen-Kennzeichnung konsequent angewendet?
- Keine echten Schülernamen im Kopf-/Namensfeld, kein Datenschutzverstoß?
- Nur Deutsch oder Ev. Religion abgedeckt?

## Beispielprompt
„Erstelle ein Arbeitsblatt zu Kurzgeschichten-Merkmalen für Deutsch, Klasse 8, Sekundarschule, mit Grund- und Zusatzaufgaben sowie separatem Lösungsblatt."
