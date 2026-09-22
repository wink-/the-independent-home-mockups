# AGENTS.md

## Purpose

Static redesign mockups for **The Independent Home** — a personal journal about
building a more self-sufficient life.

Mockups exist to be **shown side by side so people can vote on a favorite
direction**. Each mockup is one complete, standalone direction, not a stage of a
shared design.

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

**Avoid:**

- Doom and political messaging.
- Tactical/prepper imagery.
- Glossy corporate stock-art styling.

Read this before building. A direction that ignores it is the wrong direction,
however good it looks.

## Build rules

- **Standalone file.** One self-contained `.html` per direction. Opening that
  single file alone must render it correctly.
- **Inline CSS only.** All styles live in the page's own `<style>` blocks. Never
  link an external stylesheet, never `@import`, never reference another file's
  CSS. This is why `style.css` was removed.
- **First `<style>` block = shared base** — design tokens, resets, and shared
  components. These rules are repeated in every page rather than linked.
- **Later `<style>` block = page-specific** styling, placed after the shared
  block so it wins on equal specificity.
- **Static.** No build step, no dependencies, no framework. Light vanilla JS for
  interactions is fine (see `almanac.html`).
- **Distinct at a glance.** Give each direction its own paper, accent, card
  shape, and type treatment. Directions that render nearly identically defeat
  the point of the vote.
- `index.html` stays a neutral directory page.

## Adding a direction

1. Start from an existing page; it already has the shared base block in place.
2. Pick a unique filename and `<title>`, and keep two `<style>` blocks.
3. Give it a genuinely distinct treatment, following the theme above.
4. Wire it into `index.html` (nav, cards, head-to-head), the nav of **every**
   other page, and the README directions list.
5. Verify: the file has no external references, and it renders standalone.

## Files

| File | Role |
|---|---|
| `index.html` | Neutral directory of all directions |
| `README.md` | Theme, directions list, viewing and CSS notes |
| `*.html` | One standalone direction each |

## Verification

```bash
# no external stylesheet references anywhere
grep -rn 'rel="stylesheet"\|@import\|\.css' *.html

# every page still carries its own styles
for f in *.html; do printf "%-22s %s\n" "$f" "$(grep -o '<style>' "$f" | wc -l)"; done
```
