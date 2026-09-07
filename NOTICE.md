---
name: notice
description: Attribution notice for this fork
---

# Notice

This pack is a fork of the open-source **eCommerce-Skills** project, originally published by **Nexscope AI** at `github.com/nexscope-ai/eCommerce-Skills` and licensed under the MIT License (see [LICENSE](./LICENSE); the original copyright notice is preserved there as required by the license terms).

## What Resultify Technology changed

- Rebranded all install commands, footers, and metadata from Nexscope AI to Resultify Technology.
- Removed cross-sell links and copy that pointed to Nexscope's own paid platform and companion `Amazon-Skills` repo (which Resultify does not operate), replacing them with neutral text or a pointer to Resultify's own services where appropriate.
- Removed specific product-capability claims (e.g. "real-time FBA fee lookups", "Nexscope Data APIs") that described Nexscope's product, since Resultify does not offer those exact features out of the box.
- Rebuilt the README: accurate skill count (162, verified against the actual folder contents), added three catalog sections for skills that existed in the source repo but weren't listed in its README (Etsy Seller Tools, Reliability & Site Performance, Additional Tools), and rewrote the positioning/CTA sections around Resultify's actual agency services.
- Left the technical content of each skill (frameworks, checklists, platform-specific guidance) unchanged — that's the part that was already good.

## Frontmatter normalization (fixed)

The original source repo shipped 42 skills with non-standard or missing frontmatter, inherited from Nexscope and not introduced by the rebrand:

- **26 skills had no YAML frontmatter at all** (no `name:`/`description:` block) — they opened with a plain `# Heading` instead.
- **16 skills used a nested `resultify:` block** (category/tags/version) with no top-level `description:` field.

All 162 skills now carry standard `name:` (matching the folder slug) and `description:` frontmatter, generated from each skill's existing intro paragraph — no capability content was rewritten. Pre-existing metadata (category, tags, version, author) was preserved under a `metadata.resultify` block rather than discarded. Every skill in this pack now auto-registers the same way with agents that key off frontmatter.

## License

MIT — same terms as the original. See [LICENSE](./LICENSE).
