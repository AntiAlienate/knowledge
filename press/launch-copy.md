# Launch Copy — HackerNews, Reddit, X/Twitter, LinkedIn

Pre-drafted copy for the public launch. Sequence: HN first (decide what to post in the first 60 min of US morning, ideally Tue–Thu), then Reddit within 2 hours, then X/Twitter thread, then LinkedIn.

---

## HackerNews

**Title** (max 80 chars):
```
Show HN: Open-source knowledge base for parental alienation
```

**Self-text body**:
```
Hi HN — we've been building the largest open-source reference on
parental alienation: case law, research, playbooks, jurisdiction guides,
and templates, all free under CC BY 4.0.

Repo: github.com/AntiAlienate/antialienate-knowledge

What's there:
- 9 step-by-step playbooks (first 90 days, court prep, reunification
  therapy, teen cases, cross-border/Hague, accused-of-alienation,
  grandparent dynamics, working with a lawyer, documentation)
- 30 jurisdiction reference pages
- ~60 recent cross-jurisdiction rulings
- 9 profile pages on the field's leading clinicians and researchers
- 9 templates (letters, court bundle structures, prep briefs)
- 38 shareable reference cards
- An auto-accumulator polling PubMed, CrossRef, CourtListener, BAILII,
  Reddit every 25 min, pushing a daily digest

Why open source? Because the existing references in this field are
scattered across paywalled academic journals, $200/month legal
databases, and forum posts of variable accuracy. Targeted parents,
their lawyers, and the clinicians supporting them all deserve a
common starting point.

Happy to answer questions about the architecture (Python + GitHub
Contents API + scheduled cron + LLM-curated content with human review)
or the substance.

PRs welcome — especially translations, jurisdictional additions, and
corrections from clinicians whose work is referenced.
```

---

## Reddit

### r/opensource
**Title**: `Launched: Open-source knowledge base for parental alienation — CC BY 4.0`

**Body**: same as HN body, lightly adapted ("Hi r/opensource" opener)

### r/ParentalAlienation
**Title**: `New open-source repo: playbooks, case law, and resources — free, no paywall`

**Body**:
```
Sharing because some of you may find this useful.

We've put together what we believe is the largest open-source reference
on parental alienation. It's free, no signup, no email collection.

Link: github.com/AntiAlienate/antialienate-knowledge

Most directly relevant if you're in the middle of a case:
- /playbooks/first-90-days.md — week-by-week if you've just realised
- /playbooks/court-prep-checklist.md — what to bring, say, avoid
- /playbooks/documentation-system.md — the four-stream approach
- /playbooks/accused-of-alienation.md — if you're the one being accused
- /jurisdictions/ — find your country / state
- /templates/ — court bundle structures, letters, log templates

Everything is CC BY 4.0 — share, adapt, translate, use however you need.

Not affiliated with any legal-service or paid product. Not legal advice.
PRs welcome if you spot errors or gaps.
```

### r/Custody / r/Divorce / r/Divorce_Men
Similar to r/ParentalAlienation but emphasise:
- The documentation system
- The court prep checklist
- The "accused" playbook (relevant in both directions)

---

## X/Twitter thread

```
1/ We just opened the largest open-source knowledge base on parental
   alienation. Free. CC BY 4.0. No paywall.

   github.com/AntiAlienate/antialienate-knowledge

2/ Why open-source? Because the references targeted parents and their
   lawyers need are scattered across paywalled journals, $200/mo legal
   databases, and forum posts of variable accuracy.

3/ What's there:
   - 9 playbooks
   - 30 jurisdiction pages
   - ~60 recent rulings
   - 9 named-clinician profiles
   - 38 reference cards
   - Auto-updated daily digest

4/ The playbooks are step-by-step for parents in crisis:
   • First 90 days
   • Court prep
   • Reunification therapy
   • Teen alienation
   • Documentation system
   • Working with a lawyer
   • Accused of alienation
   • Cross-border / Hague
   • Grandparent dynamics

5/ Auto-accumulator polls PubMed, CrossRef, CourtListener, BAILII,
   Reddit every 25 minutes and pushes fresh findings into /digest/
   daily. The reference grows continuously.

6/ Named in the influencer section (with permission requests outbound):
   Bernet (Vanderbilt), Warshak, Baker, Eddy, Harman, Kruk, Woodall,
   Childress, Lorandos.

7/ Not legal advice. CC BY 4.0. PRs welcome — translations,
   jurisdictional additions, clinician corrections.

   Link again: github.com/AntiAlienate/antialienate-knowledge
```

---

## LinkedIn (professional audience — lawyers, clinicians)

```
We've just released what we believe is the largest open-source knowledge
base on parental alienation — free under CC BY 4.0.

🔗 github.com/AntiAlienate/antialienate-knowledge

For family lawyers, clinicians, and researchers working on cases involving
alienating behaviours, the repository consolidates in one place:

📚 9 practitioner playbooks (first 90 days, court prep, reunification
   therapy, teen cases, Hague Convention abduction, false-accusation
   defence, grandparent dynamics, lawyer engagement, documentation)

⚖️ ~60 cross-jurisdictional rulings (2024–2026)

🌐 30 country / state jurisdiction reference pages

👥 9 profile pages on the field's leading clinicians: Bernet, Warshak,
   Baker, Eddy, Harman, Kruk, Woodall, Childress, Lorandos

📊 A background agent that polls PubMed, CrossRef, CourtListener, BAILII,
   and Reddit every 25 minutes — daily auto-accumulated digest

📝 Court-ready templates and shareable reference cards

The project is licensed CC BY 4.0 — adapt, translate, share, build on.
Pull requests welcome, especially translations and jurisdictional
additions.

Not legal advice. Independent. No paywall, no signup, no email collection.

Tagging colleagues who may find this useful for their work or pass it on
to clients: [add tags]
```

---

## Launch timing

**Optimal HN window**: Tuesday–Thursday, 8:30–10:30am EST (when US tech
audience is online and engagement compounds for the rest of the day).

**Reddit posts**: 1–2 hours after HN. Allows HN traffic to populate the
analytics and the repo to handle initial load.

**Twitter/X**: same window as Reddit, with main thread author tagging
2–3 high-signal accounts in the family-law / open-source spaces.

**LinkedIn**: same day or next morning. Different audience cadence.

**Avoid**: Fri afternoon, Mon morning, US public holidays, AU/NZ holidays.

---

## Pre-launch checklist

- [ ] Repo top-level README polished (last reviewed today)
- [ ] License file present (CC BY 4.0 confirmed)
- [ ] No broken internal links
- [ ] /press/ folder visible and indexed
- [ ] Top-level CONTRIBUTING.md exists or pointed to
- [ ] Maintainer contact email visible
- [ ] One named author byline (Alan Markson) on all curated material
- [ ] Influencer outreach Tier 1 emails sent 48h before launch
- [ ] Backup distribution lined up (paid wire on standby if organic flat)
