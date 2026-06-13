# Funcleson Video Board — Project Handoff

## Project Identity
- Project name: `Funcleson Video Board`
- Project type: `web app (single-page HTML beer menu board)`
- Source-of-truth repo path: `C:\Dev\Funcleson Video Board`
- Stale/old copies to ignore: none
- Primary target for normal work: `index.html` (the beer menu board)
- GitHub remote: `https://github.com/Pulpers859/Funcleson-Beer-Menu.git`

## Repo State
- Stable branch: `main`
- Working branch: `main`
- Expected default branch for normal work: `main`
- Sync-first rule: Before normal work, fetch from the remote first. If the working tree is clean and the active branch tracks the expected upstream, pull with --ff-only before editing.

## Architecture / Product Notes
- Main product purpose: Digital beer menu board for Funcleson Funkatorium, displayed on a TV/monitor via Yodeck
- Key files: `index.html` (the entire app — HTML/CSS/JS in one file)
- Runtime asset: `assets/qr/Funcleson-Funkatorium-QR-Code.PNG`
- Data source: Google Sheets CSV (fetched at runtime for beer list)
- Features: beer menu columns, Untappd check-in ticker, photo album, QR code, Spotify jukebox integration
- Display target: TV/monitor via Yodeck video board system
- Supplementary files:
  - `support/beer-posters/` — poster designs (.afdesign/.png), not tracked in git
  - `support/docs/` — PDF/docx guides, not tracked in git
  - `support/reference-assets/photo-drop-qr.png` — tracked reference image, not used by the live board

## How The Agent Should Operate
- Inspect before assuming.
- Work in the source-of-truth repo only.
- Sync from GitHub before normal work.
- Fix root causes, not surface symptoms.
- Be honest and direct.
- Prefer architecture/data-flow fixes over hacks.
- Handle Git operations when appropriate.
- Keep normal work on `main`.
- Do not create side branches or PR-based workflows unless the user explicitly asks for them.

## Communication Style
- Warm, collaborative, calm, disciplined
- High-effort and thoughtful
- Short progress updates while working
- Clear reasoning, no fluff, no fake certainty

## Post-Fix Audit Standard
After making changes, do a harsh pass focused on:
- root-cause completeness
- adjacent fragility
- architecture quality
- silent failure risk
- maintainability

## Project-Specific Instructions For The Next Agent
```text
Project: Funcleson Video Board
Active repo path: C:\Dev\Funcleson Video Board
GitHub remote: https://github.com/Pulpers859/Funcleson-Beer-Menu.git
Stable branch: main
Working branch: main

Important:
- The entire app is a single index.html file with inline CSS/JS.
- It fetches beer data from a Google Sheets CSV at runtime.
- The display target is a TV/monitor via Yodeck — optimize for that viewport.
- Runtime QR image now lives under `assets/qr/`.
- Large media files (beer posters, PDFs) live under `support/` and are NOT tracked in git.
- Use `main` as the only normal branch for commits and pushes.
- Do not create side branches and do not use PRs unless the user explicitly requests that workflow.
- Use the standard workflow: investigate, fix root causes, audit adjacent risks, handle Git.
- Before starting normal work, fetch from origin and sync the active branch first.
```
