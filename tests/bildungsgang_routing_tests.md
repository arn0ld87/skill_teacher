# Bildungsgang-Routing-Tests

Input: Deutsch Klasse 7, Stoffverteilungsplan.
Erwartung: Sekundarschule (Lehrplanbasis Sekundarschule Klasse 5–8).

Input: Religion Klasse 8, Unterrichtsreihe.
Erwartung: Sekundarschule (Lehrplanbasis Sekundarschule Klasse 5–8).

Input: Deutsch Klasse 9, Klassenarbeit, kein Bildungsgang angegeben.
Erwartung: Rückfrage nach Bildungsgang oder sichtbar markierte Annahme (Ebene 3), keine stille Wahl.

Input: Deutsch Klasse 9, Bildungsgang Sekundarschulabschluss/mittlerer Abschluss.
Erwartung: Sekundarschule.

Input: Deutsch Klasse 10, gymnasialer Bildungsgang.
Erwartung: Gymnasium, Einführungsphase.

Input: Deutsch Klasse 10, kein Bildungsgang angegeben.
Erwartung: Rückfrage nach Bildungsgang oder sichtbar markierte Annahme (Ebene 3), da Klasse 10 sowohl Sekundarschul- als auch gymnasialer Einführungsphase zugeordnet sein kann.

Input: Deutsch Klasse 11, Klausur.
Erwartung: Gymnasium, Qualifikationsphase.

Input: Religion Klasse 12, Abiturvorbereitung.
Erwartung: Gymnasium mit explizitem Abiturbezug.

Input: Deutsch Klasse 12, ohne Angabe "Abitur".
Erwartung: Gymnasium, Qualifikationsphase (Sekundarschule existiert für Klasse 11–12 nicht).

Input: Religion Klasse 13.
Erwartung: Hinweis, dass nur Klasse 5–12 abgedeckt ist, keine Ausgabe.

Input: Deutsch Klasse 5, keine weitere Angabe.
Erwartung: Sekundarschule (Klasse 5–8 primär Sekundarschule, keine Rückfrage nötig).
