---
type: Status
title: Status
description: Current project phase and next tasks for The Independent Home mockups.
resource: the-independent-home-mockups
tags: [status, roadmap]
generated:
  by: Gemini 4 Argon Contributor (OpenCode)
  at: 2026-10-17T19:02:00+00:00
---

# Status: Fifteen Directions, Ready for the Vote

The mockup set is complete and live. The open question is a design decision, not
an engineering one.

## Completed

- Fifteen distinct directions are built (1–14 published to `main`, 15 on `add-direction-seed-box-20261017`).
- Each direction is standalone: zero external references, all CSS inline.
- Theme brief recorded in [`../README.md`](../README.md) and
  [`../AGENTS.md`](../AGENTS.md); every direction honours it.
- Model attribution recorded per direction in the README (directions 8–15 name
  the model that built them; 1–7 predate the practice).
- `style.css` removed; each page owns its CSS in two inline blocks.
- OKF documentation written against the current tree.

## Next Tasks

- Select a final design direction, or a hybrid of several.
- Extract reusable components/sections for the production site.
- Record the vote outcome and the reasons for it in [`notes.md`](notes.md).

## Blockers / Risks

- No automated visual regression. Layout is checked by hand or with a headless
  browser, not by a test runner.
- Directions 1–7 have no model attribution; git records only author `Ubuntu`.
- The final direction is a product/design decision outside this repo.

## Last Worked On

- 2026-10-17: Added The Herbarium (14th direction, `herbarium.html`) and The Seed Box (15th direction, `seed-box.html`).

## Suggested First Command

```bash
python3 -m http.server 8901 --bind 0.0.0.0
```
