# Workflow: Sitzplan

## Zweck
Erstellt einen begründeten Sitzplan für eine Klasse oder einen Kurs — als Tabelle und als ASCII-Raumplan. Ziel: Arbeitsruhe sichern, Konflikte entschärfen, Förderbedarfe berücksichtigen, ohne Schüler zu stigmatisieren oder echte Namen zu verwenden.

## Eingaben
Pflicht:
- Klasse/Kurs (z. B. "7b") und Fach, falls fachspezifisch (z. B. Sitzordnung nur für Deutschunterricht)
- Anzahl Schüler
- Raumform (Reihen, U-Form, Gruppentische, Blockanordnung) — falls unbekannt: Annahme "Reihenform mit Paartischen" markieren

Optional:
- Konflikte zwischen Schülern (neutral beschrieben, z. B. "K1 und K2 lenken sich gegenseitig ab")
- Freundschaften/Trennwünsche (z. B. "S3 und S4 sollen getrennt sitzen")
- Förderbedarf, funktional/beobachtungsbasiert (z. B. "benötigt Blickkontakt zur Tafel", "braucht ruhige Randposition")
- Sehstärke/Hörbeeinträchtigung (rein funktional, keine Diagnose)
- Vorgabe zur Anzahl gewünschter Varianten

Fehlen Angaben zu Konflikten/Förderbedarf: Sitzplan wird ohne Sonderregeln erstellt, das wird im Kopf der Ausgabe vermerkt ("keine Angaben zu Konflikten/Förderbedarf — Standardverteilung").

**Datenschutz-Pflicht:** Es werden ausschließlich Kürzel oder Pseudonyme verwendet (S1, S2, … oder frei wählbare Pseudonyme wie "Mia K."→"M.K."). Werden echte Vor-/Nachnamen übergeben, sofort durch Kürzel ersetzen und den User darauf hinweisen, dass Klarnamen aus der Ausgabe entfernt wurden.

## Vorgehen
1. Eingaben auf echte Namen prüfen, ggf. zu Kürzeln anonymisieren und Hinweis ausgeben.
2. Raumform und Platzzahl festlegen; bei Bedarf beschriftetes Rastermodell aufbauen (Zeilen × Spalten oder Gruppentische).
3. Fixpunkte setzen: Förderbedarfe mit Sitzposition verknüpfen (z. B. vorne/Rand/Fensterseite), Trennwünsche als harte Constraints behandeln.
4. Konfliktpaare räumlich entzerren (nicht nebeneinander, nicht in Sichtlinie bei Ablenkungsmustern).
5. Restliche Plätze so verteilen, dass Arbeitsruhe und Durchmischung (nicht nur Freundeskreise) gewahrt bleiben.
6. Drei Varianten erzeugen (A/B/C) mit unterschiedlichem Schwerpunkt, z. B.:
   - Variante A: Ruhe/Konfliktvermeidung im Vordergrund
   - Variante B: Durchmischung/Zusammenarbeit im Vordergrund
   - Variante C: Kompromiss aus A und B
7. Für jede Variante eine kurze pädagogische Begründung (2–4 Sätze) formulieren.
8. Tabelle und ASCII-Raumplan pro Variante erzeugen.
9. Qualitätscheck durchführen (siehe unten) und Ausgabe zusammenstellen.

## Bildungsgang-Prüfung
Für Sitzpläne ist der Bildungsgang in der Regel irrelevant, da es sich um eine organisatorische, nicht lehrplanbezogene Maßnahme handelt. Ausnahme: Kurse in Klasse 9–10, die nach Bildungsgang getrennt unterrichtet werden (z. B. äußere Fachleistungsdifferenzierung) — hier den Kurs klar benennen (z. B. "Deutsch G-Kurs 9" vs. "Deutsch E-Kurs 9"), damit der Sitzplan zum richtigen Kurs passt. `routing_rules.json` wird nur konsultiert, wenn die Klassenzusammensetzung selbst vom Bildungsgang abhängt (Kurssystem Klasse 9/10). Für Klasse 11–12 gilt automatisch Gymnasium/Kurssystem (Qualifikationsphase) — dort ist statt "Klasse" der Kursname anzugeben.

## Lehrplanbezug
Kein Lehrplanbezug. Sitzpläne sind eine klassenorganisatorische Maßnahme ohne fachdidaktischen Inhalt; `data/curriculum/`-Dateien werden nicht herangezogen. Ausnahme: Wird der Sitzplan explizit für eine bestimmte Unterrichtsform (z. B. Gruppenarbeit zu einem Lehrplanthema) erstellt, kann im Freitext ein kurzer Verweis auf die betreffende Unterrichtsreihe erfolgen — das ersetzt keine Lehrplanquelle und wird nicht mit der Vier-Ebenen-Kennzeichnung versehen.

## Ausgabeformat
Kein dediziertes Template in `templates/` vorhanden — Ausgabe folgt fixem Format:

1. Kopfzeile: Klasse/Kurs, Fach (falls fachspezifisch), Datum, Raumform, Anzahl Schüler, Hinweis auf Anonymisierung.
2. Pro Variante (A/B/C):
   - Tabelle: Platznummer | Kürzel | Begründung (falls Sonderregel greift, sonst leer)
   - ASCII-Raumplan, Beispiel für 24 Schüler, Reihenform mit Paartischen, Blickrichtung Tafel oben:

```
                    [ TAFEL / LEHRERPULT ]

   Reihe 1:   [S01][S02]   [S03][S04]   [S05][S06]
   Reihe 2:   [S07][S08]   [S09][S10]   [S11][S12]
   Reihe 3:   [S13][S14]   [S15][S16]   [S17][S18]
   Reihe 4:   [S19][S20]   [S21][S22]   [S23][S24]

              Fenster ->                <- Tür
```

   - Kurzbegründung (2–4 Sätze)
3. Abschlussabsatz: Empfehlung, welche Variante als Startpunkt geeignet ist, und Hinweis, dass Lehrkraft die finale Freigabe hat.

## Qualitätscheck
- Ausschließlich Kürzel/Pseudonyme verwendet, keine Klarnamen
- Alle übergebenen Trennwünsche als harte Constraints eingehalten
- Förderbedarfe funktional/neutral formuliert, keine Diagnosebegriffe
- Keine Schuldzuweisung bei Konfliktbeschreibung
- ASCII-Plan und Tabelle stimmen in der Platzzahl überein
- Jede Variante hat eine nachvollziehbare pädagogische Begründung
- Hinweis auf fehlenden Lehrplanbezug vorhanden (kein Lehrplanbezug-Fall)
- Datenschutz-Hinweis sichtbar, falls ursprünglich Klarnamen übergeben wurden

## Beispielprompt
"Erstell mir einen Sitzplan für die 7b, 22 Schüler, Reihenform mit Paartischen. S1 und S2 lenken sich gegeneinander ab, S5 braucht wegen Sehschwäche einen Platz vorne. S3 und S4 wollen nicht nebeneinander sitzen. Bitte drei Varianten."
