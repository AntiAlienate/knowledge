# Open Source

Everything in this knowledge base is published to be reused. The content — case studies, statutes, jurisdiction summaries, practitioner directories, evidence pages and playbooks — is licensed **CC BY 4.0**, and the structured data files in `/data/` are dedicated to the public domain under **CC0 1.0**. Attribute to AntiAlienate Knowledge with a link, and use it.

## Pages

- [Infographic cards](infographics/README.md) — 38 purpose-built, shareable knowledge cards (1200×630 PNG, CC BY 4.0) covering vocabulary, statistics, frameworks and tactics, designed to be embedded and reposted in advocacy and educational contexts

## Reusing the corpus

- **Discovery:** the canonical machine-readable entry point is [`manifest.json`](https://knowledge.antialienate.com/manifest.json), which enumerates every content type, its per-type `index.json` listing and its JSON schema
- **Schemas:** [practitioner](https://knowledge.antialienate.com/schemas/practitioner.schema.json), [case study](https://knowledge.antialienate.com/schemas/case-study.schema.json) and [jurisdiction](https://knowledge.antialienate.com/schemas/jurisdiction.schema.json) — the JSON files are the source of truth; each `.md` is rendered from its sibling `.json`
- **Source:** [github.com/AntiAlienate/knowledge](https://github.com/AntiAlienate/knowledge) — clone it, fork it, or fetch individual files from `raw.githubusercontent.com/AntiAlienate/knowledge/main/`
- **CLI:** the `aa` command-line tool reads this repository directly; install with `curl -fsSL https://antialienate.com/install.sh | sh`

## Licences

- [LICENSE](../LICENSE) — CC BY 4.0, for all written content
- [LICENSE-DATA](../LICENSE-DATA) — CC0 1.0, for the structured data files

## Contributing

- [CONTRIBUTING.md](../CONTRIBUTING.md) — how entries are verified, the named-person standard, and how to submit corrections or new material

## Related sections

- [Templates](../templates/README.md) — reusable court and documentation templates
- [Community](../community/README.md) — subreddits, advocacy organisations and peer-support resources
- [Verified Publishers](../publishers/README.md) — the people and bodies whose work this corpus draws on
