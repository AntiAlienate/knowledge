# Website Setup Options — knowledge.antialienate.com

> **Status:** Staging documentation. Awaiting maintainer decision on path before any infrastructure is committed. No external publication or DNS change has happened.

The repository's 70+ markdown pages should be reachable at `knowledge.antialienate.com` as a navigable knowledge hub. Two paths.

---

## Path A — GitHub Pages with Jekyll (fastest)

**Setup time:** ~30 minutes.
**Cost:** $0.
**What you get:** Auto-published static site from the markdown files. Default theme renders the README and section files.

**Steps:**
1. Enable GitHub Pages: Settings → Pages → Source: `main` branch, `/` (root)
2. Pick a Jekyll theme: Settings → Pages → Theme: Cayman / Minimal / Hacker / etc.
3. Add a `CNAME` file at repo root containing the single line: `knowledge.antialienate.com`
4. DNS at antialienate.com registrar: add a CNAME record `knowledge` → `antialienate.github.io`
5. Wait ~5 min for DNS + GitHub provisioning. Set "Enforce HTTPS" once available.

**Pros:** No build pipeline needed. Markdown files in the repo serve directly. Minimum surface area.

**Cons:** Navigation is weak for 70+ pages — Jekyll's default themes give you the README as the homepage and require manual front-matter and `_config.yml` to build a proper sidebar/nav. Search is non-existent without third-party plugin (e.g., lunr.js). The aesthetic is functional, not polished.

**Best for:** "Live this week, polish later."

---

## Path B — MkDocs Material on GitHub Pages (recommended)

**Setup time:** ~3-4 hours.
**Cost:** $0.
**What you get:** A first-class documentation site — full-text search, sidebar TOC, mobile nav, dark mode, breadcrumbs, mobile-first responsive design, tag system. The standard tool for reference content (used by Anthropic, Stripe, FastAPI, hundreds of major OSS projects).

**Steps:**
1. Add `mkdocs.yml` at repo root configuring:
   - `site_name: AntiAlienate Knowledge`
   - `site_url: https://knowledge.antialienate.com`
   - `theme: material` + nav structure mirroring our 14 sections
   - `docs_dir: .` (use existing markdown files in-place) OR move content under `/docs/` (cleaner but requires updating all internal links)
   - Search, dark mode, social-card generation enabled
2. Add `.github/workflows/docs.yml` — GitHub Actions workflow that runs `mkdocs build` on push to `main` and deploys to `gh-pages` branch
3. Settings → Pages → Source: `gh-pages` branch
4. Add `CNAME` file at root: `knowledge.antialienate.com`
5. DNS at registrar: CNAME `knowledge` → `antialienate.github.io`
6. Wait ~10 min for first GitHub Actions run + provisioning

**Pros:** Production-quality reference site. Search across all pages out of the box. Navigation auto-generated from `mkdocs.yml` nav tree. Loads fast. Looks credible to press, journalists, lawyers, parents alike. Mobile-friendly.

**Cons:** Requires `mkdocs.yml` to be hand-crafted; if we use `docs_dir: .` then files like `MEMORY.md` need explicit `not_in_nav` exclusion; existing internal markdown links should be tested (most will work but some need adjustment).

**Best for:** Long-term reference site. Worth doing right.

---

## Path C — Cloudflare Pages from GitHub source (alternative deploy host)

Same MkDocs Material setup but deployed via Cloudflare Pages instead of GitHub Pages.
- Cloudflare's CDN is faster globally
- Better analytics out of the box
- Same cost ($0 on free tier)
- Same CNAME approach for `knowledge.antialienate.com` (or use Cloudflare-managed DNS)

Choose this if you want better edge performance and analytics. Otherwise GitHub Pages is fine.

---

## What I need from you to proceed

1. **Path preference**: A (Jekyll fast), B (MkDocs done right), or C (MkDocs on Cloudflare Pages)?
2. **DNS access**: Can you add the CNAME at the antialienate.com registrar, or do you want a written set of instructions you'll forward to whoever holds it?
3. **Homepage**: Should `knowledge.antialienate.com/` show the existing repo README as the landing page, or do you want a redesigned landing-page-style index optimized for first-time visitors (probably worth doing — the README is great for GitHub but a landing page should be shorter and more visual)?

Once those are answered I'll commit the config files in one PR and walk you through the DNS step.

---

## What stays in scope of the knowledge hub website

Public sections worth surfacing on the site:
- Top-level README (recast as landing page)
- /playbooks/ (12 step-by-step guides)
- /case-studies/ (24 deep case investigations)
- /evidence/ (PA-as-child-abuse evidence base)
- /the-debate/ (recognition vs critique)
- /glossary/
- /influencers/ (19 profile pages)
- /community/ (advocacy orgs international)
- /resources/ (research databases + key books)
- /jurisdictions/ (30 jurisdiction pages)
- /landmark-cases/, /case-law/, /research/
- /open-source/infographics/ (38 shareable cards)
- /publishers/
- /tools/legal-research.md

## What stays OUT

- /press/ (internal staging only — pre-distribution)
- /digest/ (auto-accumulator output; could be linked but not featured)
- Any working files like CONTRIBUTING.md (linked from footer not nav)

---

*Reviewed: 2026-05-25. Open a PR or just message back with your choice and I'll execute.*
