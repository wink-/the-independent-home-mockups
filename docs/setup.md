---
type: Setup
title: Setup
description: Local setup and validation notes for The Independent Home mockups.
resource: the-independent-home-mockups
tags: [setup, static-site, validation]
generated:
  by: MiMo-V2.6-Pro (OpenCode)
  at: 2026-09-29T20:05:16+00:00
---

# Setup

No dependency installation is required. There is nothing to install.

## Local Preview

Open any `<name>.html` directly in a browser — each file renders standalone — or
serve the repository root:

```bash
python3 -m http.server 8901 --bind 0.0.0.0
```

Then visit `http://localhost:8901/` (or `<host-ip>:8901/` from another machine).

## Validation

Lightweight checks that need no dependencies:

```bash
# no external stylesheet references anywhere (want NONE)
grep -rn 'rel="stylesheet"\|@import\|\.css' *.html

# every page still carries its own styles
for f in *.html; do printf "%-22s %s\n" "$f" "$(grep -o '<style>' "$f" | wc -l)"; done

# whitespace check
git diff --check
```

Expected: no external stylesheet references, and at least one `<style>` block per
page (two for the directions that use the shared-base + page-layer split).

There is no automated test, lint, or build command configured. Visual checking is
done in a browser; the mockups are the artifact.

## Adding a Direction

1. Start from an existing page — it already has the shared base block in place.
2. Pick a unique filename and `<title>`, and keep two `<style>` blocks.
3. Give it a genuinely distinct treatment, following the theme in
   [`../AGENTS.md`](../AGENTS.md).
4. Wire it into `index.html` (nav, cards, head-to-head), the nav of **every** other
   page, and the README directions list.
5. Run the validation commands above.
