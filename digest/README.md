# Auto-Accumulated Finds

Daily digests of fresh PA-related material from public legal-research sources, pushed automatically by the AntiAlienate knowledge-base agent each loop tick.

## Sources polled (each tick)

| Source | Coverage | Auth |
|---|---|---|
| **PubMed** (E-utilities) | Clinical & academic research | none |
| **CrossRef** REST | Academic papers + DOI metadata | none |
| **CourtListener** | US federal + state appellate opinions | account |
| **BAILII** recent-decisions | UK/IE family-court rulings | none (scrape) |

## File format

`YYYY-MM-DD-finds.md` — one digest per day, organised by source, with full citation + URL per item. Re-runs append new items + skip dupes via `known-finds.json`.

## Verification

These are **research leads** auto-pulled by keyword match. Verify against primary source before relying on any specific item for advocacy or legal use.

## Future sources (when access available)

- **HUDOC** — JS-rendered, needs Playwright-style scraping
- **OpenAlex** — academic graph
- **Indian Kanoon**, **CanLII** — same scrape-friendly model as BAILII
- **EUR-Lex** — EU legal database (has API)

## Generator

Script: `/tmp/.aa-secrets/accumulator.py` (host machine — not in repo). Runs each loop tick. Idempotent — dedupes against `known-finds.json`. Sources extensible via `def {source}_search(...)` plumbing.

---

— Curated by Alan Markson · [AntiAlienate.com](https://www.antialienate.com) · CC BY 4.0
