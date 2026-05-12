# claudebridge-dashboard

Portfolio Control Centre for paul-pc (core controller across the R.T. Keedwell / ML2 portfolio).

## What this repo is

A GitHub-Pages-hosted static dashboard plus a scheduled rebuild workflow. The dashboard summarises state across the nine workstreams paul-pc coordinates: FastForward, Gallowfell, RTK SharePoint, ML2 Consulting, Dropship, Hollow Kin, Nestwell, operational data, and ClaudeBridge itself.

## Pages

`docs/index.html` is the seed. GitHub Pages is configured to serve from `/docs` on `main`, so the dashboard URL is `https://gonzo8285.github.io/claudebridge-dashboard/`.

## Rebuild workflow

`.github/workflows/rebuild.yml` runs on a schedule, polls commit metadata for each project repo, and regenerates `docs/index.html`. Currently a placeholder — the actual rebuild script will land in the next pass.

## Sources of truth

- Memory at `C:\Users\Paul McCann\AppData\Roaming\Claude\local-agent-mode-sessions\...\memory\` (paul-pc-local)
- ClaudeBridge file tree at `G:\My Drive\ClaudeBridge\` (paul-pc + ff-151 shared)
- The five other Gonzo8285 repos (one per project)

## Cadence

Mon / Wed / Fri 18:00 UK — `pulse-housekeep` generates a docx + pdf + html status pack to `G:\My Drive\ClaudeBridge\shared\status\portfolio\` and commits the html slice to this repo so the latest is always live.

## Naming

Five rationalised entities Paul standardised on 2026-05-12:

- **PPC** = paul-pc (this controller, on Paul's main machine)
- **151** = ff-151 (on 192.168.0.151, FastForward build owner)
- **Claude Code** = the heartbeat process committing to Gonzo8285/MobileGame
- **Three pulses** = pulse-build / pulse-gamedev / pulse-housekeep — the rationalised heartbeat surface
- **Bridge** = the G:\My Drive\ClaudeBridge\ tree
