# Coverage-Report — Abdeckung pro Fach, Klasse, Lehrplanbasis

> Stand: nach Konsolidierung aller Lehrplandateien und Beispielausgaben.

## Zusammenfassung

- **Fächer:** Deutsch, Evangelische Religion
- **Klassen:** 5, 6, 7, 8, 9, 10, 11, 12
- **Lehrplanbasen:** Sekundarschule (5–10), Gymnasium (9–12)
- **Status:** alle vom Auftrag geforderten Klassen-Lehrplan-Kombinationen sind hinterlegt. Klasse 12 Gymnasium ist als Verweis-Datei auf Klasse 11 Gymnasium implementiert, weil der Lehrplan die Qualifikationsphase 11/12 gemeinsam führt.

## Detail-Übersicht

### Deutsch — Sekundarschule

| Klasse | Lehrplan-Original | Lehrplan-Struktur | Kompetenzbereiche extrahiert | Inhaltsbereiche extrahiert | Status |
|---|---|---|---|---|---|
| 5 | `lp_sks_deutsch_01_08_2019_k2.pdf` | Doppeljahrgang 5/6 | 4 (Sprache, Sprechen/Schreiben, Lesen, Medien) | ja, grundlegende Wissensbestände | vollständig |
| 6 | dito | Doppeljahrgang 5/6 (deckungsgleich) | 4 | ja | vollständig |
| 7 | dito | Doppeljahrgang 7/8 | 4 (RSA + HSA getrennt) | ja, Lektüreverzeichnis | vollständig |
| 8 | dito | Doppeljahrgang 7/8 (deckungsgleich) | 4 (RSA + HSA getrennt) | ja | vollständig |
| 9 | dito | Einzeljahrgang 9 / Doppeljahrgang 9/10 | 4 (RSA + HSA getrennt) | ja | vollständig |
| 10 | dito | Doppeljahrgang 9/10 | 4 (realschulabschlussbezogen) | ja | vollständig |

**Quelle für Verbindliche Vorgaben:** Kap. 2.3 des Lehrplans (zwei auswendig gelernte Texte je Schuljahrgang).

**Ergänzung:** `Fachliche_Orientierung_Deutsch.pdf` ist keine eigene Klassenstufe, sondern eine ergänzende fachdidaktische Orientierung; sie ist im `index.json` als Ergänzung referenziert und in den Curriculum-Dateien als zusätzliche Quelle genannt.

### Deutsch — Gymnasium

| Klasse | Lehrplan-Original | Phase | Kompetenzbereiche | Status |
|---|---|---|---|---|
| 9 | `FLP_Deutsch_Gym_swd.pdf` | Sek I | 5 (Sprechen/Zuhören, Schreiben, Lesen, Texte/Medien, Sprache) | vollständig |
| 10 | dito | Einführungsphase | 5 | vollständig |
| 11 | dito | Qualifikationsphase 11/12 | 5 (gAN + eAN) | vollständig |
| 12 | dito | Qualifikationsphase 11/12 (Verweis auf Kl. 11) | 5 (Verweis) | vollständig (als Verweis-Datei) |

**Hinweis Klasse 12:** Der Lehrplan führt 11/12 als gemeinsame Qualifikationsphase ohne separates Kap. 3.5.3. Die Datei `klasse_12.md` ist daher als Verweis auf `klasse_11.md` implementiert und ergänzt ausschließlich Abiturprüfungs-relevante Rahmungen (Kurshalbjahre, schriftliche/mündliche Abiturprüfung). Die Inhalte sind nicht dupliziert, um keine Halluzinationen zu erzeugen.

**Hinweis Operatorenliste:** Im bereitgestellten Lehrplan ist keine formale Operatorenliste mit Zuordnung zu Anforderungsbereichen (AFB I/II/III) enthalten. In den Beispiel-Klausuren / Klassenarbeiten ist die AFB-Zuordnung daher als didaktisch ergänzt markiert.

### Evangelische Religion — Sekundarschule

| Klasse | Lehrplan-Original | Lehrplan-Struktur | Kompetenzbereiche | Kompetenzschwerpunkte | Status |
|---|---|---|---|---|---|
| 5 | `lp_sks_evrel_01_08_2019.pdf` | Doppeljahrgang 5/6 | 5 (Wahrnehmung/Darstellung, Deutung, Beurteilung, Kommunikation/Dialog, Gestaltung) | 6 (Anthropologie, Theologie, Christologie, Ethik, KG/Ekklesiologie, Eschatologie) | vollständig |
| 6 | dito | Doppeljahrgang 5/6 (deckungsgleich) | 5 | 6 (deckungsgleich) | vollständig |
| 7 | dito | Doppeljahrgang 7/8 | 5 | 5 (Anthropologie: Partnerschaft, Theologie, Christologie, Ethik, Eschatologie) | vollständig |
| 8 | dito | Doppeljahrgang 7/8 (deckungsgleich) | 5 | 5 (deckungsgleich) | vollständig |
| 9 | dito | Doppeljahrgang 9/10 | 5 | 5 (Anthropologie, Theologie, Christologie, Ethik, Eschatologie) | vollständig |
| 10 | dito | Doppeljahrgang 9/10 (deckungsgleich) | 5 | 5 (deckungsgleich) | vollständig |

### Evangelische Religion — Gymnasium

| Klasse | Lehrplan-Original | Phase | Kompetenzbereiche | Kompetenzschwerpunkte | Status |
|---|---|---|---|---|---|
| 9 | `FLP_EvangRU_Gym_01082022_swd.pdf` | Sek I | 5 | 6 (alle Schwerpunkte) | vollständig |
| 10 | dito | Einführungsphase | 5 | 2 (Ethik, Eschatologie) — Gelenkfunktion | vollständig |
| 11 | dito | Qualifikationsphase 11/12 | 5 | 4 (Anthropologie, Christologie, Theologie, Ekklesiologie) | vollständig |
| 12 | dito | Qualifikationsphase 11/12 (deckungsgleich) | 5 | 4 (deckungsgleich) | vollständig |

**Hinweis Klasse 11/12:** Der Lehrplan führt die Qualifikationsphase 11/12 zusammen; beide Dateien dokumentieren denselben Stand.

**Hinweis Operatorenliste:** Auch im Ev. RU-Lehrplan ist keine formale Operatorenliste mit AFB-Zuordnung ausgewiesen.

## Cross-Skill-Abdeckung (Beispiele)

| Beispiel | Lehrplanbasis | Phase | Datei |
|---|---|---|---|
| Stoffverteilungsplan Deutsch Kl. 7 | Sekundarschule | Doppeljahrgang 7/8 | `examples/deutsch_klasse_07_stoffverteilungsplan_sekundarschule.md` |
| Klassenarbeit Deutsch Kl. 9 | Sekundarschule | RSA/HSA 9 | `examples/deutsch_klasse_09_klassenarbeit_sekundarschule.md` |
| Klausur Deutsch Kl. 11 | Gymnasium | Qualifikationsphase | `examples/deutsch_klasse_11_klausur_gymnasium.md` |
| Unterrichtsreihe Ev. Religion Kl. 6 | Sekundarschule | Doppeljahrgang 5/6 | `examples/religion_klasse_06_unterrichtsreihe_sekundarschule.md` |
| Mündliche Prüfung Ev. Religion Kl. 10 | Gymnasium | Einführungsphase | `examples/religion_klasse_10_muendliche_pruefung_gymnasium.md` |
| Sitzplan (fachunabhängig) | beliebig | beliebig | `examples/sitzplan_beispiel.md` |

## Lücken / unsichere Stellen

| Stelle | Befund | Maßnahme |
|---|---|---|
| Deutsch Kl. 12 Gym — separate Inhalte | nicht im Lehrplan ausgewiesen (Qualifikationsphase gemeinsam) | `klasse_12.md` als Verweis auf `klasse_11.md`; Abiturprüfungs-Rahmung didaktisch ergänzt |
| Ev. Religion Kl. 11/12 Gym — Einzeljahrtrennung | nicht im Lehrplan ausgewiesen | beide Dateien dokumentieren denselben Stand; kein Konflikt |
| Operatorenliste mit AFB-Zuordnung | im bereitgestellten Lehrplan (beide Fächer) nicht enthalten | in Beispielen didaktisch ergänzt + explizit markiert (Ebene 2) |
| Konkrete Abiturprüfungsformate | nicht im Lehrplan; Oberstufenverordnung maßgeblich | in `klasse_12.md` und in der Klausur-Datei Hinweis auf Oberstufenverordnung |
| Gymnasialer Zweig Kl. 5–8 an Gemeinschaftsschule | nicht im Skill abgedeckt — laut Routing Kl. 5–8 = Sekundarschule | dokumentiert in `input_issues.md`; Erweiterung möglich |
| Fächerübergreifende Bezüge im Lehrplan Ev. RU Gym | in `klasse_10.md` ausgewiesen; in Sek I nur teilweise | dokumentiert in jeweiligen Curriculum-Dateien |

## Nicht im Skill abgedeckt (bewusst dokumentiert)

- Katholischer Religionsunterricht (kein Lehrplan bereitgestellt)
- Ethik (kein Lehrplan bereitgestellt)
- Klasse 1–4 / 13
- Andere Bundesländer
- Rein fachspezifische Sekundarschul- oder Gymnasium-Anfragen ohne Gemeinschaftsschul-Kontext (Routing technisch möglich, aber Skill ist auf Gemeinschaftsschule fokussiert)