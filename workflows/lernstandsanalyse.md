# Workflow: Lernstandsanalyse

## Zweck
Erstellt eine kompetenzorientierte Lernstandserhebung für Deutsch oder Ev. Religion — Beobachtungskriterien, Aufgabenformate zur Standortbestimmung und Auswertungshinweise, aus denen Fördermaßnahmen abgeleitet werden können (Verweis auf `foerderplan.md`). Ausdrücklich KEINE medizinische, psychologische oder sonderpädagogisch-diagnostische Einordnung — reine fachliche/didaktische Standortbestimmung.

## Eingaben
Pflicht:
- Fach (Deutsch oder Ev. Religion)
- Klassenstufe
- Kompetenzbereich, der erhoben werden soll (z. B. Leseverstehen, Textproduktion, Argumentieren/Urteilen in Religion)
- Anlass (Schuljahresbeginn, nach Unterrichtseinheit, Verdacht auf Förderbedarf, Übergang)

Optional (mit Annahme bei Fehlen):
- Erhebungsform (schriftlich, mündlich, Beobachtung im Unterricht) — ohne Angabe: schriftliche Aufgabe plus ergänzende Beobachtungscheckliste annehmen
- Gruppengröße (Einzelperson, Kleingruppe, ganze Klasse) — ohne Angabe: ganze Klasse annehmen, mit Hinweis auf Einzelauswertung
- Vorwissen/bisherige Auffälligkeiten — ohne Angabe: keine Vorannahme treffen, Erhebung ergebnisoffen gestalten

Bei Hinweisen auf möglichen sonderpädagogischen Förderbedarf: RÜCKFRAGE oder deutlicher Hinweis, dass eine förmliche Diagnostik nicht Teil dieses Workflows ist und ggf. Fachkräfte (Förderschullehrkraft, Schulpsychologie) einzubeziehen sind.

## Vorgehen
1. Bildungsgang-Prüfung durchführen (siehe unten) und Kopf-Kennzeichnung festlegen.
2. Kompetenzbereich mit Lehrplan abgleichen: erwartetes Kompetenzniveau der Klassenstufe identifizieren.
3. Beobachtungskriterien formulieren — konkret, verhaltensbezogen, wertfrei (z. B. „erkennt Hauptaussage eines Textes" statt „versteht schlecht").
4. Aufgabenformat zur Standortbestimmung auswählen (kurze diagnostische Aufgabe, kein Notendruck, klar abgegrenzter Umfang).
5. Auswertungsraster erstellen: Kompetenzstufen (z. B. „sicher / grundlegend / im Aufbau") statt Notenskala.
6. Aussagen konsequent funktional/beobachtungsbasiert formulieren, keine Diagnosen, keine Ursachenzuschreibung (z. B. nicht „hat Konzentrationsstörung", sondern „zeigt in Aufgabe X wiederholt Schwierigkeiten bei Y").
7. Ableitung von Fördermaßnahmen skizzieren: konkrete nächste Schritte benennen, für die Detailplanung auf `templates/foerderplan.md` verweisen.
8. Datenschutz-Hinweis prominent einfügen (siehe Qualitätscheck).
9. Quellenbezug (Lehrplanstelle für erwartetes Kompetenzniveau) anfügen.
10. Qualitätscheck durchführen, Ausgabe formatieren.

## Bildungsgang-Prüfung
- Klasse 5–8: Lehrplanbasis Sekundarschule, Kompetenzerwartungen daraus ableiten.
- Klasse 9–10: Bildungsgang klären, da erwartetes Kompetenzniveau je nach Bildungsgang unterschiedlich ist (Sekundarschulabschluss vs. gymnasialer Bildungsgang). Ohne Angabe: Annahme Sekundarschule, sichtbar markiert.
- Klasse 11–12: nur Gymnasium, Qualifikationsphase — Lernstandsanalyse hier seltener, meist im Kontext von Kurswahl oder Aufholbedarf vor Klausuren.
- Bei unklarem Bildungsgang: Rückfrage ODER sichtbar markierte Annahme.
- Routing-Details siehe `routing_rules.json` und `bildungsgang_guardrails.md`.

## Lehrplanbezug
Herangezogen werden `data/curriculum/deutsch/` bzw. `data/curriculum/religion/`, Unterordner nach Bildungsgang, für die passende Klassenstufe — zur Bestimmung des erwarteten Kompetenzniveaus als Bezugspunkt der Erhebung. Die konkrete Auswertung einzelner Schülerergebnisse ist kein Lehrplaninhalt und wird als didaktische Ergänzung (Ebene 2) bzw. Annahme (Ebene 3) gekennzeichnet, nicht als direkter Lehrplanbezug.

## Ausgabeformat
Kopfzeile: `Schulform: Gemeinschaftsschule | Bildungsgang: <…> | Lehrplanbasis: <…>`
Danach: Kompetenzbereich, Klassenstufe, Anlass, Erhebungsform.
Abschnitt Beobachtungskriterien (Liste, wertfrei formuliert).
Abschnitt Aufgabe(n) zur Standortbestimmung.
Abschnitt Auswertungsraster (Tabelle: Kompetenzstufe | Beschreibung | Indikatoren).
Abschnitt Ableitung Fördermaßnahmen (Kurzfassung, Verweis auf `templates/foerderplan.md`).
Abschnitt Datenschutz-Hinweis (eigener, deutlich abgesetzter Absatz).
Abschnitt Quellenbezug.
Für die Detailplanung von Fördermaßnahmen wird `templates/foerderplan.md` genutzt; die Lernstandsanalyse selbst hat kein eigenes Template und orientiert sich strukturell an `templates/bewertungsraster.md` für das Auswertungsraster.

## Qualitätscheck
- Lehrplanbasis im Kopf ausgewiesen, Bildungsgang bei Kl. 9–10 geklärt?
- Alle Beobachtungsformulierungen funktional/beobachtungsbasiert, keine medizinischen/psychologischen Begriffe (z. B. keine Diagnosen wie „ADHS", „Legasthenie" ohne fachärztliche/förderschulpädagogische Grundlage)?
- Keine Schuldzuweisungen, keine Ursachenspekulation?
- Vier-Ebenen-Kennzeichnung angewandt, insbesondere Auswertung als Ebene 2/3 markiert?
- Datenschutz-Hinweis vorhanden und prominent platziert?
- Nur Kürzel/Pseudonyme statt echter Schülernamen in Beispielen?
- Quellen (Lehrplandatei, Fach, Klasse, Abschnitt) für Kompetenzniveau genannt?
- Verweis auf `foerderplan.md` vorhanden, falls Fördermaßnahmen abgeleitet werden?

## Beispielprompt
„Erstelle eine Lernstandsanalyse für Deutsch, Klasse 6, Kompetenzbereich Leseverstehen, zu Schuljahresbeginn, mit Beobachtungskriterien und Auswertungsraster."
