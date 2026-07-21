# Marketing Klausur – Interaktives Lerntool

Interaktive Lern-App für die Marketing-Klausur (FAU): Themenmodule mit
Fortschrittstracking, ein Rechen-Trainer für die klausurrelevanten
Aufgabentypen, ein MC-Selbsttest, Karteikarten und interaktive Diagramme.

Die App ist eine einzelne, abhängigkeitsfreie HTML-Datei (`index.html`) —
identisch zum Original, ergänzt um eine dünne PWA-Hülle, damit sie sich wie
eine App auf dem iPad installieren lässt.

## Auf dem iPad installieren

1. Die Seite in **Safari** öffnen (die GitHub-Pages-URL, siehe unten).
2. Auf das **Teilen**-Symbol tippen.
3. **„Zum Home-Bildschirm"** auswählen.
4. Die App erscheint danach als eigenes Icon und startet im Vollbild
   (ohne Safari-Leiste), inkl. Offline-Zugriff dank Service Worker.

## Lokal öffnen

Einfach `index.html` in einem Browser öffnen — keine Build-Schritte, kein
Server nötig.

## Deployment (GitHub Pages)

Der Workflow [`.github/workflows/deploy.yml`](.github/workflows/deploy.yml)
deployed den Inhalt dieses Repos bei jedem Push auf `main` automatisch nach
GitHub Pages.

Einmalig muss in den Repo-Einstellungen unter **Settings → Pages** als
**Source** „**GitHub Actions**" ausgewählt werden. Danach läuft jeder Push
auf `main` automatisch durch und die App ist unter der von GitHub
angezeigten Pages-URL erreichbar.

## Projektstruktur

| Datei | Zweck |
|---|---|
| `index.html` | Die App (1:1 Original-Inhalt + PWA-Meta-Tags) |
| `manifest.json` | Web-App-Manifest (Name, Icons, Standalone-Modus) |
| `sw.js` | Service Worker fürs Offline-Caching |
| `icons/`, `apple-touch-icon.png` | App-Icons für Home-Bildschirm |
| `.github/workflows/deploy.yml` | GitHub Pages Auto-Deployment |
