---
type: Architecture
title: Architecture
description: Runtime shape and key files for The Independent Home mockups.
resource: the-independent-home-mockups
tags: [architecture, static-site, mockups]
generated:
  by: MiMo-V2.6-Pro (OpenCode)
  at: 2026-09-29T20:05:16+00:00
---

# Architecture

A plain static mockup gallery. Thirteen self-contained design directions, plus a
neutral directory page. No build step, no dependencies, no framework.

## Runtime Shape

One file per direction. Opening any single file alone must render it correctly:
nothing is linked, nothing is bundled.

| File | Role |
| --- | --- |
| `index.html` | Neutral directory of all directions |
| `field-journal.html` | Rugged notebook, paper-first source material, monospaced transcript |
| `ledger.html` | Dashboard/stat-card view for monthly control-ledger updates |
| `homestead.html` | Warm editorial direction for broader readers |
| `terminal.html` | Tech-forward AI transparency / paper transcript direction |
| `ephemera.html` | Kitchen-table clippings, receipts, scan scraps, pinned notes |
| `blueprint.html` | Technical house-systems map for power, food, water, money, privacy |
| `workshop.html` | Manuals, checklists, and course funnel |
| `almanac.html` | Seasonal filing by power, food, water, money, and privacy |
| `proof.html` | Two-colour risograph field zine (orange = wins, green = costs) |
| `dispatches.html` | Postal correspondence: envelopes, stamps, postmarks, returned mail |
| `pegboard.html` | Shop wall: tools on hooks, kraft tags, empty hooks for mistakes |
| `herald.html` | Local broadsheet: front page, briefs, corrections, classifieds |
| `quilt.html` | Mended patchwork quilt: patches, stitched seams, mending ledger |

## Styling Contract

There is **no shared stylesheet**. Every page owns all of its CSS, inline.

- The **first** `<style>` block holds the shared base: design tokens, resets, and
  shared components (`.wrap`, `.top`, `.nav`, `.hero`, `.card`, `.btn`, and so on).
  These rules are repeated verbatim in every page rather than linked, which is what
  keeps each file standalone.
- A **later** `<style>` block holds the page-specific layer. It comes after the base
  so it wins on equal specificity — it overrides tokens and adds that direction's
  own components.
- The shared base block must stay byte-identical across pages. To change a shared
  rule, apply the same edit to every page's first block.

Known exceptions: `index.html` (neutral directory, one block) and `proof.html`
(built without inheriting the shared base, so it carries a single combined block).

## Interaction

Most directions are static. A few use light vanilla JS for a single interaction —
a registration slider, a mail-sorting filter, a patch that lifts. No framework,
no dependencies, no build output.

## Dependencies

None. No package manager, no runtime, no build pipeline. The only external assets
are inline SVG data URIs.

## Deployment

GitHub Pages from `main` at
[`https://wink-.github.io/the-independent-home-mockups/`](https://wink-.github.io/the-independent-home-mockups/).
Each push to `main` triggers a Pages build; verify with `gh api` against the
latest `github-pages` deployment.
