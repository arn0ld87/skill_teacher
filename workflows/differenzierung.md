# Workflow: Differenzierung

## Zweck
Erstellt konkrete Differenzierungsmaßnahmen für heterogene Lerngruppen an der Gemeinschaftsschule — Materialstufen, Aufgabenniveaus, Zeitdifferenzierung, Sozialformen — mit besonderem Blick auf die Bildungsgang-Heterogenität, die für Gemeinschaftsschulen typisch ist (Sekundarschul- und gymnasialer Bildungsgang in derselben Lerngruppe, insbesondere ab Klasse 7/8 aufwärts).

## Eingaben
Pflicht:
- Thema/Unterrichtsinhalt, für den differenziert werden soll
- Fach und Klassenstufe
- Art der Heterogenität, grob benannt (z. B. „unterschiedliches Lesetempo", „unterschiedliche Bildungsgänge in einer Lerngruppe", „unterschiedlicher Sprachstand")

Optional (mit Annahme bei Fehlen):
- Anzahl der Differenzierungsstufen — ohne Angabe: 3 Stufen annehmen (Basis/Regel/Erweiterung), kennzeichnen
- Sozialform-Präferenz — ohne Angabe: Mischung aus Einzel- und Partnerarbeit annehmen
- Bildungsgang-Zusammensetzung der Klasse — ohne Angabe bei Klasse 9–10: Annahme „gemischte Lerngruppe, Bildungsgänge noch nicht endgültig getrennt" kennzeichnen, da an Gemeinschaftsschulen üblich

## Vorgehen
1. Thema und Lernziel für die Gesamtgruppe festlegen (gemeinsamer Kern, der für alle gilt).
2. Heterogenitätsart klären: Leistungsniveau, Bildungsgang, Sprachstand, Arbeitstempo — kann kombiniert auftreten.
3. Materialstufen entwickeln: gleicher inhaltlicher Kern, unterschiedliche Komplexität/Textlänge/Aufgabenanzahl.
4. Aufgabenniveaus zuordnen (z. B. gestützte Aufgabe mit Formulierungshilfen vs. offene Aufgabe mit höherem Transferanspruch).
5. Zeitdifferenzierung festlegen (Zusatzaufgaben für schnellere Schüler, reduzierter Pflichtteil für andere).
6. Sozialform je Differenzierungsstufe festlegen (z. B. Einzelarbeit für Übungsniveau, Partnerarbeit für Transferniveau).
7. Bei Bildungsgang-Heterogenität: prüfen, ob Aufgaben auf beide Lehrplanbasen (Sekundarschule/Gymnasium) adaptierbar sind, ohne den gemeinsamen Unterrichtsgegenstand aufzugeben.
8. Übergänge zwischen Stufen beschreiben (wie Schüler wechseln können, ohne Etikettierung).
9. Lehrplanbezug und Quellenangabe ergänzen.
10. Qualitätscheck durchführen.

## Bildungsgang-Prüfung
Gemeinschaftsschulen führen Sekundarschul- und gymnasialen Bildungsgang häufig gemeinsam bis Klasse 8 oder 9, danach zunehmend getrennt. Zu klären:
- Klasse 5–8: i. d. R. gemeinsamer Unterricht, Differenzierung erfolgt binnendifferenziert innerhalb einer Lerngruppe mit einer Lehrplanbasis (Sekundarschule) als Ausgangspunkt, mit Erweiterungsangeboten für leistungsstärkere Schüler.
- Klasse 9–10: Bildungsgang-Trennung oft schulorganisatorisch vorgegeben (Kurse/Klassen nach Abschluss), kann aber je nach Schule noch gemeinsam unterrichtet werden — im Zweifel Rückfrage, ob eine oder zwei Lehrplanbasen relevant sind. Klasse 10 im gymnasialen Bildungsgang ist Einführungsphase.
- Klasse 11–12: nur Gymnasium, keine Bildungsgang-Heterogenität mehr in diesem Sinn — Differenzierung hier eher leistungs- und interessenbezogen innerhalb des gymnasialen Bildungsgangs.
- Bei unklarer Zusammensetzung: sichtbar markierte Annahme oder Rückfrage. Details in `routing_rules.json` und `bildungsgang_guardrails.md`.

## Lehrplanbezug
Bei einheitlicher Lehrplanbasis wird `data/curriculum/<fach>/<bildungsgang>/klasse_XX.md` herangezogen. Bei paralleler Bildungsgang-Heterogenität (z. B. Klasse 9 mit Sekundarschul- und gymnasialem Zweig im selben Kurs) werden beide Dateien herangezogen und die Lehrplanbasis im Kopf als „kombiniert" ausgewiesen; Unterschiede in Anforderungsniveau/Kompetenzformulierung werden explizit benannt.

## Ausgabeformat
Kopfzeile: `Schulform: Gemeinschaftsschule | Bildungsgang: <…/kombiniert> | Lehrplanbasis: <…/kombiniert>`
Tabelle: Differenzierungsstufe | Material/Aufgabe | Anforderungsniveau | Sozialform | Zeitrahmen.
Abschnitt „Gemeinsamer Kern" (was für alle gilt).
Abschnitt „Übergänge zwischen Stufen" (ohne Etikettierung).
Abschnitt „Quellenbezug".
Kein eigenes Template unter `templates/` — Struktur an `templates/unterrichtsreihe.md` (Aufbau nach Lernphasen) anlehnen.

## Qualitätscheck
- Lehrplanbasis ausgewiesen, bei Bildungsgang-Mischung als „kombiniert" gekennzeichnet?
- Gemeinsamer inhaltlicher Kern für alle Differenzierungsstufen erkennbar?
- Keine Etikettierung von Schülern oder Gruppen nach Diagnose/Defizit, nur funktionale Beschreibung von Förderbedarf?
- Vier-Ebenen-Kennzeichnung bei Annahmen zur Klassenzusammensetzung gesetzt?
- Quellen genannt?
- Keine personenbezogenen Daten, keine Schülernamen?

## Beispielprompt
„Erstelle differenzierte Aufgaben zum Thema Kurzgeschichte für Deutsch Klasse 9, gemischte Lerngruppe mit Sekundarschul- und gymnasialem Bildungsgang, drei Anforderungsstufen."
