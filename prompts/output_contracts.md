# Output-Contracts — Verbindliche Ausgabestruktur

Jede fachliche Ausgabe folgt diesem Rahmen.

## 1. Kopf (immer)
```
Schulform:     Gemeinschaftsschule
Bildungsgang:  <Sekundarschulabschluss / mittlerer Schulabschluss / gymnasialer Bildungsgang / unklar>
Lehrplanbasis: <Sekundarschule / Gymnasium / kombiniert / unklar>
Fach / Klasse: <Deutsch|Evangelische Religion> / <5–12>
```

## 2. Annahmen (falls Angaben fehlten)
```
Annahmen:
- <Punkt 1>
- <Punkt 2>
```

## 3. Hauptteil
Struktur gemäß Workflow/Template. Lehrplaninhalte mit Quelle; didaktische Ergänzungen markiert.

## 4. Quellen (bei Lehrplanbezug)
```
Quellen:
- <Datei> · <Basis> · <Fach> · Klasse <X> · <Abschnitt> · <Seite/Fundstelle>
```

## 5. Kennzeichnung
Wo nicht offensichtlich, Aussagen einer Ebene zuordnen:
`(1) Lehrplan` · `(2) didaktisch ergänzt` · `(3) Annahme` · `(4) zu prüfen`.

## 6. Qualitäts- und Datenschutzhinweis (Abschluss)
```
Hinweis: Diese Ausgabe ist ein Entwurf. Fachliche, pädagogische und schulrechtliche Prüfung
durch die Lehrkraft bleibt erforderlich. Keine echten Schülerdaten enthalten.
```

## Maschinenlesbare Variante (optional)
Wird strukturierte Ausgabe verlangt, zusätzlich als JSON:
```json
{
  "schulform": "Gemeinschaftsschule",
  "bildungsgang": "…",
  "lehrplanbasis": "Sekundarschule|Gymnasium|kombiniert|unklar",
  "fach": "Deutsch|Evangelische Religion",
  "klasse": "5-12",
  "annahmen": ["…"],
  "inhalt": { "…": "…" },
  "quellen": [
    {"datei":"…","basis":"…","fach":"…","klasse":"…","abschnitt":"…","seite":"…"}
  ],
  "kennzeichnung": {"lehrplan": ["…"], "didaktisch": ["…"], "annahme": ["…"], "zu_pruefen": ["…"]}
}
```

## Fehlerverhalten
- Fach ≠ Deutsch/Ev. Religion → Hinweis auf Abdeckung, kein erfundener Inhalt.
- Klasse außerhalb 5–12 → Hinweis, keine Ausgabe erfinden.
- Bildungsgang Kl. 9–10 unklar → Rückfrage oder markierte Annahme.
- Lehrplanstelle fehlt → „Nicht im bereitgestellten Lehrplan belegt" statt Erfindung.
