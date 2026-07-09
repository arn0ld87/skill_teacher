# Routing-Prompt — Fach / Klasse / Bildungsgang / Lehrplanbasis bestimmen

Ziel: Vor jeder fachlichen Ausgabe die **Lehrplanbasis** eindeutig festlegen. Grundlage:
`data/curriculum/routing_rules.json`.

## Ablauf
1. **Fach** erkennen. Nur `Deutsch` oder `Evangelische Religion`. Sonst Hinweis auf Grenzen.
2. **Klasse** erkennen (5–12). Außerhalb → Hinweis: „Nur Klasse 5–12 abgedeckt."
3. **Bildungsgang** bestimmen:
   - Klasse **5–8** → Lehrplanbasis **Sekundarschule** (keine Rückfrage nötig).
   - Klasse **9–10** → Bildungsgang klären:
     - Sekundarschulabschluss / mittlerer Schulabschluss → **Sekundarschule**
     - gymnasialer Bildungsgang → **Gymnasium** (Klasse 10 = **Einführungsphase**)
     - keine Angabe und kein Oberstufen-/Abiturbezug → **Annahme Sekundarschule**, sichtbar markiert
   - Klasse **11–12** → **Gymnasium** (Qualifikationsphase, Abiturbezug); Sekundarschule existiert hier nicht.
4. **Abitur-/Oberstufen-Trigger** prüfen: Fällt eines der Stichwörter
   (Abitur, Abiturprüfung, Abiturklausur, Qualifikationsphase, Einführungsphase, Oberstufe,
   Kurshalbjahr, gymnasiale Oberstufe), dann Gymnasium-Fachlehrplan zusätzlich/primär und
   Abiturbezug kennzeichnen — unabhängig von einer sonst angenommenen Basis.
5. **Lehrplanbasis ausweisen** (Sekundarschule / Gymnasium / kombiniert / unklar) und die passenden
   `data/curriculum/…`-Dateien laden.

## Annahmen offen nennen (Beispielblock)
```
Annahme:
- Schulform: Gemeinschaftsschule
- Klasse: 8
- Bildungsgang: nicht gesondert angegeben
- Lehrplanbasis: Sekundarschule
- Leistungsniveau: mittel
- Dauer: 45 Minuten
```

## Entscheidungslogik (kurz)
| Klasse | Standard-Basis | Rückfrage? | Sonderfall |
|---|---|---|---|
| 5–8 | Sekundarschule | nein | — |
| 9 | Bildungsgang klären | ja | gymn. → Gymnasium |
| 10 | Bildungsgang klären | ja | gymn. → Gymnasium (Einführungsphase) |
| 11–12 | Gymnasium | nein | Qualifikationsphase, Abiturbezug |

Bei „kombiniert" (z. B. binnendifferenzierter Unterricht Kl. 9/10 mit beiden Bildungsgängen):
beide Basen laden und **je Aussage** die Basis kennzeichnen.
