# MP3 Converter – PWA

Audio-Dateien (WAV, OGG, M4A, FLAC, WebM …) lokal im Browser in MP3 umwandeln.
Keine Uploads, alles läuft auf dem Gerät.

## Dateien
- `index.html` – die App
- `sw.js` – Service Worker (Offline-Funktion)
- `manifest.json` – PWA-Manifest (Installierbarkeit)
- `icon.svg` – App-Icon

**Alle vier Dateien müssen im selben Ordner liegen.**

## Installieren

Wichtig: Eine PWA lässt sich nur über **HTTPS** oder **localhost** installieren –
ein Doppelklick auf `index.html` (file://) reicht NICHT.

### Variante A – GitHub Pages
1. Alle 4 Dateien in ein Repo hochladen
2. Settings → Pages → Branch auswählen → Save
3. Die `https://<name>.github.io/<repo>/`-URL öffnen
4. In der Adressleiste (Chrome/Edge) auf das Installieren-Symbol klicken,
   oder den "Installieren"-Button in der App nutzen

### Variante B – lokal testen
Im Ordner ein Terminal öffnen und:

    python -m http.server 8080

Dann im Browser `http://localhost:8080/` öffnen → installierbar.

## Offline
Beim ersten Laden mit Internet wird der MP3-Encoder (lame.js) gecached.
Danach funktioniert die App komplett offline.
