# Workflow: Förderplan

## Zweck
Erstellt einen schulischen Förderplan auf Basis beobachtbaren Verhaltens (nicht auf Basis von Diagnosen): Beobachtung, Förderziel, Maßnahme, Zeitraum, Verantwortliche, benötigtes Material, Überprüfungsart und nächster Termin. Der Plan dient der internen schulischen Dokumentation und Abstimmung, nicht der medizinischen oder psychologischen Einordnung.

## Eingaben
Pflicht:
- Beobachtete Ausgangslage (funktional, verhaltensbezogen, z. B. „Schüler/in X hat Schwierigkeiten, mehrschrittige Leseaufträge selbstständig zu strukturieren")
- Fach/Bereich, für den der Förderplan gilt
- Klassenstufe

Optional (mit Annahme bei Fehlen):
- Zeitraum — ohne Angabe: Standardzeitraum 6–8 Wochen bis zur ersten Überprüfung annehmen und kennzeichnen
- Verantwortliche Person(en) — ohne Angabe: „Fachlehrkraft" als Platzhalter setzen, sichtbar als zu ergänzen markieren
- Vorhandene Diagnosen/Gutachten — werden NICHT abgefragt und NICHT verarbeitet, siehe Datenschutz-Hinweis unten

Fehlt die Ausgangslage komplett oder ist sie erkennbar diagnostisch formuliert (z. B. „hat ADHS", „ist lese-rechtschreib-gestört" ohne amtliche Feststellung im Kontext schulischer Zuständigkeit), RÜCKFRAGE stellen bzw. Umformulierung in beobachtbares Verhalten vorschlagen.

## Vorgehen
1. Eingangsbeschreibung auf diagnostische Formulierungen prüfen; ggf. in beobachtbares, funktionales Verhalten umformulieren (siehe Datenschutz-Regel).
2. Schülerbezeichnung auf Kürzel/Pseudonym prüfen; bei echtem Namen Warnhinweis ausgeben und Pseudonymisierung vorschlagen.
3. Beobachtung konkretisieren: Was genau, in welchem Kontext, wie oft beobachtet?
4. Realistisches, überprüfbares Förderziel formulieren (SMART-Logik: spezifisch, messbar, angemessen, realistisch, terminiert).
5. Konkrete schulische Maßnahme(n) ableiten (methodisch-didaktisch, keine therapeutischen Maßnahmen).
6. Zeitraum und Verantwortliche festlegen.
7. Benötigtes Material benennen (Arbeitsblätter, Strukturierungshilfen, Zeitpläne o. ä.).
8. Überprüfungsart festlegen (wie wird der Zielfortschritt erfasst — Beobachtung, Kurztest, Selbsteinschätzung).
9. Nächsten Termin/nächste Überprüfung terminieren.
10. Datenschutz- und Kennzeichnungscheck durchführen, Ausgabe formatieren.

## Bildungsgang-Prüfung
Förderpläne sind grundsätzlich bildungsgangunabhängig anwendbar (Klasse 5–12), da sie sich auf schulisches Verhalten und Lernprozess beziehen, nicht auf Lehrplaninhalte im engeren Sinn. Dennoch zu klären:
- Klassenstufe angeben, um Maßnahmen altersangemessen zu formulieren.
- Bei Klasse 9–12 ggf. Bildungsgang nennen, falls die Maßnahme an einen bestimmten Lehrplaninhalt anknüpft (z. B. Abiturvorbereitung vs. Abschlussprüfung Sekundarschule) — sonst nicht zwingend erforderlich.
- Kein Zwang zur strikten Lehrplanbasis-Kennzeichnung im Kopf, da Förderpläne primär pädagogisch-organisatorisch sind; bei fachbezogenen Zielen dennoch Lehrplanbasis ausweisen. Siehe `routing_rules.json` und `bildungsgang_guardrails.md` für Grenzfälle.

## Lehrplanbezug
Nur wenn das Förderziel an einen konkreten Lehrplaninhalt anknüpft (z. B. „sicherer Umgang mit Nebensatzkonstruktionen"), wird `data/curriculum/<fach>/<bildungsgang>/klasse_XX.md` herangezogen und die betroffene Kompetenz benannt. Rein verhaltens- oder arbeitsorganisationsbezogene Ziele (z. B. Aufgabenstrukturierung, Zeitmanagement) benötigen keinen Lehrplanbezug — das wird in der Ausgabe kenntlich gemacht.

## Ausgabeformat
Tabelle: Beobachtung | Ziel | Maßnahme | Zeitraum | Verantwortliche | Material | Überprüfung | nächster Termin.
Kopfzeile nur bei Lehrplanbezug: `Schulform: Gemeinschaftsschule | Bildungsgang: <…> | Lehrplanbasis: <…>` — sonst entfällt der Lehrplanbasis-Hinweis, stattdessen Vermerk „kein direkter Lehrplanbezug, verhaltens-/organisationsbezogenes Ziel".
Abschnitt „Datenschutz-Hinweis" (Pseudonymisierung, keine Diagnosen).
Kein eigenes Template unter `templates/` — Tabellenstruktur an `templates/stoffverteilungsplan.md` anlehnen.

## Qualitätscheck
- Schülerbezeichnung als Kürzel/Pseudonym, kein echter Name?
- Beobachtung funktional/verhaltensbasiert formuliert, keine medizinische/psychologische/rechtliche Diagnose?
- Keine Schuldzuweisung (weder an Schüler noch an Elternhaus)?
- Ziel SMART formuliert und schulisch (nicht therapeutisch) umsetzbar?
- Bei Lehrplanbezug: Lehrplanbasis ausgewiesen, Quelle genannt?
- Vier-Ebenen-Kennzeichnung bei Annahmen (z. B. Standardzeitraum) gesetzt?
- Datenschutz-Warnhinweis ausgegeben, falls Eingabe personenbezogene oder diagnostische Formulierungen enthielt?

## Beispielprompt
„Erstelle einen Förderplan für Schüler/in M.K., Klasse 6, der/die Schwierigkeiten hat, sich beim selbstständigen Lesen längerer Texte zu konzentrieren."
