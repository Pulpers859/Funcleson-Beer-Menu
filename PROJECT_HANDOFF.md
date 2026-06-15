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
- If you make code or tracked-file changes, commit them and push them to `origin/main` before ending the task unless the user explicitly tells you not to.
- Do not leave intended repo updates only on the local machine.
- Do not create side branches or PR-based workflows unless the user explicitly asks for them.
- If the user references prior work by another AI agent, another machine, another terminal, or another conversation, do not assume the current diff or latest visible commit tells the full story.
- Before making new edits, rebases, resets, merges, or sync claims in that case, perform an external-agent reconciliation pass:
  - Inspect any outside artifact the user provides, such as a transcript, chat export, screenshot, commit list, or claimed fix summary.
  - Compare what that agent claimed to change against the current local files, the local git history, and the current `main` branch on GitHub.
  - Tell the user plainly whether each claimed change is present, missing, partially landed, or overwritten.
  - Only after that comparison should you decide whether to pull, rebase, merge, patch missing work, or leave newer work intact.
  - Do not say the repo is fully assessed or in sync until this reconciliation step is complete whenever outside-agent work is part of the context.

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
- If you make code or tracked-file changes, commit them and push them to `origin/main` before ending the task unless the user explicitly says not to.
- Do not create side branches and do not use PRs unless the user explicitly requests that workflow.
- Use the standard workflow: investigate, fix root causes, audit adjacent risks, handle Git.
- Before starting normal work, fetch from origin and sync the active branch first.
- If outside-agent work is referenced, perform an external-agent reconciliation pass before new edits, rebases, resets, merges, or sync claims.
```
