# Website — Downloads & CV

Statische Website (reines HTML/CSS, keine Frameworks) mit vier Seiten:
`index.html` (Home), `downloads.html`, `cv.html`, `kontakt.html`.

## Vor dem Hochladen: Platzhalter ersetzen

Suche in allen `.html`-Dateien nach `[Platzhalter]`-Text und `[Nachname]` und
ersetze sie durch deine echten Angaben (Name, Bio, E-Mail, LinkedIn,
Publikationstitel, CV-Einträge). Am schnellsten geht das mit "Suchen &
Ersetzen" in einem Code-Editor wie VS Code.

Lege deine PDFs im Ordner `downloads/` ab (siehe `downloads/README.txt`).

## Mit GitHub Pages veröffentlichen

1. Erstelle ein neues **öffentliches** Repository auf GitHub, z. B.
   `dein-github-name.github.io` (dieser exakte Name macht die Seite direkt
   über `https://dein-github-name.github.io` erreichbar — sonst liegt sie
   unter `https://dein-github-name.github.io/repo-name`).

2. Lade alle Dateien aus diesem Ordner in das Repository hoch — entweder per
   Drag & Drop im Browser ("Add file" → "Upload files") oder per Git:

   ```
   git init
   git add .
   git commit -m "Erste Version der Website"
   git branch -M main
   git remote add origin https://github.com/dein-github-name/dein-repo-name.git
   git push -u origin main
   ```

3. Im Repository: **Settings → Pages** → unter "Build and deployment" als
   Source **"Deploy from a branch"** wählen, Branch `main` und Ordner `/root`
   auswählen, speichern.

4. Nach 1–2 Minuten ist die Seite live unter der oben angezeigten URL.

## Lokal testen

Einfach `index.html` per Doppelklick im Browser öffnen — funktioniert auch
ohne Server, da keine Build-Schritte nötig sind.

## Struktur

```
index.html            Home / Kurzprofil
downloads.html     Downloads-Seite: Publikationen, Daten, Code, Materialien
cv.html                 CV / Werdegang
kontakt.html            Kontaktdaten
style.css               Gemeinsames Stylesheet (Farben, Typografie, Layout)
downloads/               Ablageort für PDFs
```

## Design-Hinweise

- Akzentfarbe: gedecktes Petrol/Tanne (`--accent-dark` bis `--accent-pale`
  in `style.css`), zieht sich als "Faden" farblich abgestuft durch alle
  Seiten (sichtbar links neben den Überschriften).
- Schriften: Fraunces (Überschriften), Inter (Fließtext), IBM Plex Mono
  (Jahreszahlen, Labels, Metadaten) — über Google Fonts eingebunden.
- Um die Akzentfarbe zu ändern, reicht es, die Werte von `--accent-dark`,
  `--accent-mid`, `--accent-light`, `--accent-pale` und `--accent-wash` in
  `style.css` anzupassen — alle Farbabstufungen aktualisieren sich dann
  automatisch.
