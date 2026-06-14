# Open Source

The AntiAlienate Knowledge Base is an open-source project. All content under [CC BY 4.0](../LICENSE) (editorial commentary; primary statutory and case-law text under each source's own license).

## Source repository

- **Public mirror:** [antialienateorg/antialienate-knowledge](https://github.com/antialienateorg/antialienate-knowledge)
- **License:** [CC BY 4.0](../LICENSE)
- **Contributing:** [CONTRIBUTING.md](../CONTRIBUTING.md)

## What's in the open

- **Markdown source** for every page on knowledge.antialienate.com
- **JSON schemas** at [/schemas/](https://knowledge.antialienate.com/schemas/) — practitioner.schema.json, case-study.schema.json, jurisdiction.schema.json
- **Manifest** at [/manifest.json](https://knowledge.antialienate.com/manifest.json) — self-hosted URLs for downstream consumers
- **Case-law per-entry JSON** at `/case-law/<jurisdiction>/<slug>.json` — verbatim statutory text + commentary for app/RAG consumption
- **Build tooling** in `/bin/` — aa-build, aa-cite, aa-crosslink, aa-autolink
- **Infographics** assets at [open-source/infographics/](infographics/)

## Downstream consumers

The site is the canonical data source for the AntiAlienate app and Liena RAG. The self-hosted JSON layer ensures downstream consumers fetch directly from `knowledge.antialienate.com` without GitHub API dependencies.

## Reporting issues

Found a citation error, a missing jurisdiction, or a stale link? Open an issue or PR at the source repository above.

## Related sections

- [Verified Publishers](../publishers/) — upstream sources we cite
- [Community](../community/) — how to participate
- [Contributing guide](../CONTRIBUTING.md)

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
