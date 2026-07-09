# Workflow: Schülerfeedback zum Unterricht

## Zweck
Erstellt Feedbackbögen, mit denen Schüler:innen Rückmeldung zum Unterricht (nicht zu ihrer eigenen Note) geben — für Deutsch oder Ev. Religion, in verschiedenen Formaten (Ampel, offene Fragen, Skala), datenschutzkonform und anonymisierbar. Ziel ist Unterrichtsentwicklung, nicht Leistungsbewertung.

## Eingaben
Pflicht:
- Fach (Deutsch oder Ev. Religion) — kann auch fachübergreifend „allgemeiner Unterricht" sein
- Klassenstufe
- Anlass (z. B. nach Unterrichtsreihe, Halbjahresende, neue Methode ausprobiert, allgemeines Stimmungsbild)

Optional (mit Annahme bei Fehlen):
- Format (Ampel, offene Fragen, Skala 1–5, Kombination) — ohne Angabe: Kombination aus Skala und 1–2 offenen Fragen annehmen, kompakt gehalten
- Anonymität (anonym, mit Namen, freiwillig) — ohne Angabe: anonym annehmen, sichtbar markiert, als datenschutzfreundlichster Standard
- Fokus (Methodik, Tempo, Klassenklima, konkrete Unterrichtseinheit) — ohne Angabe: allgemeines Stimmungsbild zu Methodik und Verständlichkeit annehmen
- Digital oder Papierform — ohne Angabe: Papierform annehmen (voraussetzungsärmster Standard)

Feedback zu einzelnen Lehrkräften Dritter oder vergleichende Bewertung von Kolleg:innen: nicht Gegenstand dieses Workflows, Hinweis ausgeben.

## Vorgehen
1. Bildungsgang-Prüfung durchführen (siehe unten) — hier meist kurz, da Feedbackbögen selten bildungsgangspezifisch sind.
2. Anlass und Fokus klären: Was genau soll zurückgemeldet werden (Methode, Tempo, Klarheit, Klassenklima, Einzelstunde vs. Reihe).
3. Format wählen und altersgerecht gestalten: Kl. 5–6 eher Ampel/Symbole, Kl. 7–10 Skala plus offene Fragen, Kl. 11–12 differenziertere offene Fragen möglich.
4. Fragen formulieren: konkret, auf den Unterricht bezogen, nicht auf die Lehrkraft als Person, keine Suggestivfragen.
5. Anonymitätsstufe festlegen und im Bogen selbst kommunizieren (Schüler:innen wissen, wie die Angaben verwendet werden).
6. Auswertungshinweise für die Lehrkraft ergänzen: Wie werden Antworten gebündelt (z. B. Häufigkeiten bei Ampel, Kernaussagen bei offenen Fragen), wie wird ein Ergebnis in die Unterrichtsentwicklung zurückgespiegelt (z. B. kurze Rückmeldung an die Klasse „Das habe ich gehört, das ändere ich").
7. Datenschutz-Hinweis ergänzen: keine Zuordnung zu einzelnen Schüler:innen bei anonymer Erhebung, Aufbewahrung/Löschung der Bögen ansprechen.
8. Qualitätscheck durchführen, Ausgabe formatieren.

## Bildungsgang-Prüfung
Feedbackbögen zum Unterricht sind in der Regel bildungsgangunabhängig, da sie keine Lehrplaninhalte prüfen, sondern die Unterrichtsgestaltung betreffen.
- Klasse 5–8: keine Bildungsgangtrennung, Lehrplanbasis Sekundarschule nur als grober Rahmen relevant.
- Klasse 9–10: Bildungsgang für den Feedbackbogen selbst meist irrelevant; nur klären, falls das Feedback sich explizit auf bildungsgangspezifische Formate bezieht (z. B. Rückmeldung zur Projektarbeitsbetreuung).
- Klasse 11–12: nur Gymnasium — Feedbackbogen kann altersgerecht differenzierter formuliert werden.
- Bei diesem Workflow genügt in der Regel eine kurze, sichtbar markierte Einordnung statt zwingender Rückfrage; Details siehe `routing_rules.json` und `bildungsgang_guardrails.md`.

## Lehrplanbezug
Für diesen Workflow besteht kaum Lehrplanbezug: Feedback zum Unterricht ist ein didaktisch-organisatorisches Instrument der Unterrichtsentwicklung, kein fachlicher Lehrplaninhalt. `data/curriculum/`-Dateien werden nicht herangezogen. Im Ausgabekopf wird `Lehrplanbasis: nicht anwendbar (kein fachlicher Lehrplanbezug, Instrument der Unterrichtsentwicklung)` ausgewiesen, Schulform und Bildungsgang werden dennoch benannt, soweit für die Altersgerechtheit der Formulierung relevant.

## Ausgabeformat
Kopfzeile: `Schulform: Gemeinschaftsschule | Bildungsgang: <…> | Lehrplanbasis: nicht anwendbar`
Danach: Anlass, Klassenstufe, Fokus, Format, Anonymitätsstufe.
Abschnitt Feedbackbogen (je nach Format: Ampel-Tabelle, Skala-Fragen, offene Fragen — als druckfertige Vorlage).
Abschnitt Auswertungshinweise für die Lehrkraft.
Abschnitt Rückspiegelung an die Klasse (kurzer Hinweistext).
Abschnitt Datenschutz-Hinweis.
Kein dediziertes Feedback-Template unter `templates/` vorhanden — Layout an `templates/arbeitsblatt.md` orientieren, ohne Bewertungsspalten.

## Qualitätscheck
- Lehrplanbasis korrekt als „nicht anwendbar" gekennzeichnet, kein künstlicher Lehrplanbezug konstruiert?
- Fragen unterrichtsbezogen formuliert, nicht personenbezogen auf die Lehrkraft oder auf einzelne Schüler:innen?
- Format altersgerecht zur Klassenstufe?
- Anonymitätsstufe klar kommuniziert und im Bogen selbst sichtbar?
- Datenschutz-Hinweis vorhanden (Anonymität, Aufbewahrung/Löschung)?
- Keine Notenbezug-Vermischung (Feedback zum Unterricht, nicht zur Schülerleistung)?
- Keine echten Schülernamen in Beispielantworten, keine Diagnosen oder Schuldzuweisungen in Auswertungshinweisen?

## Beispielprompt
„Erstelle einen anonymen Feedbackbogen für Deutsch, Klasse 8, nach Abschluss der Unterrichtsreihe zu Kurzgeschichten, mit Ampel-Format und zwei offenen Fragen."
