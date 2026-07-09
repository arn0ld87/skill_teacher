# Workflow: Mündliche Prüfung

## Zweck
Erstellt Prüfungsformat, Aufgabenstellung, Erwartungshorizont und Bewertungskriterien für eine mündliche Prüfung in Deutsch oder Ev. Religion — von der mündlichen Leistungsüberprüfung im Regelunterricht (Kl. 5–10) bis zur mündlichen Abiturprüfung/Präsentationsprüfung (Kl. 11–12, als Annahme gekennzeichnet, da schulformspezifisch unterschiedlich geregelt).

## Eingaben
Pflicht:
- Fach (Deutsch oder Ev. Religion)
- Klassenstufe
- Anlass (reguläre mündliche Note, Ersatzleistung, Prüfungsteil des Abschlussverfahrens, Abiturprüfung)
- Thema/Themenbereich

Optional (mit Annahme bei Fehlen):
- Prüfungsdauer — ohne Angabe: Richtwert nach Anlass (Regelunterricht ca. 5–10 Min., Abschluss-/Abiturprüfung ca. 15–20 Min.) als Annahme
- Prüfungsform (Einzelprüfung, Prüfungsgespräch mit Vorbereitungszeit, Präsentation mit Kolloquium) — ohne Angabe: Prüfungsgespräch mit kurzer Vorbereitungszeit annehmen
- Hilfsmittel — ohne Angabe: Standardhilfsmittel des Fachs (z. B. Textausgabe, Bibel) annehmen und kennzeichnen

Fehlt die Klassenstufe komplett, RÜCKFRAGE stellen — Prüfungsformat und Anforderungsniveau sind bildungsgangspezifisch.

## Vorgehen
1. Bildungsgang-Prüfung durchführen (siehe unten) und Kopf-Kennzeichnung festlegen.
2. Anlass klären: reguläre mündliche Leistungsfeststellung vs. formeller Prüfungsteil — daraus ergeben sich unterschiedliche Formstrenge und Dokumentationspflicht.
3. Lehrplanabschnitt(e) identifizieren, aus denen sich Thema und erwartetes Anforderungsniveau ableiten.
4. Aufgabenstellung formulieren: klare Fragestellung oder Impuls, ggf. mit Textgrundlage/Material für Vorbereitungszeit.
5. Anforderungsbereiche zuordnen (AFB I–III), Operatoren passend zum mündlichen Format wählen (z. B. „erläutern", „begründen", „Stellung nehmen").
6. Erwartungshorizont skizzieren: mögliche Antwortaspekte, keine abschließende Musterlösung bei offenen Aufgaben.
7. Bewertungskriterien festlegen: fachliche Richtigkeit, Argumentationsqualität, sprachliche Darstellung, Gesprächsverhalten — mit Gewichtung.
8. Ablauf beschreiben: Vorbereitungszeit, Prüfungsgespräch, ggf. Nachfragen, Protokollierung.
9. Differenzierungshinweis ergänzen, sofern Nachteilsausgleich neutral/funktional angesprochen werden muss (keine Diagnose nennen).
10. Quellenbezug (Lehrplanstelle, bei Abiturbezug Hinweis auf EPA-Orientierung als Annahme) anfügen.
11. Qualitätscheck durchführen, Ausgabe formatieren.

## Bildungsgang-Prüfung
- Klasse 5–8: Lehrplanbasis Sekundarschule, reguläre mündliche Leistungsfeststellung.
- Klasse 9–10: Bildungsgang klären. Sekundarschulabschluss/mittlerer Schulabschluss → mündliche Prüfung ggf. Teil des Abschlussverfahrens (Annahme, Ebene 3, da konkrete Prüfungsordnungsdetails nicht im Repository hinterlegt sind). Gymnasialer Bildungsgang → Klasse 10 ist Einführungsphase, kein Abiturbezug, aber ggf. Vorbereitung auf spätere Präsentationsprüfung.
- Klasse 11–12: nur Gymnasium, Qualifikationsphase, Abiturbezug wahrscheinlich. Mündliche Abiturprüfung bzw. Präsentationsprüfung als Annahme kennzeichnen (Ebene 3) — genaue Prüfungsordnung ist schulform-/landesspezifisch und nicht abschließend im Repository hinterlegt, daher „noch zu prüfen" (Ebene 4) für Verfahrensdetails.
- Bei unklarem Bildungsgang in Kl. 9–10: Rückfrage stellen ODER sichtbar markierte Annahme (Sekundarschule).
- Routing-Details siehe `routing_rules.json` und `bildungsgang_guardrails.md` — insbesondere die Klasse-10-Sonderregel.

## Lehrplanbezug
Herangezogen werden `data/curriculum/deutsch/` bzw. `data/curriculum/religion/`, Unterordner nach Bildungsgang (`sekundarschule/` oder `gymnasium/`), für die passende Klassenstufe. Bei Fach Ev. Religion gilt: nur evangelischer RU. Die Lehrplanbasis wird im Ausgabekopf ausgewiesen. Prüfungsformale Vorgaben (Dauer, Gewichtung, Zulassungsbedingungen) sind kein Lehrplaninhalt und werden konsequent als Annahme (Ebene 3) oder offen (Ebene 4) markiert, nicht als direkter Lehrplanbezug (Ebene 1).

## Ausgabeformat
Kopfzeile: `Schulform: Gemeinschaftsschule | Bildungsgang: <…> | Lehrplanbasis: <…>`
Danach: Thema, Klassenstufe, Anlass, Dauer, Hilfsmittel.
Abschnitt Aufgabenstellung (inkl. Material bei Vorbereitungszeit).
Abschnitt Erwartungshorizont (Kurzfassung, mit AFB-Zuordnung).
Abschnitt Bewertungskriterien (Tabelle: Kriterium | Gewichtung | Beschreibung).
Abschnitt Ablauf.
Abschnitt Differenzierungshinweis (falls relevant).
Abschnitt Quellenbezug.
Kein dediziertes Template für mündliche Prüfungen unter `templates/` vorhanden — Erwartungshorizont-Teil an `templates/erwartungshorizont.md`, Bewertungsteil an `templates/bewertungsraster.md` anlehnen.

## Qualitätscheck
- Lehrplanbasis im Kopf ausgewiesen, Bildungsgang bei Kl. 9–10 geklärt oder als Annahme markiert?
- Prüfungsformale Annahmen (Dauer, Ablauf, Abiturbezug) klar als Ebene 3/4 gekennzeichnet, nicht als Lehrplanbezug ausgegeben?
- Operatoren korrekt dem AFB zugeordnet und mündlich umsetzbar formuliert?
- Bewertungskriterien vollständig, Gewichtung nachvollziehbar?
- Quellen (Lehrplandatei, Fach, Klasse, Abschnitt) genannt?
- Keine echten Schülernamen, keine Diagnosen bei Differenzierungshinweisen (funktional formuliert)?
- Abiturbezug nur erwähnt, wenn explizit angefragt oder aus Kontext eindeutig?

## Beispielprompt
„Erstelle eine mündliche Prüfung für Ev. Religion, Klasse 10, gymnasialer Bildungsgang (Einführungsphase), zum Thema Theodizeeproblem, mit Vorbereitungszeit, Erwartungshorizont und Bewertungskriterien."
