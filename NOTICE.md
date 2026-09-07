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

## Known gaps carried over from the source repo

This is inherited from the original Nexscope repo, not introduced by the rebrand — verified against the untouched source before packaging:

- **26 skills ship with no YAML frontmatter at all** (no `name:`/`description:` block up top) — e.g. `ebay-seller-guide`, `shopify-conversion-optimization`, `omnichannel-ecommerce`, `ecommerce-ab-testing`, and 22 others. They open with a plain `# Heading` instead.
- **18 skills use a different frontmatter schema** (the Reliability & Site Performance and Additional Tools sections) — a nested `resultify:` block with `category`/`tags`/`version`, but no top-level `description:` field.
- **2 skills** (`ebay-seller-tools`, `walmart-seller-tools`) are the most extreme version of the first case.

Depending on how your agent discovers skills, files without a top-level `name:`/`description:` may not auto-register or auto-invoke the same way the rest of the pack does. Worth normalizing (adding standard frontmatter to all ~46 affected files) before handing this to a client if automatic skill discovery matters for your use case — the written content in every one of them is otherwise complete and usable.

## License

MIT — same terms as the original. See [LICENSE](./LICENSE).
