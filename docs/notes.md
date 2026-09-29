---
type: Notes
title: Notes
description: Decisions and context for The Independent Home mockups.
resource: the-independent-home-mockups
tags: [notes, design]
generated:
  by: MiMo-V2.6-Pro (OpenCode)
  at: 2026-09-29T20:05:16+00:00
---

# Notes

## Build

- **Standalone is the point.** Any single file must open and render correctly with
  no network access to the repo. That is why there is no shared stylesheet and why
  the base block is duplicated rather than linked.
- **Keep the base block byte-identical** across pages. It is the shared design
  language; drift between pages defeats the comparison.
- **Two style blocks, in order.** Base first, page layer second. Later wins on equal
  specificity, so the page layer can override tokens without specificity hacks.
- Known exceptions: `index.html` stays neutral (one block) and `proof.html` was
  built without inheriting the base (one combined block). Both are deliberate.

## Design

- **Distinct at a glance.** Each direction needs its own paper, accent, card shape,
  and type treatment. Directions that render nearly identically defeat the vote.
- **The theme is a hard constraint**, not a mood board: warm, grounded, hopeful, a
  little rugged; a lived-in working property; natural colours and hand-drawn
  texture; no doom, politics, tactical/prepper imagery, or glossy stock art.
- **Show the mistakes.** The brief asks for honest costs alongside the wins. Every
  direction carries this some way — a corrections panel, empty hooks, mended seams,
  returned mail, misprints kept at full size.
- `index.html` must remain a neutral directory page. It lists directions; it does
  not advocate for one.

## Attribution

- Record which model built each direction in the README, so future work can go
  back to the same source. Directions 1–7 predate the practice and are marked
  "not recorded" rather than guessed.

## Gotchas

- No handwriting fonts on typical Linux: `Segoe Print`, `Bradley Hand`, and
  `Comic Sans MS` all fall back to DejaVu Sans. The fallback chain ends in
  `Liberation Serif` so the script blocks degrade to a serif, not a sans.
- `pkill -f "http.server 8901"` kills the calling shell too — the pattern matches
  its own command line. Use the PID, or `pgrep -f "[h]ttp.server"`.
- Headless Chrome screenshots work for visual review; the in-app browser preview
  needs a connected desktop browser.
