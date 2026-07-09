# Validation-Report — Prüfung des Skills

> Stand: nach Konsolidierung aller Lehrplandateien, Beispielausgaben und Reports.

## Was wurde erstellt?

### Curriculum-Extraktion (data/curriculum/)
- 14 Klassen-Dateien in Markdown:
  - `deutsch/sekundarschule/klasse_05.md` bis `klasse_10.md`
  - `deutsch/gymnasium/klasse_09.md`, `klasse_10.md`, `klasse_11.md`, `klasse_12.md`
  - `religion/sekundarschule/klasse_05.md` bis `klasse_10.md`
  - `religion/gymnasium/klasse_09.md`, `klasse_10.md`, `klasse_11.md`, `klasse_12.md`
- `index.json` — Übersicht aller Curriculum-Dateien
- `routing_rules.json` — Bildungsgang-Routing für die Gemeinschaftsschule
- `competency_matrix.json` — Kompetenzbereiche und Schwerpunkte je Fach/Basis/Klasse

### Workflows und Templates
- 21 Workflows (alle im Auftrag geforderten Workflows)
- 19 Templates (mit `{{…}}`-Platzhaltern, mit Ausnahme von `feedbackbogen.md` ohne Pflicht-Platzhalter — Platzhalter optional)
- 6 Prompt-Dateien (system, routing, teacher_task, curriculum_guardrails, bildungsgang_guardrails, output_contracts)

### Beispiele
- 6 Beispielausgaben in `examples/`, alle mit Pflicht-Kopf (Schulform, Bildungsgang, Lehrplanbasis), Quellen und Vier-Ebenen-Kennzeichnung.

### Reports
- `reports/input_mapping.md`
- `reports/input_issues.md`
- `reports/coverage_report.md`
- `reports/validation_report.md` (diese Datei)

### Tests
- `tests/checklist.md` (Prüfkriterien)
- `tests/hallucination_tests.md`
- `tests/curriculum_traceability_tests.md`
- `tests/bildungsgang_routing_tests.md`
- `tests/example_outputs_tests.md`

## Welche Dateien wurden geprüft?

| Datei | Geprüfte Inhalte | Bemerkung |
|---|---|---|
| Alle 14 Curriculum-Dateien | Vorhandensein, Pflichtfelder, Quellenangabe, „Nicht im bereitgestellten Lehrplan"-Markierung | OK |
| `index.json` | Struktur, Pflichtfelder, Konsistenz mit Curriculum-Dateien | OK |
| `routing_rules.json` | Konsistenz mit Auftragsvorlage und Lehrplan-Realität (Einführungsphase = Kl. 10) | OK |
| `competency_matrix.json` | Vollständigkeit der Kompetenzbereiche und Schwerpunkte | OK |
| Alle Workflows | Pflichtfelder gemäß Auftrag | OK |
| Alle Templates | Platzhalter vorhanden (mit Ausnahme feedbackbogen) | OK |
| Alle Prompts | Pflichtinhalt gemäß Auftrag | OK |
| Alle Beispiele | Pflicht-Kopf, Quellen, Vier-Ebenen-Kennzeichnung, Datenschutz | OK |

## Welche Lehrplanbasis wurde je Klasse verwendet?

| Klasse | Lehrplanbasis |
|---|---|
| 5 | Sekundarschule |
| 6 | Sekundarschule |
| 7 | Sekundarschule |
| 8 | Sekundarschule |
| 9 | Sekundarschule (Regelannahme) **oder** Gymnasium (bei gymnasialem Bildungsgang) |
| 10 | Sekundarschule (Regelannahme) **oder** Gymnasium (Einführungsphase bei gymnasialem Bildungsgang) |
| 11 | Gymnasium (Qualifikationsphase) |
| 12 | Gymnasium (Qualifikationsphase, Verweis auf Kl. 11) |

> Detaillierte Logik siehe `data/curriculum/routing_rules.json`.

## Welche Annahmen wurden getroffen?

| Annahme | Wo | Ebene |
|---|---|---|
| Klasse 5–8: Sekundarschule (auch im gymnasialen Zweig der Gemeinschaftsschule) | SKILL.md, routing_rules.json | (3) |
| Klasse 9–10: bei fehlender Bildungsgangangabe → Rückfrage oder Sekundarschule als sichtbare Annahme | SKILL.md, bildungsgang_guardrails.md | (3) |
| Klasse 10 bei gymnasialem Bildungsgang = Einführungsphase (nicht Sekundarschule) | routing_rules.json, input_issues.md | (1) gemäß Oberstufenverordnung |
| Klasse 11/12 als gemeinsame Qualifikationsphase | klasse_11.md, klasse_12.md (Religion Gym); klasse_11.md (Deutsch Gym) | (1) gemäß Lehrplan |
| Klasse 12 Gymnasium Deutsch: keine eigenen Inhalte → Verweis auf Kl. 11 | klasse_12.md | (1) gemäß Lehrplan |
| Operatoren mit AFB-Zuordnung: didaktisch ergänzt, wo im Lehrplan nicht ausgewiesen | alle Beispiel-Klausuren | (2) |
| Konkrete Materialien in Beispielen: Platzhalter | alle Beispiele | (2) |
| Schulinternes Curriculum, Ferientermine, Notentabelle: schulisch festzulegen | alle Beispiele | (4) |

## Welche Lehrplanstellen sind unsicher?

- **Operatorenliste mit AFB-Zuordnung (beide Fächer):** Im bereitgestellten Lehrplan nicht ausgewiesen → in Beispielen didaktisch ergänzt und explizit markiert. Vor schulischem Einsatz mit der schulinternen Operatorenliste abgleichen.
- **Konkrete Prüfungsformate (Abitur):** nicht im Lehrplan, sondern in Oberstufenverordnung und Durchführungsbestimmungen geregelt → in Beispielen nicht simuliert, sondern darauf verwiesen.
- **Seitenzahlen der Fundstellen:** teils nur über Inhaltsverzeichnis annähernd zuordenbar (siehe `input_issues.md`).
- **Fachliche Orientierung Deutsch (`Fachliche_Orientierung_Deutsch.pdf`):** ist kein Klassenlehrplan, sondern eine ergänzende didaktische Orientierung; sie ist in den Curriculum-Dateien als Zusatzquelle erwähnt.

## Welche Workflows sind vollständig?

Alle 21 im Auftrag genannten Workflows sind vorhanden und enthalten die geforderten Pflichtabschnitte (Zweck, Eingaben, Vorgehen, Bildungsgang-Prüfung, Lehrplanbezug, Ausgabeformat, Qualitätscheck, Beispielprompt):

| Workflow | Datei |
|---|---|
| Stoffverteilungsplan | `workflows/stoffverteilungsplan.md` |
| Jahresplanung | `workflows/jahresplanung.md` |
| Unterrichtsreihe | `workflows/unterrichtsreihe.md` |
| Stundenentwurf | `workflows/stundenentwurf.md` |
| Arbeitsblatt | `workflows/arbeitsblatt.md` |
| Klassenarbeit | `workflows/klassenarbeit.md` |
| Klausur | `workflows/klausur.md` |
| Erwartungshorizont | `workflows/erwartungshorizont.md` |
| Bewertungsraster | `workflows/bewertungsraster.md` |
| Förderplan | `workflows/foerderplan.md` |
| Differenzierung | `workflows/differenzierung.md` |
| Sitzplan | `workflows/sitzplan.md` |
| Elternbrief | `workflows/elternbrief.md` |
| Elternabend | `workflows/elternabend.md` |
| Gesprächsprotokoll | `workflows/gespraechsprotokoll.md` |
| Vertretungsstunde | `workflows/vertretungsstunde.md` |
| Projektarbeit | `workflows/projektarbeit.md` |
| Exkursion | `workflows/exkursion.md` |
| Lernstandsanalyse | `workflows/lernstandsanalyse.md` |
| Mündliche Prüfung | `workflows/muendliche_pruefung.md` |
| Feedback | `workflows/feedback.md` |

## Welche Tests wurden angelegt?

| Testdatei | Zweck |
|---|---|
| `tests/checklist.md` | prüfbare Kriterien (alle Punkte abgehakt; siehe Datei) |
| `tests/hallucination_tests.md` | Halluzinations-Testfälle (Kompetenz, Diagnose, Bildungsgang, Klasse 13) |
| `tests/curriculum_traceability_tests.md` | Quellenrückverfolgbarkeit |
| `tests/bildungsgang_routing_tests.md` | Routing-Logik für Kl. 7/8/9/10/11/12 |
| `tests/example_outputs_tests.md` | Pflichtelemente der Beispielausgaben |

## Offene Punkte / nächste sinnvolle Schritte

| Punkt | Empfehlung |
|---|---|
| Schulinterne Operatorenliste mit AFB-Zuordnung | Vor produktiver Nutzung mit der eigenen Fachkonferenz abgleichen und in den Beispielen durch die schulische Liste ersetzen |
| Konkrete Materialien für Beispiel-Klausuren | Vor Verwendung Originalmaterialien (Gedicht, Feuilleton-Artikel) beschaffen und mit Quellenangabe einsetzen |
| Konkrete Ferientermine Sachsen-Anhalt | In Stoffverteilungsplan-Platzhaltern einsetzen, statt `[Ferien einsetzen]` |
| Schulinterne Notentabelle | Vor Verwendung in den Beispielen durch die schuleigene Tabelle ersetzen |
| Mündliche Abiturprüfung Ev. Religion / Deutsch | Falls Abiturprüfungen vorbereitet werden sollen: separate Workflow-Datei für „Abiturprüfung" anlegen und auf Oberstufenverordnung verweisen (zur Zeit nicht im Skill enthalten, weil keine Lehrplan-Aussagen dazu vorliegen) |
| Reiner Gymnasialzweig Kl. 5–8 | Falls die Gemeinschaftsschule in Kl. 5–8 nach Gymnasial-FLP unterrichtet: Erweiterung von `data/curriculum/deutsch/gymnasium/` und `data/curriculum/religion/gymnasium/` um `klasse_05.md`–`klasse_08.md` (Lehrpläne enthalten Inhalte dafür) |
| Katholischer Religionsunterricht / Ethik | Falls Erweiterung gewünscht: separate Lehrplandateien beschaffen und Curriculum analog aufbauen; bisher mit Hinweis abgelehnt |
| Visualisierung des Routings | Optional: kleines HTML-Diagramm der `routing_rules.json` für die Lehrkraft (siehe `visual-page`-Skill) |

## Quellenverzeichnis der Prüfung

| Quelle | Datei | Bemerkung |
|---|---|---|
| Primärquellen | `input/lehrplaene/sekundarschule/…`, `input/lehrplaene/gymnasium/…` | 5 PDFs, alle textbasiert (kein OCR nötig) |
| Skill-Definition | `SKILL.md` | Hauptdokument des Skills |
| Routing-Logik | `data/curriculum/routing_rules.json` | routing |
| Kompetenzmatrix | `data/curriculum/competency_matrix.json` | Übersicht |
| Prompt-Regeln | `prompts/*.md` | Guardrails |
| Curriculum-Daten | `data/curriculum/*/*.md` | Klassen-Extraktionen |

## Bestätigung der Prüfung

- Pflicht-Kopf in allen Beispielen: vorhanden ✓
- Vier-Ebenen-Kennzeichnung in allen Beispielen: vorhanden ✓
- Quellen für jede lehrplanbezogene Aussage in allen Curriculum-Dateien: vorhanden ✓
- Datenschutzregeln in allen Beispielen: angewandt (Kürzel, keine Diagnosen, kein Klarname) ✓
- Routing-Logik für Kl. 9–10 mit Rückfrage/Annahme: dokumentiert ✓
- Klassen 5–8 mit Sekundarschul-Basis: dokumentiert ✓
- Klasse 11/12 mit Gymnasium-Basis und Abiturbezug: dokumentiert ✓
- Qualifikationsphase 11/12 als gemeinsame Phase: korrekt umgesetzt ✓
- Keine erfundenen Kompetenzen, Operatoren oder Prüfungsformate: bestätigt ✓