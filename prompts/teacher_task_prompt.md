# Teacher-Task-Prompt — Ablauf für eine konkrete Aufgabe

Für jede Lehrkraft-Anfrage (Stundenentwurf, Klassenarbeit, Elternbrief, …):

## 1. Aufgabe einordnen
- Welcher **Workflow** passt? → `workflows/<name>.md`.
- Welche Eingaben liegen vor, welche fehlen?

## 2. Routing (siehe `routing_prompt.md`)
- Fach, Klasse, Bildungsgang, Lehrplanbasis festlegen.
- Fehlende Angaben als **Annahme** sichtbar machen.

## 3. Lehrplan laden
- Passende Datei(en) aus `data/curriculum/<fach>/<basis>/klasse_XX.md`.
- Bei Klasse 9–10 mit unklarem Bildungsgang ggf. beide Basen bereithalten.

## 4. Erstellen
- Struktur aus dem passenden **Template** (`templates/<name>.md`) übernehmen.
- Kompetenzen/Inhalte **aus dem Lehrplan** übernehmen, mit Quelle.
- Didaktische Ergänzungen als solche kennzeichnen (Ebene 2).

## 5. Ausgabe formatieren
- Pflicht-Kopf (Schulform / Bildungsgang / Lehrplanbasis).
- Vier-Ebenen-Kennzeichnung, wo nötig.
- Quellenblock bei Lehrplanbezug.
- Datenschutz einhalten (keine echten Namen/Diagnosen).

## 6. Qualitätscheck
- Checkliste des jeweiligen Workflows durchgehen.
- Offene Punkte / Annahmen am Ende auflisten.

## Eingabe-Raster (fragt der Skill intern ab)
```
Fach:            {{fach}}
Klassenstufe:    {{klasse}}
Schulform:       Gemeinschaftsschule
Bildungsgang:    {{bildungsgang}}
Lehrplanbasis:   {{lehrplanbasis}}
Thema:           {{thema}}
Ziel:            {{ziel}}
Zeitrahmen:      {{zeitraum}}
Lerngruppe:      {{lerngruppe}}
Leistungsniveau: {{niveau}}
Ausgabeformat:   {{format}}
```
