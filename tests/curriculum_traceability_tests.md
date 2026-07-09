# Lehrplan-Rückverfolgbarkeits-Tests

Test: Jede Aussage, die einen Lehrplaninhalt behauptet, trägt eine Quellenangabe (Datei, Lehrplanbasis, Fach, Klasse, Abschnitt, Seite).
Erwartung: Fehlt eines dieser Elemente, wird die Aussage als "zu prüfen" (Ebene 4) markiert statt unbelegt präsentiert.

Test: Lehrplaninhalt und didaktische Ergänzung (z. B. Methodenvorschlag, Beispielaufgabe) stehen sichtbar getrennt.
Erwartung: Kennzeichnung erlaubt eindeutige Unterscheidung, welcher Teil Ebene 1 (Lehrplan) und welcher Ebene 2 (didaktisch) ist.

Test: Kompetenzformulierung wird wörtlich oder sinngemäß aus dem Lehrplan übernommen.
Erwartung: Quelle verweist auf konkrete Fundstelle (Fach/Klasse/Abschnitt/Seite), keine pauschale "laut Lehrplan"-Aussage ohne Fundstelle.

Test: Zwei Aussagen zu derselben Kompetenz stammen aus unterschiedlichen Lehrplanbasen (Sekundarschule vs. Gymnasium).
Erwartung: Beide Quellenangaben sind getrennt ausgewiesen und der Lehrplanbasis eindeutig zugeordnet, keine Vermischung.

Test: Ein Beispieloutput enthält eine didaktische Empfehlung ohne Lehrplanbezug (z. B. allgemeine Methodik).
Erwartung: Empfehlung ist als Ebene 2 gekennzeichnet, nicht fälschlich als Lehrplanvorgabe (Ebene 1) dargestellt.

Test: Quellenangabe verweist auf eine Datei, die im Skill-Repository nicht existiert.
Erwartung: Fehler wird erkannt/gemeldet, keine stillschweigende Übernahme einer nicht vorhandenen Quelle.

Test: Nutzer fragt "Woher stammt diese Kompetenz?" zu einer bereits ausgegebenen Aussage.
Erwartung: Antwort liefert exakte Fundstelle (Datei/Basis/Fach/Klasse/Abschnitt/Seite) oder markiert die Aussage nachträglich als unbelegt.

Test: Abiturbezogene Aussage in Klasse 12 wird geprüft.
Erwartung: Quelle stammt aus dem Gymnasium-Fachlehrplan (Qualifikationsphase), nicht aus einem Sekundarschul-Dokument.
