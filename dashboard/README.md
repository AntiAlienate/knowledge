# AntiAlienate Mission Control

Single-page mission-control dashboard for the AntiAlienate operational loop.

## What it shows

- **Overview** — repo entries, jurisdictions covered, FB posts shipped, videos, research entries, ECHR cluster size; live recent-commits and recent-actions feeds
- **Knowledge Graph** — full-bleed force-directed graph of 80+ nodes (jurisdictions, statutes, ECHR cases, research anchors, treaties) with drag, zoom, pan, hover tooltips, fit/reseed/pause controls
- **Action Log** — live tail of every commit, FB post, video push, and queue update from `/tmp/.aa-secrets/action-log.jsonl`
- **Backfill** — vault → repo migration progress (30/65)
- **Wiki + Case Law** — jurisdiction coverage grid, ECHR standalones, research entries
- **Alan Videos** — file table from `/Users/mada/AntiAlienate-videos/`
- **Facebook Queue** — posted history, last-post timestamp, next eligible (1/hour rate-limit)
- **Live Commits** — last 15 commits on `main` with clickable SHAs
- **Quotas + Health** — HeyGen credits, FB token status, Gemini image-gen, cron expiry
- **Mission Brief** — full 5-vector mission statement

## Running locally

Open `dashboard/app.html` directly in a browser. No build step. All data inlined into the single HTML file as a `DATA` constant.

```bash
open dashboard/app.html
```

## Re-generating with fresh data

Re-running the operational loop regenerates the HTML with the latest counters and feed snapshots. The graph data is hand-curated for the topology view; counters and tables are auto-baked.

## GitHub Pages

To serve via Pages: enable Pages on `main` branch, `/dashboard` directory. URL will be:

```
https://antialienate.github.io/antialienate-knowledge/
```

## Action log format

`/tmp/.aa-secrets/action-log.jsonl` — one JSON object per line:

```json
{"t": "2026-05-18 11:02", "kind": "commit", "msg": "case-law(sa): KSA PSL 2022", "sha": "7ff946d"}
{"t": "2026-05-18 10:55", "kind": "fb", "msg": "FB posted #79 weaponized-therapy", "id": "1066...292114"}
```

Kinds: `commit`, `fb`, `video`, `queue`, `err`, `info`.

Append via `/tmp/.aa-secrets/log-action.py <kind> <msg> [k=v ...]`.
