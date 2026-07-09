# Input-Mapping — Zuordnung der Lehrplandateien

Zuordnung der bereitgestellten PDF-Lehrpläne zu Fach, Lehrplanbasis und Klassenstufen.

| Datei | Lehrplanbasis | Fach | Klassen (laut Lehrplan) | Original-Ablage | Ziel im Skill |
|---|---|---|---|---|---|
| `lp_sks_deutsch_01_08_2019_k2.pdf` | Sekundarschule | Deutsch | 5/6, 7/8, 9, 9/10 | `input/lehrplaene/sekundarschule/deutsch/` | `data/curriculum/deutsch/sekundarschule/klasse_05–10.md` |
| `Fachliche_Orientierung_Deutsch.pdf` | Sekundarschule | Deutsch | Ergänzung (fachliche Orientierung) | `input/lehrplaene/sekundarschule/deutsch/` | ergänzend in `deutsch/sekundarschule/` |
| `lp_sks_evrel_01_08_2019.pdf` | Sekundarschule | Evangelische Religion | 5/6, 7/8, 9/10 | `input/lehrplaene/sekundarschule/religion/` | `data/curriculum/religion/sekundarschule/klasse_05–10.md` |
| `FLP_Deutsch_Gym_swd.pdf` | Gymnasium | Deutsch | 5/6, 7/8, 9, 10 (EP), 11/12 (Q) | `input/lehrplaene/gymnasium/deutsch/` | `data/curriculum/deutsch/gymnasium/klasse_09–12.md` |
| `FLP_EvangRU_Gym_01082022_swd.pdf` | Gymnasium | Evangelische Religion | 5/6, 7/8, 9, 10 (EP), 11/12 (Q) | `input/lehrplaene/gymnasium/religion/` | `data/curriculum/religion/gymnasium/klasse_09–12.md` |

**EP** = Einführungsphase (Klasse 10) · **Q** = Qualifikationsphase (Klasse 11/12).

## Zuordnungslogik
- Die Eingabestruktur `input/lehrplaene/<basis>/<fach>/` war bereits sauber angelegt; keine Umbenennung nötig.
- `Fachliche_Orientierung_Deutsch.pdf` ist kein eigener Jahrgangslehrplan, sondern eine fachliche
  Orientierung; sie wird ergänzend zum Deutsch-Sekundarschullehrplan ausgewertet.
- Die Gymnasial-Fachlehrpläne decken laut Inhaltsverzeichnis 5–12 ab. Für die Gemeinschaftsschule
  werden aus ihnen nur die Jahrgänge **9–12** in `data/curriculum/…/gymnasium/` überführt, da 5–8
  über die Sekundarschule laufen (siehe `routing_rules.json`).

## Nicht bereitgestellt (bewusst dokumentiert)
- Katholischer Religionsunterricht — nicht vorhanden.
- Ethik — nicht vorhanden.
- Separate Lehrplandokumente ausschließlich für die gymnasiale Oberstufe (die Oberstufe ist in den
  vorliegenden Fachlehrplänen als Einführungs-/Qualifikationsphase enthalten).
