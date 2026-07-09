# Workflow: Klausur (Oberstufe, Qualifikationsphase)

## Zweck
Erstellt eine Oberstufen-Klausur für Deutsch oder Evangelische Religion (Klasse 11–12, gymnasialer Bildungsgang, Qualifikationsphase) inklusive Aufgabenstellung, Operatoren, Anforderungsbereichen (AFB I–III), Punkteverteilung, Erwartungshorizont und Bewertungsschlüssel. Abgrenzung zu `klassenarbeit.md`: Klausuren sind grundsätzlich Gymnasium-FLP, näher an EPA-Logik und Abiturvorbereitung.

## Eingaben
Pflicht:
- Fach (Deutsch oder Ev. Religion)
- Thema/Unterrichtsreihe, aus der die Klausur hervorgeht
- Klassenstufe (11 oder 12) bzw. Kurs (grundlegendes/erhöhtes Anforderungsniveau, falls zutreffend)
- Bearbeitungsdauer

Optional (mit Annahme bei Fehlen):
- Kursart (GK/LK bzw. grundlegend/erhöht) — ohne Angabe: Annahme „grundlegendes Anforderungsniveau", sichtbar markiert (Ebene 3)
- Aufgabenanzahl/-typ — ohne Angabe: eine Aufgabe mit Teilaufgaben, orientiert an gängigem Klausurformat des Fachs
- Hilfsmittel (Textausgabe, Wörterbuch, Bibel) — ohne Angabe: Standardhilfsmittel des Fachs annehmen und kennzeichnen
- Abiturbezug (ja/nein) — ohne Angabe: keine explizite Abiturprüfungssimulation, nur EPA-orientierte Aufgabenkultur

Fehlt die Klassenstufe komplett, RÜCKFRAGE stellen — Klausuren sind bildungsgangspezifisch und ohne Stufenangabe nicht sauber verortbar.

## Vorgehen
1. Bildungsgang-Prüfung durchführen (siehe unten) und Kopf-Kennzeichnung festlegen.
2. Lehrplanabschnitt(e) aus `data/curriculum/<fach>/gymnasium/klasse_11.md` bzw. `klasse_12.md` identifizieren, die zum Thema passen.
3. Aufgabenformat wählen: klassische Textaufgabe mit Teilaufgaben (Deutsch: Analyse/Interpretation/Erörterung; Religion: Text-/Bildanalyse, Positionsentwicklung).
4. Operatoren aus dem Fach-Operatorenkatalog des Anforderungsbereichs zuordnen (AFB I: nennen/beschreiben, AFB II: erklären/analysieren, AFB III: erörtern/beurteilen/gestalten).
5. Teilaufgaben formulieren, jeweils mit Operator, AFB-Zuordnung, Punktzahl.
6. Bewertungsschlüssel festlegen (i. d. R. Punkte → Note nach Notenschlüssel des Bundeslands bzw. schulinternem Fachschaftsbeschluss; falls unbekannt, Standard-Punkte-Noten-Tabelle als Annahme kennzeichnen).
7. Erwartungshorizont skizzieren (Kurzfassung inline; für Details auf `erwartungshorizont.md`-Workflow verweisen).
8. Differenzierungshinweis ergänzen (z. B. Wortschatzhilfen, Strukturierungshilfe für Aufgabe 1 bei Bedarf) — kurz, ohne Diagnosebezug.
9. Quellenbezug (Lehrplanstelle, ggf. EPA-Hinweis) anfügen.
10. Qualitätscheck durchführen, Ausgabe formatieren.

## Bildungsgang-Prüfung
Klausuren sind ausschließlich Gymnasium-Format (Qualifikationsphase). Zu klären:
- Klasse 11 oder 12 → beides ist Gymnasium-Qualifikationsphase, kein Sekundarschulbezug möglich (Sekundarschule endet nach Klasse 10).
- Falls versehentlich Klasse 9 oder 10 angegeben wird: prüfen, ob gymnasialer Bildungsgang vorliegt. Klasse 10 im gymnasialen Bildungsgang = Einführungsphase, noch keine Klausur im Qualifikationsphasen-Sinn — Rückfrage, ob „Klausur" oder „Test/Kursarbeit der Einführungsphase" gemeint ist.
- Bei Klasse 9–10 im Sekundarschul-Bildungsgang: Klausur-Format ungeeignet, stattdessen auf `klassenarbeit.md` verweisen.
- Routing-Details siehe `routing_rules.json` und `bildungsgang_guardrails.md` — dort ist die Klasse-10-Sonderregel (Einführungsphase vs. Sekundarschulabschlussjahr) verbindlich hinterlegt.

## Lehrplanbezug
Herangezogen wird ausschließlich `data/curriculum/<fach>/gymnasium/klasse_11.md` bzw. `klasse_12.md`. Bei Fach Ev. Religion gilt: nur evangelischer RU, kein katholischer RU und keine Ethik-Lehrplaninhalte. Die Lehrplanbasis wird im Ausgabekopf ausgewiesen (Schulform, Bildungsgang, Lehrplanbasis). Bei Abiturbezug zusätzlich Hinweis, dass die EPA (Einheitliche Prüfungsanforderungen Abitur) als Orientierungsrahmen für Aufgabenkultur dient, nicht als eigene Datenquelle im Repository.

## Ausgabeformat
Kopfzeile: `Schulform: Gemeinschaftsschule | Bildungsgang: Gymnasium | Lehrplanbasis: Gymnasium`
Danach: Thema, Klassenstufe/Kurs, Dauer, Hilfsmittel.
Aufgabenteil: nummerierte Aufgaben/Teilaufgaben mit Operator, AFB, Punkten.
Abschnitt Erwartungshorizont (Kurzfassung).
Abschnitt Bewertungsschlüssel (Punkte-Noten-Tabelle).
Abschnitt Differenzierungshinweis.
Abschnitt Quellenbezug.
Kein dediziertes Klausur-Template unter `templates/` vorhanden — Struktur an `templates/stundenentwurf.md` (Formatierungslogik) orientieren, bis ein `klausur.md`-Template ergänzt wird.

## Qualitätscheck
- Lehrplanbasis im Kopf ausgewiesen (Gymnasium, Klasse 11/12)?
- Bildungsgang-Klärung dokumentiert, insbesondere bei Klasse 9–10-Grenzfällen?
- Alle Aussagen mit Vier-Ebenen-Kennzeichnung (1 Lehrplan direkt / 2 didaktisch ergänzt / 3 Annahme / 4 noch zu prüfen) versehen, wo relevant?
- Operatoren korrekt dem AFB zugeordnet?
- Punktesumme und Bewertungsschlüssel schlüssig?
- Quellen (Lehrplandatei, Abschnitt, ggf. EPA-Hinweis) genannt?
- Keine personenbezogenen Daten, keine Schülernamen?
- Abiturbezug nur erwähnt, wenn explizit angefragt oder aus Kontext eindeutig?

## Beispielprompt
„Erstelle eine 90-minütige Deutsch-Klausur für Klasse 12 (grundlegendes Anforderungsniveau) zum Thema Lyrikinterpretation im Kontext von Naturlyrik, mit Erwartungshorizont und Punkteschlüssel."
