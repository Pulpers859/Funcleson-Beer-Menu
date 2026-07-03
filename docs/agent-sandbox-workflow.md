# Agent Sandbox Workflow

Use a detached agent sandbox when an AI agent needs to explore risky or creative changes without mutating the main checkout.

## Default Rule

Normal work still happens on `main`. This repo remains main-only: do not create side branches, push sandbox commits, or open PRs unless Patrick explicitly asks for that workflow.

For risky experiments, create a detached worktree:

```powershell
.\tools\New-AgentSandbox.ps1 -Name menu-layout
```

Review the sandbox diff, then integrate only selected changes back into the main checkout:

```powershell
git -C "C:\Dev\Funcleson Video Board-agent-sandboxes\menu-layout" diff
```

Remove the sandbox when finished:

```powershell
.\tools\Remove-AgentSandbox.ps1 -NameOrPath menu-layout
```

## Use A Sandbox For

- Competing TV menu-board layouts.
- Google Sheets CSV parsing or fallback behavior changes.
- Untappd ticker, photo album, QR, or Spotify integration experiments.
- Changes that would be hard to visually compare inside one `index.html`.

## Skip A Sandbox For

- Tiny copy changes.
- Single-value CSS tweaks.
- Documentation-only edits that do not change operating rules.

The sandbox is for isolation, not final delivery. Final visual/browser validation, commit, and push happen from `C:\Dev\Funcleson Video Board` on `main`.
