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
- Working branch: `dev`
- Expected default branch for normal work: `dev`
- Sync-first rule: Before normal work, fetch from the remote first. If the working tree is clean and the active branch tracks the expected upstream, pull with --ff-only before editing.

## Architecture / Product Notes
- Main product purpose: Digital beer menu board for Funcleson Funkatorium, displayed on a TV/monitor via Yodeck
- Key files: `index.html` (the entire app — HTML/CSS/JS in one file)
- Data source: Google Sheets CSV (fetched at runtime for beer list)
- Features: beer menu columns, Untappd check-in ticker, photo album, QR code, Spotify jukebox integration
- Display target: TV/monitor via Yodeck video board system
- Supplementary files in repo directory (not tracked in git): beer poster designs (.afdesign/.png), PDF guides, photo album assets

## How The Agent Should Operate
- Inspect before assuming.
- Work in the source-of-truth repo only.
- Sync from GitHub before normal work.
- Fix root causes, not surface symptoms.
- Be honest and direct.
- Prefer architecture/data-flow fixes over hacks.
- Handle Git operations when appropriate.
- Keep normal work on `dev`, not `main`.

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
Working branch: dev

Important:
- The entire app is a single index.html file with inline CSS/JS.
- It fetches beer data from a Google Sheets CSV at runtime.
- The display target is a TV/monitor via Yodeck — optimize for that viewport.
- Large media files (beer posters, PDFs) are in the directory but NOT tracked in git.
- Use the standard workflow: investigate, fix root causes, audit adjacent risks, handle Git.
- Before starting normal work, fetch from origin and sync the active branch first.
```
