# Input-Issues — Auffälligkeiten der Eingabedaten

## Zusammenfassung
Fünf lesbare PDF-Lehrpläne bereitgestellt, alle korrekt einer Basis/Fach zugeordnet. Keine
unlesbaren oder doppelten Dateien. Strukturelle Abweichungen von der Auftragsannahme sind unten
dokumentiert; keine blockiert die Erstellung.

## Befunde

### 1. Nur Evangelische Religion (kein katholischer RU, keine Ethik)
Alle Religions-PDFs sind **Evangelischer Religionsunterricht** (`lp_sks_evrel…`, `FLP_EvangRU…`).
Der Skill deckt „Religion" ausschließlich als **Evangelische Religion** ab. Pfad `religion/` bleibt,
Inhalt ist durchgängig als Ev. Religion gekennzeichnet.
→ Auswirkung: `Religion Klasse X` wird als Ev. Religion behandelt; andere Konfessionen/Ethik → Hinweis.

### 2. Doppeljahrgangs-Struktur der Lehrpläne
Die Lehrpläne differenzieren nicht nach Einzelklasse, sondern nach Doppeljahrgängen
(5/6, 7/8) bzw. Phasen (11/12 = Qualifikationsphase). Die geforderten Einzelklassen-Dateien
(`klasse_05.md` … `klasse_12.md`) wurden angelegt; jede markiert sichtbar den zugrundeliegenden
Doppeljahrgang/die Phase und den Hinweis, dass keine Einzeljahrestrennung erfolgt.

### 3. Einführungsphase = Klasse 10 (nicht 11)
In Sachsen-Anhalt ist die gymnasiale **Einführungsphase Klasse 10**. Das Routing weicht daher von
der Auftragsvorlage ab: Bei gymnasialem Bildungsgang zählt bereits Klasse 10 zur Oberstufe.
Dokumentiert in `routing_rules.json` und `bildungsgang_guardrails.md`.

### 4. Sekundarschule endet Klasse 10
Es existieren keine Sekundarschul-Lehrpläne für 11/12. Für diese Jahrgänge ist ausschließlich der
Gymnasial-Fachlehrplan maßgeblich. (Auftrag bereits konsistent.)

### 5. Gymnasial-FLPs decken 5–12 ab
Beide Gymnasial-Fachlehrpläne enthalten auch 5/6 und 7/8. Für die Gemeinschaftsschule werden aus
ihnen nur 9–12 übernommen (5–8 laufen über die Sekundarschule). Die Gym-Anteile 5–8 sind im Skill
nicht als eigene Dateien hinterlegt; bei Bedarf im gymnasialen Zweig Kl. 5–8 wäre eine Ergänzung nötig.

### 6. PDF-Extraktion
`pdftotext -layout` meldete „Bad annotation destination"-Warnungen (defekte interne Verlinkungen im
PDF); der Textinhalt wurde vollständig extrahiert. Kein Datenverlust erkennbar.

## Offene Prüfpunkte
- Exakte Seitenzahlen der Fundstellen sind teils nur über das Inhaltsverzeichnis annähernd zuordenbar.
- Ob im gymnasialen Zweig der Gemeinschaftsschule auch Kl. 5–8 nach Gym-FLP unterrichtet werden soll,
  ist organisatorisch zu klären (aktuell: 5–8 = Sekundarschule).
