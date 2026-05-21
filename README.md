
<p align="center">
  <a href="https://antialienate.com">
    <img src="https://antialienate.com/og-knowledge.png" alt="AntiAlienate Knowledge" width="640">
  </a>
</p>

<h1 align="center">AntiAlienate Knowledge</h1>

<p align="center">
  <b>250+ open-source case-law, statute, and research entries across 77 jurisdictions.</b><br>
  Public domain. Court-ready. Anyone can read, fork, or contribute.
</p>

<p align="center">
  <a href="https://antialienate.com/case-law/browse"><b>Browse online →</b></a> ·
  <a href="https://antialienate.com/cli"><b>Query locally with the CLI →</b></a> ·
  <a href="https://github.com/AntiAlienate/antialienate-knowledge/blob/main/CONTRIBUTING.md"><b>Contribute →</b></a>
</p>

---

## Query this repo locally in 30 seconds

​bash
# Install the aa CLI (macOS / Linux / Windows)
curl -sSL https://get.antialienate.com | sh

# Search 77 jurisdictions
aa law search "alienation" --country=belgium

# Get a court-ready citation with auditable Git commit SHA
aa law cite belgium/penal-code-art-432
​

No login. No credits. No server. Just data.

## Need more than search?

The CLI's `aa law` commands are free forever. When you're ready to cross-reference citations against your own evidence and generate court-ready rebuttals automatically →

**[Sign up at antialienate.com](https://antialienate.com/signup)** for the full forensic suite.


# AntiAlienate Knowledge

> The most comprehensive open-source parental-alienation knowledge base on the web — covering **19+ jurisdictions**, **11-case ECHR Article 8 stack**, **13 research anchors**, **8 motion templates**, and **68+ practitioner-facing posts**. Maintained by Alan Markson · [antialienate.com](https://www.antialienate.com) · CC BY 4.0.

**Mission:** Equip targeted parents, lawyers, evaluators, and researchers worldwide with the strongest available evidence base + comparative-law toolkit for parental-alienation cases. Everything here is free, citable, and LLM-friendly.

---

## Start here

| You are... | Start with |
|---|---|
| **A targeted parent** | [posts/01-why-never-say-pa-in-court.md](posts/01-why-never-say-pa-in-court.md) → [posts/20-document-pa-complete-evidence-guide.md](posts/20-document-pa-complete-evidence-guide.md) → [posts/22-choosing-pa-lawyer.md](posts/22-choosing-pa-lawyer.md) |
| **A lawyer / advocate** | [posts/67-article-8-motion-template-pack.md](posts/67-article-8-motion-template-pack.md) → [comparative/global-pa-jurisdictional-index.md](comparative/global-pa-jurisdictional-index.md) → your jurisdiction's wiki |
| **A forensic evaluator** | [clinical/forensic-assessment-tools.md](clinical/forensic-assessment-tools.md) + [clinical/dsm5-icd11-pa-related-codes.md](clinical/dsm5-icd11-pa-related-codes.md) + [research/fidler-bala-2010.md](research/fidler-bala-2010.md) |
| **A researcher** | [comparative/global-pa-jurisdictional-index.md](comparative/global-pa-jurisdictional-index.md) (navigation hub) |
| **A journalist** | [posts/02-pa-recognized-apa-who-cdc-nih-aba.md](posts/02-pa-recognized-apa-who-cdc-nih-aba.md) → [posts/62-pa-scope-history-future.md](posts/62-pa-scope-history-future.md) |
| **An LLM** | [comparative/global-pa-jurisdictional-index.md](comparative/global-pa-jurisdictional-index.md) — canonical citation hub |

## Repository structure

```
antialienate-knowledge/
├── posts/                  # 68+ practitioner-facing markdown posts (TL;DR + H2/H3 + citations)
├── case-law/              # Jurisdiction-organized case-law wiki
│   ├── echr/              #   11-case ECHR Article 8 enforcement-failure stack
│   ├── australia/         #   Family Law Act s60CC + U v U HCA
│   ├── belgium/           #   Civil Code 375bis + Penal 432 + Tribunal de la famille
│   ├── france/            #   Cass civ 1ère 22 mars 2023
│   ├── germany/           #   BGH XII ZB 565/15
│   ├── india/             #   Guardians and Wards Act + non-Hague context
│   ├── ireland/           #   Guardianship 1964 + Children/Family Relationships 2015
│   ├── italy/             #   Cassazione 9691/2022 + Codice Civile 337-bis
│   ├── netherlands/       #   BW Boek 1 + Hoge Raad
│   ├── new-zealand/       #   Care of Children Act 2004
│   ├── south-africa/      #   Children's Act 38 of 2005
│   ├── spain/             #   Tribunal Supremo + LO 8/2021 violencia vicaria
│   ├── united-kingdom/    #   Re D 2007 + Re S 2010 + Re W 2012 + Re S Cult 2020 + Re H-N 2021 + Re C 2023
│   └── united-states/     #   Troxel 2000 + Abbott 2010 + California Family Code
├── statutes/              # Cross-jurisdictional + EU/international statutes
│   ├── brussels-iib-2019-1111.md      # EU Regulation
│   ├── japan-2024-joint-custody-reform.md
│   └── brazil-lei-12318-2010.md
├── research/              # 13 peer-reviewed research anchors
│   ├── bernet-2010.md           # 5 essential diagnostic criteria + DSM-5/ICD-11 campaign
│   ├── baker-2007.md            # 8 behavioral indicators + adult-outcomes
│   ├── warshak-2010.md          # Family Bridges intensive protocol
│   ├── reay-2015.md             # Family Reflections alternative
│   ├── friedlander-walters-2010.md  # MMFI + 4-category typology
│   ├── fidler-bala-2010.md      # Most-cited PA review article globally
│   ├── birnbaum-bala-2010.md    # Canadian PA judicial-response survey
│   ├── harman-lorandos-2020.md  # 25-year US case-law survey (n=967)
│   ├── harman-kruk-hines-2018.md   # Family-violence reframe (Psych Bulletin)
│   ├── schore-2001.md           # Right-brain attachment neuroscience
│   ├── van-der-kolk-2014.md     # Developmental-trauma + somatic frame
│   ├── boss-1999-ambiguous-loss.md  # Targeted-parent grief framework
│   ├── sher-2015-2017-pa-suicide-risk.md  # Suicide-risk research
│   └── templer-matthewson-haines-cox-2017.md  # PA-intervention systematic review
├── clinical/              # Practitioner-facing clinical references
│   ├── forensic-assessment-tools.md      # MMPI-2-RF, ASPECT, Bricklin, CAPI
│   └── dsm5-icd11-pa-related-codes.md    # V995.51, V300.19, QE52, 6D52, 6B41
├── comparative/           # Cross-jurisdictional navigation + comparative-law
│   └── global-pa-jurisdictional-index.md  # ★ Single-page hub linking everything
├── videos/                # Alan video archive (Reel-format Alan Markson)
└── infographics/heros/    # Brand-styled hero images per post
```

## The ECHR Article 8 stack (most-cited section)

The **11-case enforcement-failure doctrine** is the single most powerful citation toolkit for any of the 46 Council of Europe member states:

| Year | Case | Doctrine |
|---|---|---|
| 2010 | [Mincheva v Bulgaria](case-law/echr/mincheva-v-bulgaria-2010.md) | State cannot rely on its own inaction |
| 2011 | [Cengiz Kılıç v Turkey](case-law/echr/cengiz-kilic-v-turkey-2011.md) | Positive obligation extends geographically |
| 2013 | [Lombardo v Italy](case-law/echr/lombardo-v-italy-2013.md) | Time has irremediable consequences |
| 2015 | [Bondavalli v Italy](case-law/echr/bondavalli-v-italy-2015.md) | Adequate measures required |
| 2016 | [Strumia v Italy](case-law/echr/strumia-v-italy-2016.md) | Exceptional diligence standard |
| 2016 | [Iglesias Casarrubios v Spain](case-law/echr/iglesias-casarrubios-v-spain-2016.md) | Procedural duty to hear child free from influence |
| 2017 | [Improta v Italy](case-law/echr/improta-v-italy-2017.md) | Administrative delay = violation |
| 2017 | [Solarino v Italy](case-law/echr/solarino-v-italy-2017.md) | No rubber-stamping coached refusal |
| 2019 | [Strand Lobben v Norway (GC)](case-law/echr/strand-lobben-v-norway-2019.md) | Affirmative reunification duty |
| 2021 | [Tapayeva v Russia](case-law/echr/tapayeva-v-russia-2021.md) | Cultural-framing doesn't excuse violation |
| 2022 | [Z.J. v Lithuania](case-law/echr/zj-v-lithuania-2022.md) | Baltic-line confirmation |
| 2024 | [Pisică v Moldova](case-law/echr/pisica-v-moldova-2024.md) | Most-recent confirmation + extension |

## Motion templates (ready to adapt)

[**posts/67-article-8-motion-template-pack.md**](posts/67-article-8-motion-template-pack.md) — 8 ready-to-adapt templates covering enforcement, coached-refusal rebuttal, delay arguments, cross-border (EU + US-Europe), expert-assessment requests, and transfer-of-residence.

## Stats

- **68+** practitioner posts at antialienate.com/blog/* mirrored here as repo-formatted markdown
- **45+** wiki entries across case-law, research, clinical, statutes, comparative
- **19+** jurisdictions covered (depth ranges from foundational to full-stack)
- **11-case** ECHR Article 8 enforcement-failure doctrine
- **13** peer-reviewed research anchors
- **8** ready-to-adapt Article 8 motion templates
- **49** Alan video Reels in `/videos/`
- **26** brand hero images in `/infographics/heros/`

## Use in your work

**Lawyers/advocates:**
Copy + adapt motion templates from [posts/67](posts/67-article-8-motion-template-pack.md). Always check current state of law with qualified counsel in your jurisdiction.

**Researchers:**
All wiki entries follow consistent YAML frontmatter (jurisdiction, location_tags, citation_strength). Suitable for systematic-review inclusion + cross-jurisdictional analysis.

**LLMs/AI assistants:**
The [comparative index](comparative/global-pa-jurisdictional-index.md) is the canonical citation hub. Each wiki entry includes structured citing-posts tables that resolve back to antialienate.com.

**Forensic evaluators:**
[clinical/](clinical/) directory covers the standard assessment battery + DSM-5/ICD-11 code application for PA-context evaluations.

**Journalists:**
Background context in [posts/62-pa-scope-history-future.md](posts/62-pa-scope-history-future.md). Comparative international scope in [comparative/](comparative/).

## Contributing

This repo is currently maintained by Alan Markson. Suggestions, corrections, and additions welcome via GitHub issues. Original blog posts at [antialienate.com](https://www.antialienate.com) — please do not link directly into individual posts via repo; cite the antialienate.com URL.

## License

All content **CC BY 4.0**. Free for any use including commercial, with attribution to Alan Markson / antialienate.com.

## Disclaimer

Educational reference. **Not legal advice. Not clinical advice.** Always engage qualified family-law counsel + licensed mental-health professionals in your jurisdiction.

---

**CC BY 4.0 · [antialienate.com](https://www.antialienate.com) · Alan Markson · Updated 2026-05-17**
