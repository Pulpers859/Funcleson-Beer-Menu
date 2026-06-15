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
- Working branch: `main`
- Fetch and sync before normal work

## Rules
- Use `main` as the only normal working and push branch.
- Do not create side branches.
- Do not open or rely on pull requests.
- Only use another branch if the user explicitly asks for one in that session.
- If you make code or tracked-file changes, you must commit them and push them to `origin/main` before ending the task unless the user explicitly tells you not to.
- Do not leave code changes only in the local working tree when the intended outcome is for the repo to stay current across machines.
- Fix root causes, not surface symptoms
- Large media files (.afdesign, .png posters, PDFs) live in the directory but are NOT tracked in git
- The app is one self-contained HTML file — preserve that architecture unless there's a strong reason to split
- Display target is a TV via Yodeck — test for that viewport
- If the user references prior work from another AI agent, another machine, another terminal, or another conversation, do not assume the visible diff or latest local commit tells the whole story.
- Before making new edits, rebases, resets, merges, or sync claims in that situation, perform an external-agent reconciliation pass.
- Reconciliation pass requirements:
  - Inspect any outside artifact the user provides, such as a transcript, chat export, screenshot, commit list, or claimed fix summary.
  - Compare each claimed change against the current local files, the local git history, and the current `main` branch on GitHub.
  - Tell the user plainly whether each claimed change is present, missing, partially landed, or overwritten.
  - Only after that comparison should you decide whether to pull, rebase, merge, patch missing work, or leave newer work intact.
  - Do not say the repo is fully assessed or in sync until this reconciliation step is complete whenever outside-agent work is part of the context.

## Structure
- `index.html` — the live app (self-contained HTML/CSS/JS)
- `assets/qr/Funcleson-Funkatorium-QR-Code.PNG` — QR code used by the app (referenced in index.html)
- `prototypes/` — style experiments (jukebox variants, untappd ticker)
- `support/` — non-runtime project material
- `support/docs/` — reference PDFs and guides (not tracked in git)
- `support/beer-posters/` — poster designs (not tracked in git)
- `support/reference-assets/photo-drop-qr.png` — tracked reference image, not part of the live board
