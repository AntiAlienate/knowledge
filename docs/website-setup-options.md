# Website Deployment — knowledge.antialienate.com + command.antialienate.com

This repo is configured to build a static MkDocs Material site (`mkdocs.yml`) and to deploy via any of three hosts. Pick the one you prefer.

## What's been committed

| File | Purpose |
|---|---|
| `mkdocs.yml` | Static-site config (theme, nav, plugins, exclusions) |
| `requirements.txt` | Python deps (`mkdocs`, `mkdocs-material`, `awesome-pages`) |
| `.github/workflows/docs.yml` | Build + deploy workflow (one of three targets) |
| `firebase.json` | Firebase Hosting two-target config (knowledge + command) |
| `.firebaserc` | Firebase project pointer |
| `CNAME` | Custom-domain pointer for GitHub Pages path |

The build step always runs. The deploy step depends on a repo variable `DEPLOY_TARGET`.

## Option A — Cloudflare Pages (simplest, single-vendor with your existing DNS)

**Recommended.** Cloudflare-DNS + Cloudflare-Pages = one console; no manual CNAME juggling.

**Setup once:**
1. Cloudflare dashboard → **Workers & Pages** → Create application → Pages → Connect to Git
2. Select `AntiAlienate/antialienate-knowledge` → branch `main`
3. Build settings: Build command `pip install -r requirements.txt && mkdocs build --site-dir _site`, build output `_site`
4. Pages assigns `antialienate-knowledge.pages.dev`
5. Custom domain → add `knowledge.antialienate.com` → Cloudflare auto-creates the CNAME because you own the DNS
6. For the dashboard: create a second Pages project, build output `dashboard/`, custom domain `command.antialienate.com`

**Repo settings to add:**
- Repo variable: `DEPLOY_TARGET = cloudflare`
- Repo secret: `CF_API_TOKEN` (create at Cloudflare → My Profile → API Tokens → "Edit Cloudflare Workers" template)
- Repo secret: `CF_ACCOUNT_ID` (Cloudflare dashboard → right sidebar)

**CNAMEs you add manually:** none needed — Cloudflare auto-handles them in the Pages flow.

## Option B — Firebase Hosting (Google Cloud, via ICOS)

**If you prefer the Google stack** and ICOS already has Firebase project access.

**Setup once (you or ICOS):**
1. Firebase Console → Create project `antialienate-knowledge` (or use existing)
2. Enable Hosting → add two sites: `antialienate-knowledge` + `antialienate-command`
3. Generate service-account key (Project Settings → Service Accounts → Generate new private key → JSON)
4. Add Firebase Hosting custom domain in Firebase Console for each subdomain
5. Firebase provides A records (typically `151.101.x.x` Fastly CDN) — add those in Cloudflare DNS

**Repo settings to add:**
- Repo variable: `DEPLOY_TARGET = firebase`
- Repo secret: `FIREBASE_SERVICE_ACCOUNT_KEY` (paste the JSON)

**CNAMEs / A records you add in Cloudflare (after Firebase custom-domain wizard):**

| Subdomain | Record | Target |
|---|---|---|
| `knowledge` | A | `151.101.1.195` |
| `knowledge` | A | `151.101.65.195` |
| `command` | A | `151.101.1.195` |
| `command` | A | `151.101.65.195` |

(Firebase will show you the actual exact A records to use when you add the custom domain — copy from there. Set proxy status OFF (DNS only, grey cloud) initially so Firebase can verify; can be re-enabled after SSL issues.)

## Option C — GitHub Pages (no extra vendor)

**Simplest, but only supports one custom domain per repo.**

**Setup once:**
1. Repo Settings → Pages → Source: GitHub Actions
2. Add CNAME file at repo root with `knowledge.antialienate.com` (already done)
3. Workflow auto-deploys

**Repo settings to add:**
- Repo variable: `DEPLOY_TARGET = github-pages` (or leave unset — this is default)

**CNAME you add in Cloudflare:**

| Subdomain | Record | Target |
|---|---|---|
| `knowledge` | CNAME | `antialienate.github.io` (proxy: OFF) |

For `command.antialienate.com` you'd need a separate repo or a different host — GitHub Pages can't serve two custom domains per repo.

## What to tell me to proceed

1. **Pick A, B, or C.**
2. **If A**: add the CF_API_TOKEN + CF_ACCOUNT_ID secrets, set DEPLOY_TARGET=cloudflare, then click Save in Pages. I'll watch the deploy.
3. **If B**: confirm the Firebase project name (default `antialienate-knowledge`); paste the service-account JSON to a vault key I can read. I'll handle the rest.
4. **If C**: enable Pages in Settings, set DEPLOY_TARGET=github-pages. Live in ~3 min.

Once you pick + complete the per-option setup, the site goes live on the next push to `main`.
