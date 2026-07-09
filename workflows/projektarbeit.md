# Workflow: Projektarbeit

## Zweck
Begleitet Planung, Durchführung und Bewertung einer Projektarbeit (z. B. Facharbeit, Projektwoche, fächerübergreifendes Projekt) in Deutsch oder Ev. Religion — von der Themenfindung über Zeitplan und Meilensteine bis zu Bewertungskriterien und Dokumentationspflicht. Deckt sowohl die Sekundarschul-Prüfungsform (Projektarbeit als Teil des Abschlussverfahrens Kl. 9/10) als auch gymnasiale Formate (Facharbeit/Seminarfach-Analogon Kl. 11/12) ab.

## Eingaben
Pflicht:
- Fach (Deutsch oder Ev. Religion) oder fächerübergreifend mit Deutsch/Religion als Leitfach
- Klassenstufe
- Anlass (Unterrichtsprojekt, Prüfungsteil, Projektwoche, freiwillige Vertiefung)
- Verfügbarer Zeitraum (Wochen/Monate bis Abgabe)

Optional (mit Annahme bei Fehlen):
- Themenvorschlag der Schüler:innen — ohne Angabe: drei Themenvorschläge passend zu Fach/Klassenstufe generieren, als Ebene-2-Vorschlag (didaktisch ergänzt) markiert
- Gruppengröße (Einzel-/Partnerarbeit) — ohne Angabe: Einzelarbeit annehmen (Standardfall bei Prüfungsformaten)
- Umfang der schriftlichen Dokumentation — ohne Angabe: Richtwert nach Klassenstufe (Kl. 9/10 ca. 6–10 Seiten, Kl. 11/12 ca. 10–15 Seiten) als Annahme kennzeichnen
- Bewertungsgewichtung (schriftlich vs. Präsentation vs. Prozess) — ohne Angabe: Standardgewichtung 50/30/20 als Annahme

Fehlt die Klassenstufe komplett, RÜCKFRAGE stellen — Projektarbeit ist bildungsgangspezifisch (Prüfungsformat unterscheidet sich stark zwischen Kl. 9/10 und Kl. 11/12).

## Vorgehen
1. Bildungsgang-Prüfung durchführen (siehe unten) und Kopf-Kennzeichnung festlegen.
2. Anlass klären: Prüfungsrelevante Projektarbeit (Sekundarschulabschluss) vs. unterrichtsinterne Projektarbeit vs. gymnasiale Facharbeit — daraus ergeben sich unterschiedliche Formvorgaben.
3. Themenfindung: Bezug zu einer Lehrplaneinheit/Unterrichtsreihe herstellen, Themenformulierung als konkrete Fragestellung (nicht nur Oberbegriff).
4. Kompetenzbezug ausweisen: Welche Fachkompetenzen (Deutsch: z. B. Textproduktion, Recherche, Präsentation; Religion: z. B. Urteilsbildung, Perspektivenübernahme) werden durch das Projekt geschult.
5. Zeitplan mit Meilensteinen erstellen: Themenfindung → Exposé/Gliederung → Recherchephase → Rohfassung → Überarbeitung → Abgabe → ggf. Präsentation. Realistische Zwischentermine anhand des verfügbaren Zeitraums setzen.
6. Betreuungsstruktur festlegen: Anzahl und Anlass der Beratungsgespräche (i. d. R. 2–3 feste Termine), Dokumentationspflicht der Betreuung (Kurzprotokoll je Gespräch, kein Bewertungsvorgriff).
7. Bewertungskriterien formulieren, getrennt nach schriftlicher Leistung, Präsentation/Prüfungsgespräch (falls vorgesehen) und Arbeitsprozess (Selbstständigkeit, Termintreue).
8. Dokumentationspflicht für Schüler:innen benennen: Quellenverzeichnis, Eigenständigkeitserklärung, ggf. Praxisbericht bei Projektwochen.
9. Quellenbezug (Lehrplanstelle, ggf. Prüfungsordnungshinweis als Annahme) anfügen.
10. Qualitätscheck durchführen, Ausgabe formatieren.

## Bildungsgang-Prüfung
- Klasse 5–8: Projektarbeit ist unterrichtsinternes Format ohne Prüfungscharakter, Lehrplanbasis Sekundarschule.
- Klasse 9–10: Bildungsgang klären. Sekundarschulabschluss/mittlerer Schulabschluss → Projektarbeit kann Teil des Abschlussverfahrens sein (Annahme, Ebene 3: konkrete Prüfungsordnungsdetails nicht im Repository hinterlegt, daher als „noch zu prüfen" kennzeichnen). Gymnasialer Bildungsgang → Klasse 10 ist Einführungsphase, Projektarbeit hier eher vorbereitend auf spätere Facharbeit, kein Abschlussprüfungsbezug.
- Klasse 11–12: nur Gymnasium, Qualifikationsphase. Facharbeit bzw. seminarfachähnliches Format als Annahme kennzeichnen (Ebene 3) — die genaue Bezeichnung und Verortung im Schulformkontext einer Gemeinschaftsschule ist schulspezifisch und nicht abschließend im Repository hinterlegt.
- Bei unklarem Bildungsgang in Kl. 9–10: Rückfrage stellen ODER sichtbar markierte Annahme (Sekundarschule) treffen.
- Routing-Details siehe `routing_rules.json` und `bildungsgang_guardrails.md` — dort ist die Klasse-10-Sonderregel verbindlich hinterlegt.

## Lehrplanbezug
Herangezogen werden `data/curriculum/deutsch/` bzw. `data/curriculum/religion/` — je nach Bildungsgang die Unterordner `sekundarschule/` oder `gymnasium/` für die passende Klassenstufe. Die Lehrplanbasis wird im Ausgabekopf ausgewiesen. Wichtig: Der organisatorische Rahmen der Projektarbeit (Prüfungsordnung, Bewertungsschlüssel des Abschlussverfahrens) ist NICHT Teil der Lehrplandateien und wird daher konsequent als Annahme (Ebene 3) oder „noch zu prüfen" (Ebene 4) gekennzeichnet, nicht als direkter Lehrplanbezug (Ebene 1). Nur der fachliche Kompetenzbezug (Ebene 1/2) stützt sich auf die Curriculum-Dateien.

## Ausgabeformat
Kopfzeile: `Schulform: Gemeinschaftsschule | Bildungsgang: <…> | Lehrplanbasis: <…>`
Danach: Thema/Fragestellung, Klassenstufe, Anlass, Zeitraum.
Abschnitt Kompetenzbezug.
Abschnitt Zeitplan/Meilensteine (Tabelle: Phase | Zeitraum | Ergebnis).
Abschnitt Betreuung (Anzahl Termine, Anlass, Dokumentation).
Abschnitt Bewertungskriterien (Tabelle: Kriterium | Gewichtung | Beschreibung), Vorlage `templates/bewertungsraster.md` nutzen.
Abschnitt Dokumentationspflicht.
Abschnitt Quellenbezug.
Kein dediziertes Projektarbeit-Template unter `templates/` vorhanden — Bewertungsteil an `templates/bewertungsraster.md` anlehnen, Zeitplan-Struktur an `templates/jahresplanung.md` orientieren.

## Qualitätscheck
- Lehrplanbasis im Kopf ausgewiesen, Bildungsgang bei Kl. 9–10 geklärt oder als Annahme markiert?
- Vier-Ebenen-Kennzeichnung konsequent angewandt, insbesondere Prüfungsordnungsdetails als Annahme/offen gekennzeichnet (nicht als Lehrplanbezug ausgegeben)?
- Zeitplan realistisch im Rahmen des angegebenen Zeitraums?
- Bewertungskriterien vollständig und Gewichtung nachvollziehbar?
- Quellen (Lehrplandatei, Fach, Klasse, Abschnitt) genannt, soweit Lehrplanbezug besteht?
- Keine echten Schülernamen, keine Diagnosen, keine Schuldzuweisungen bei Betreuungshinweisen?
- Datenschutz-Hinweis ergänzt, falls Beispielarbeiten oder Schülerdaten referenziert werden?

## Beispielprompt
„Plane eine Projektarbeit für Deutsch, Klasse 9, im Rahmen des Sekundarschulabschlusses zum Themenfeld Berufsorientierung und Bewerbung, mit Zeitplan über 8 Wochen und Bewertungsraster."
