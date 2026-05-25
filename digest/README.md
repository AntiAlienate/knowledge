# Auto-Accumulated Finds

Daily digests of fresh PA-related material from zero-auth public sources, pushed automatically by the AntiAlienate knowledge-base agent each loop tick.

## Sources polled

- **PubMed** — clinical & academic research (E-utilities API, no key required)
- **CrossRef** — academic papers with DOI metadata (no key)
- **BAILII** — recent UK/IE court decisions (scrape-friendly recent-decisions page)

## File format

`YYYY-MM-DD-finds.md` — one digest per day, organised by source, with full citation + URL per item.

## Verification

These are **research leads** auto-pulled by keyword match. Verify against primary source before relying on any specific item for advocacy or legal use.

## Future sources

When access becomes available:
- CourtListener (needs free API token)
- HUDOC (JS-rendered, needs different scraping approach)
- OpenAlex, Indian Kanoon, CanLII

## Generator

Script: `/tmp/.aa-secrets/accumulator.py` (host machine — not in repo). Runs each loop tick. Idempotent — dedupes against `known-finds.json`.

---

— Curated by Alan Markson · [AntiAlienate.com](https://www.antialienate.com) · CC BY 4.0
