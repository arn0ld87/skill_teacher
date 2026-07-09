# Workflow: Erwartungshorizont

## Zweck
Erstellt zu einer gegebenen Aufgabe (Klassenarbeit, Klausur, Test) einen detaillierten Erwartungshorizont: erwartete Schülerleistung, Teilpunkte, Anforderungsbereichszuordnung, typische Fehler, Bewertungshinweise und Feedbackbausteine für die Korrektur.

## Eingaben
Pflicht:
- Die konkrete Aufgabenstellung (Text oder Verweis auf vorhandene Aufgabe aus `klausur.md`/`klassenarbeit.md`-Workflow)
- Fach und Klassenstufe
- Gesamtpunktzahl der Aufgabe

Optional (mit Annahme bei Fehlen):
- Bildungsgang — ohne Angabe: aus Klassenstufe ableiten (siehe Bildungsgang-Prüfung), bei Ambiguität Annahme kennzeichnen
- Musterlösung/Kernaussagen des Fachs — ohne Angabe: aus Lehrplan und Fachdidaktik plausibel entwickeln, als „didaktisch ergänzt" (Ebene 2) kennzeichnen
- Gewichtung von Inhalt vs. Sprache/Darstellung — ohne Angabe: fachübliche Standardgewichtung annehmen (Deutsch häufig 2/3 Inhalt–1/3 Darstellung, kenntlich machen)

## Vorgehen
1. Aufgabenstellung analysieren, in Teilaufgaben/Teilleistungen zerlegen.
2. Jeder Teilleistung einen Anforderungsbereich (AFB I/II/III) zuordnen.
3. Erwartete inhaltliche Kernpunkte formulieren (Stichpunkte, keine ausformulierte Musterlösung, sofern nicht explizit gewünscht).
4. Teilpunkte je Kernpunkt vergeben, Summe gegen Gesamtpunktzahl prüfen.
5. Typische Fehlerquellen benennen (fachlich und methodisch, z. B. Operatorverfehlung, fehlender Textbezug, unvollständige Argumentation).
6. Bewertungshinweise für Grenzfälle ergänzen (z. B. Umgang mit richtigem Ergebnis bei falschem Lösungsweg, Teilleistung bei unvollständiger Bearbeitung).
7. Feedbackbausteine formulieren — kurze, wiederverwendbare Formulierungen für Rückmeldung an Schüler (positiv und konstruktiv-kritisch), ohne Namen.
8. Lehrplanbezug und Quellenangabe ergänzen.
9. Qualitätscheck durchführen.

## Bildungsgang-Prüfung
- Klasse 5–8: Sekundarschul-Lehrplanbasis, Erwartungshorizont orientiert sich an Kompetenzstufen der Sekundarschule.
- Klasse 9–10: Bildungsgang klären (Sekundarschulabschluss vs. gymnasialer Bildungsgang/Einführungsphase in Klasse 10). Unterschiedliche Anforderungsniveaus bei AFB-III-Aufgaben möglich.
- Klasse 11–12: nur Gymnasium, Qualifikationsphase — Erwartungshorizont orientiert sich näher an EPA-Aufgabenkultur.
- Bei fehlender oder unklarer Angabe: Rückfrage oder sichtbar markierte Annahme, siehe `routing_rules.json` und `bildungsgang_guardrails.md`.

## Lehrplanbezug
Herangezogen wird `data/curriculum/<fach>/<bildungsgang>/klasse_XX.md` entsprechend der geklärten Klassenstufe und des Bildungsgangs. Die im Erwartungshorizont geforderten Kompetenzen werden, soweit möglich, auf konkrete Kompetenzformulierungen aus dem jeweiligen Lehrplanabschnitt zurückgeführt. Nicht direkt lehrplangedeckte Erwartungen (z. B. spezifische Textkenntnis) werden als „didaktisch ergänzt" oder „Annahme" gekennzeichnet.

## Ausgabeformat
Kopfzeile: `Schulform: Gemeinschaftsschule | Bildungsgang: <…> | Lehrplanbasis: <…>`
Tabelle je Teilaufgabe: Teilaufgabe | erwartete Leistung | AFB | Punkte | Kennzeichnungsebene (1–4).
Abschnitt „Typische Fehler" (Liste).
Abschnitt „Bewertungshinweise für Grenzfälle".
Abschnitt „Feedbackbausteine" (kurze Textbausteine).
Abschnitt „Quellenbezug".
Kein eigenes Template unter `templates/` — Tabellenstruktur an `templates/stoffverteilungsplan.md` (tabellarisches Format) anlehnen, bis ein dediziertes Template ergänzt wird.

## Qualitätscheck
- Lehrplanbasis ausgewiesen und zur Klassenstufe/Bildungsgang passend?
- Teilpunkte summieren korrekt auf Gesamtpunktzahl?
- Jede Teilleistung einem AFB zugeordnet?
- Vier-Ebenen-Kennzeichnung bei nicht direkt lehrplangedeckten Erwartungen gesetzt?
- Quellen (Datei, Abschnitt) genannt?
- Feedbackbausteine ohne Namen, ohne Diagnosen, konstruktiv formuliert?
- Keine personenbezogenen Daten enthalten?

## Beispielprompt
„Erstelle den Erwartungshorizont zu Aufgabe 2 meiner Deutsch-Klassenarbeit Klasse 7 (Charakterisierung einer literarischen Figur), 20 Punkte gesamt, mit typischen Fehlern und Feedbackbausteinen."
