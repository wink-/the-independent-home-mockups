# The Independent Home mockups

Static redesign mockups for a handwritten-first version of The Independent Home.

Live site: https://wink-.github.io/the-independent-home-mockups/

## The theme

The Independent Home is a personal journal about building a more self-sufficient
life—taking practical steps toward more control over your home, money, work, and
time. It's for ordinary people who feel tied to a paycheck and want more
independence without disappearing into the wilderness.

The content follows real projects and honest progress: solar power, DIY and
workshop projects, improving the property, side income, and making full-time
employment optional. It should show the mistakes and actual costs alongside the
wins—not pretend to have everything figured out.

**Central feeling:** "I'm not a prepper. I just want more control."
Practical independence, one project at a time.

### Artwork direction

Warm, grounded, hopeful, and a little rugged.

- A lived-in home and working property, not a luxury farmhouse or survival bunker.
- Imagery could include a workshop, garden beds, solar panels, tools, and
  handwritten journal details.
- Natural colors, hand-drawn textures, and a sense of things being built
  gradually would fit.

Avoid:

- Doom and political messaging.
- Tactical/prepper imagery.
- Glossy corporate stock-art styling.

## What this repo is

A set of showcase mockups to be shown side by side so people can vote on a
favorite direction.

- **Independent.** Each page is one complete direction, not a stage of a shared
  design. Any single file can be opened, previewed, or shared on its own and
  still renders correctly.
- **Inline CSS only.** Every page carries its own styles in its own `<style>`
  block. No page links an external stylesheet, so nothing breaks when a file is
  viewed in isolation.
- **Static.** Plain HTML + CSS, no build step, no dependencies.

**Every direction must honor [The theme](#the-theme) above** — warm, grounded,
hopeful, a little rugged; a lived-in working property rather than a luxury
farmhouse or bunker; and free of doom, political, tactical/prepper, or glossy
corporate stock-art styling.

`index.html` is the neutral directory page that lists all directions.

## Directions

1. **Field Journal** — rugged notebook, paper-first source material, monospaced transcript. *Made by: not recorded*
2. **Independence Ledger** — dashboard/stat-card view for monthly control-ledger updates. *Made by: not recorded*
3. **Homestead Magazine** — warm editorial direction for broader readers. *Made by: not recorded*
4. **Terminal Paper Lab** — tech-forward AI transparency / paper transcript direction. *Made by: not recorded*
5. **Kitchen Table Evidence Board** (`ephemera.html`) — kitchen-table clippings, receipts, scan scraps, and pinned notes. *Made by: not recorded*
6. **Home Systems Blueprint** — technical house-systems map for power, food, water, money, privacy. *Made by: not recorded*
7. **Workshop Manual** — calm lead-magnet/course funnel built around operating manuals and checklists. *Made by: not recorded*
8. **Home Almanac** — seasonal filing by power, food, water, money, and privacy; reader enters through the year, not the feed. *Made by: MiMo-V2.6-Flash Free (`mimo-v2.6-flash-free`)*
9. **Proof Sheets** (`proof.html`) — two-colour risograph field zine: orange prints what went right, green prints what it cost, so mistakes and real costs get equal billing with the wins. *Made by: MiMo-V2.6-Flash Free (`mimo-v2.6-flash-free`)*
10. **Dispatches** (`dispatches.html`) — postal correspondence from the property: every project mailed twice (what it gave us / what it took), with the returned envelopes filed alongside. *Made by: DeepSeek V4.1 Flash (`deepseek-v4.1-flash`)*
11. **Pegboard** (`pegboard.html`) — every project as a tool on the shop wall, tagged with what it does and what it cost; empty hooks left dashed. *Made by: Hy4 preview (`hy4-preview`)*

### Attribution notes

- Directions **8–9** were built by `mimo-v2.6-flash-free` (MiMo-V2.6-Flash Free), OpenCode, September 2026.
- Direction **10** (Dispatches) was built by `deepseek-v4.1-flash` (DeepSeek V4.1 Flash, provider `opencode-go`), OpenCode, September 2026.
- Direction **11** (Pegboard) was built by `hy4-preview` (Hy4 preview, provider `opencode-go`), OpenCode, September 2026.
- Directions **1–7** predate this record. Git shows only author `Ubuntu` and no model metadata, so their model is **not recorded** — don't guess:
  - 1–4 — commit `d3fd932`, 2026-05-20, "Add Independent Home mockups"
  - 5–7 — commit `092cfc1`, 2026-06-11, "Add more Independent Home mockup directions"
- Directions 8–10 were published to `main` on 2026-09-22. Direction 11 is on branch `add-direction-pegboard-20260922`.
- If you know which model built 1–7, record it here so future work can go back to it.

Recommendation: use Field Journal as the base, then borrow Ledger stat cards,
Workshop conversion sections, and Blueprint explainers as modules.

## Viewing

Open any `<name>.html` directly in a browser, or serve the folder:

```bash
python3 -m http.server 8901
```

Then visit http://localhost:8901/ (or `<host-ip>:8901/` from another machine).

## Editing CSS

There is no shared stylesheet — each page owns all of its CSS.

- A page's **first** `<style>` block holds the shared tokens and base rules.
  Those rules are repeated in every page rather than linked, which is what
  keeps each file standalone.
- To change a shared rule, apply it to every page's first `<style>` block so
  the directions stay consistent.
- Page-specific styling belongs in a **later** `<style>` block in that page
  only, placed after the shared block so it wins on equal specificity.
