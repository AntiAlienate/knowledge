# Auto-Accumulated Finds

Daily digests of fresh PA-related material from public legal-research sources, pushed automatically by the AntiAlienate knowledge-base agent each loop tick.

## Sources polled (each tick)

| Source | Coverage | Auth |
|---|---|---|
| **[PubMed](https://pubmed.ncbi.nlm.nih.gov/)** (E-utilities) | Clinical & academic research | none |
| **CrossRef** REST | Academic papers + DOI metadata | none |
| **CourtListener** | US federal + state appellate opinions | account |
| **[BAILII](https://www.bailii.org/)** recent-decisions | UK/IE family-court rulings | none (scrape) |

## File format

`YYYY-MM-DD-finds.md` — one digest per day, organised by source, with full citation + URL per item. Re-runs append new items + skip dupes via `known-finds.json`.

## Verification

These are **research leads** auto-pulled by keyword match. Verify against primary source before relying on any specific item for advocacy or legal use.

## Future sources (when access available)

- **[HUDOC](https://hudoc.echr.coe.int/)** — JS-rendered, needs Playwright-style scraping
- **OpenAlex** — academic graph
- **Indian Kanoon**, **[CanLII](https://www.canlii.org/)** — same scrape-friendly model as [BAILII](https://www.bailii.org/)
- **EUR-Lex** — EU legal database (has API)

## Generator

Script: `/tmp/.aa-secrets/accumulator.py` (host machine — not in repo). Runs each loop tick. Idempotent — dedupes against `known-finds.json`. Sources extensible via `def {source}_search(...)` plumbing.

---

— Curated by Alan Markson · [AntiAlienate.com](https://www.antialienate.com) · CC BY 4.0
















































































































<!-- AA-CITE-START -->

---

## Sources & authoritative references

**Referenced in this page:**

- [DSM-5-TR (APA)](https://www.appi.org/products/dsm)
- [ICD-11 (WHO)](https://icd.who.int/)

**Topic baseline (independently verifiable):**

- [AntiAlienate Knowledge Base](https://knowledge.antialienate.com/)
- [DSM-5-TR (APA)](https://www.appi.org/products/dsm)
- [ICD-11 (WHO)](https://icd.who.int/)
- [HCCH — Hague Conference](https://www.hcch.net/)
- [Council of Europe](https://www.coe.int/)

<!-- AA-CITE-END -->

<!-- AA-CROSSLINK-START -->

---

## Related on antialienate.com

- [Are Fathers Discriminated Against In Family Court](https://www.antialienate.com/blog/are-fathers-discriminated-against-in-family-court)
- [How To File Ethics Malpractice Complaint Therapist Psychologist](https://www.antialienate.com/blog/how-to-file-ethics-malpractice-complaint-therapist-psychologist)
- [How To File Police Report Custody Dispute Belgium](https://www.antialienate.com/blog/how-to-file-police-report-custody-dispute-belgium)
- [Parental Alienation Scope History Future](https://www.antialienate.com/blog/parental-alienation-scope-history-future)
- [Who Is Antialienate For](https://www.antialienate.com/blog/who-is-antialienate-for)

<!-- AA-CROSSLINK-END -->
