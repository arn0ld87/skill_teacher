# Lehrer-Skill — Gemeinschaftsschule Sachsen-Anhalt

Modularer, lehrplangebundener Skill für Lehrkräfte an der **Gemeinschaftsschule Sachsen-Anhalt**. Unterstützt bei typischen schulischen Planungs-, Material- und Kommunikationsaufgaben in den Fächern **Deutsch** und **Evangelische Religion** (Klassen 5–12).

> **Wichtig:** Der Skill arbeitet ausschließlich mit den hinterlegten Lehrplänen. Er erfindet keine Kompetenzen, keine Operatoren und keine Prüfungsformate. Jede lehrplanbezogene Aussage wird mit Quelle ausgewiesen.

## Was dieser Skill kann

- **Stoffverteilungspläne und Jahresplanungen** auf Basis der Lehrplan-Kompetenzbereiche
- **Unterrichtsreihen, Stundenentwürfe, Wochenpläne, Arbeitsblätter**
- **Klassenarbeiten, Klausuren, mündliche Prüfungen, Erwartungshorizonte, Bewertungsraster, Kompetenzraster**
- **Förderpläne, Differenzierung, Lernstandserhebungen, Schülerfeedback**
- **Sitzpläne, Elternbriefe, Elternabende, Gesprächsprotokolle**
- **Vertretungsstunden, Projektarbeiten, Exkursionen/Wandertage**
- **Aufgaben mit Lösungen, didaktische Hinweise, Materiallisten**

## Was dieser Skill nicht kann

- **Katholischen Religionsunterricht** und **Ethik** (keine Lehrpläne hinterlegt)
- Klassen außerhalb 5–12
- Andere Bundesländer oder Schulformen
- Verbindliche schulrechtliche Auskünfte (Ausgaben sind Entwürfe, keine Rechtsauskunft)

## Schnellstart

1. Aufgabe in natürlicher Sprache formulieren, z. B.:
   - „Stoffverteilungsplan Deutsch Klasse 7 für das Schuljahr 2026/27."
   - „Klassenarbeit Deutsch Klasse 9 zum Thema Erörterung."
   - „Abiturklausur Deutsch Klasse 12 mit Erwartungshorizont."
   - „Unterrichtsreihe Ev. Religion Klasse 6 zu Gleichnissen."
   - „Mündliche Prüfung Ev. Religion Klasse 10, gymnasialer Bildungsgang."
   - „Sitzplan für 24 Schüler, U-Form, mit Kürzeln."

2. Der Skill klärt bzw. leitet ab: **Schulform**, **Bildungsgang**, **Lehrplanbasis**, **Fach**, **Klasse**, **Thema**, **Ziel**, **Zeitrahmen**, **Lerngruppe**, **Leistungsniveau**, **Ausgabeformat**.

3. Der Skill lädt die passende Lehrplan-Datei aus `data/curriculum/`, nutzt das passende Template aus `templates/` und folgt dem Workflow aus `workflows/`.

## Verzeichnisstruktur

```
teacher-skill-sachsen-anhalt/
├── SKILL.md                 # Hauptskill (Router, Regeln, Pflicht-Kopf)
├── README.md                # diese Datei
├── data/
│   └── curriculum/
│       ├── index.json                 # Übersicht aller Curricula
│       ├── routing_rules.json         # Bildungsgang-Routing
│       ├── competency_matrix.json     # Kompetenzbereiche je Klasse
│       ├── deutsch/
│       │   ├── sekundarschule/        # Kl. 5–10
│       │   └── gymnasium/             # Kl. 9–12 (Kl. 12 als Verweis auf Kl. 11)
│       └── religion/
│           ├── sekundarschule/        # Kl. 5–10
│           └── gymnasium/             # Kl. 9–12
├── workflows/               # 21 Workflow-Dateien (eine je Aufgabentyp)
├── templates/               # 19 ausfüllbare Markdown-Templates
├── prompts/                 # 6 Prompt-Dateien (System, Routing, Guardrails, Output)
├── examples/                # 6 Beispielausgaben mit Pflicht-Kopf
├── reports/                 # input_mapping, input_issues, coverage, validation
└── tests/                   # 5 Test-Dateien (checklist, hallucination, routing, traceability, examples)
```

## Bildungsgang-Routing (Kurzfassung)

| Klasse | Lehrplanbasis |
|---|---|
| 5–8 | primär **Sekundarschule** |
| 9–10 | Bildungsgang klären; bei gymnasialem Bildungsgang zusätzlich **Gymnasium** |
| 11–12 | **Gymnasium** (Qualifikationsphase, Abiturbezug) |

> Volle Logik: `data/curriculum/routing_rules.json` und `SKILL.md`.

## Fächer

| Fach | Klassen 5–8 | Klassen 9–10 | Klassen 11–12 |
|---|---|---|---|
| Deutsch | Sekundarschule | je nach Bildungsgang | Gymnasium (Qualifikationsphase) |
| Evangelische Religion | Sekundarschule | je nach Bildungsgang | Gymnasium (Qualifikationsphase) |

## Datenschutz

- **Keine echten Schülernamen** — nur Kürzel (S1, S2 … oder A., B. …).
- **Keine Diagnosen** (medizinisch, psychologisch, rechtlich).
- **Förderbedarf** wird funktional/beobachtungsbasiert beschrieben.
- **Elternbriefe** ohne unnötige personenbezogene Details.
- **Gesprächsprotokolle** sachlich, knapp, beobachtungsbasiert.

Details: `prompts/curriculum_guardrails.md`.

## Lehrplanbindung

Jede lehrplanbezogene Aussage trägt eine Quelle:

- **Datei** (z. B. `lp_sks_deutsch_01_08_2019_k2.pdf`)
- **Lehrplanbasis** (Sekundarschule / Gymnasium)
- **Fach** (Deutsch / Evangelische Religion)
- **Klasse** (5–12)
- **Abschnitt / Kapitelnummer / Seite**

Nicht direkt aus dem Lehrplan ableitbare Aussagen werden mit einer der folgenden Ebenen gekennzeichnet:

- (1) Direkt aus Lehrplan ableitbar
- (2) Didaktisch ergänzt
- (3) Annahme
- (4) Noch zu prüfen

## Eingabequellen

Die Lehrpläne liegen unter `input/lehrplaene/`:

```
input/lehrplaene/
├── sekundarschule/
│   ├── deutsch/
│   │   ├── lp_sks_deutsch_01_08_2019_k2.pdf
│   │   └── Fachliche_Orientierung_Deutsch.pdf
│   └── religion/
│       └── lp_sks_evrel_01_08_2019.pdf
└── gymnasium/
    ├── deutsch/
    │   └── FLP_Deutsch_Gym_swd.pdf
    └── religion/
        └── FLP_EvangRU_Gym_01082022_swd.pdf
```

Zuordnung dokumentiert in `reports/input_mapping.md`. Auffälligkeiten dokumentiert in `reports/input_issues.md`.

## Qualitätssicherung

- `tests/checklist.md` — prüfbare Kriterien
- `tests/hallucination_tests.md` — Halluzinations-Testfälle
- `tests/bildungsgang_routing_tests.md` — Routing-Logik
- `tests/curriculum_traceability_tests.md` — Quellenrückverfolgbarkeit
- `tests/example_outputs_tests.md` — Pflichtelemente der Beispielausgaben
- `reports/coverage_report.md` — Abdeckungsbericht
- `reports/validation_report.md` — Prüfbericht

## Wichtige Hinweise

- **Der Skill ist kein Ersatz für die Fachkonferenz und Schulleitung.** Alle Ausgaben sind Entwürfe und müssen vor schulischem Einsatz geprüft werden.
- **Der Skill erfindet nichts** — was im Lehrplan nicht steht, wird als „didaktisch ergänzt" markiert.
- **Die Oberstufenverordnung Sachsen-Anhalt** regelt die konkreten Abiturprüfungsformate; diese sind im Fachlehrplan nicht eigens ausgewiesen.
- **Eine formale Operatorenliste mit AFB-Zuordnung ist im bereitgestellten Lehrplan (beide Fächer) nicht enthalten.** AFB-Zuordnungen in Beispielen sind didaktisch ergänzt und müssen mit der schulinternen Liste abgeglichen werden.

## Lizenz / Quellennachweis

Die Lehrpläne stammen vom **Landesinstitut für Schulqualität und Lehrerbildung Sachsen-Anhalt (LISA)** und sind unter **Creative Commons CC BY-SA 3.0** lizenziert (siehe Header der PDFs). Der Skill selbst enthält Auszüge und konsolidierte Zusammenfassungen und ist als pädagogisches Arbeitsmittel für Lehrkräfte gedacht.

## Maintainer / Kontakt

Skill-Betreiber: siehe Projektkontext. Bei Updates der Lehrpläne (z. B. neue Fassung) muss die jeweilige Curriculum-Datei in `data/curriculum/` aktualisiert und `index.json` angepasst werden.