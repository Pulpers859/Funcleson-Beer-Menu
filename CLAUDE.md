# Funcleson Video Board

## Project
- Digital beer menu board for Funcleson Funkatorium
- Single-page HTML app (`index.html`) with inline CSS/JS
- Fetches beer list from Google Sheets CSV at runtime: https://docs.google.com/spreadsheets/d/e/2PACX-1vS8XJ2EmSMTcR_XrbIegnEEZvGCmix6h9EnEgQi-QwUpIM0JQ0GkdtbiD1X5V29gdG_S81hKd3Eh6QA/pubhtml
- Displayed on TV/monitor via Yodeck

## Repo
- Source of truth: `C:\Dev\Funcleson Video Board`
- GitHub: `https://github.com/Pulpers859/Funcleson-Beer-Menu.git`
- Stable branch: `main`
- Working branch: `dev`
- Fetch and sync before normal work

## Rules
- Keep work on `dev`, not `main`
- Fix root causes, not surface symptoms
- Large media files (.afdesign, .png posters, PDFs) live in the directory but are NOT tracked in git
- The app is one self-contained HTML file — preserve that architecture unless there's a strong reason to split
- Display target is a TV via Yodeck — test for that viewport

## Structure
- `index.html` — the live app (self-contained HTML/CSS/JS)
- `Funcleson-Funkatorium-QR-Code.PNG` — QR code used by the app (referenced in index.html)
- `prototypes/` — style experiments (jukebox variants, untappd ticker)
- `docs/` — reference PDFs and guides (not tracked in git)
- `Beer Posters/` — poster designs (not tracked in git)
