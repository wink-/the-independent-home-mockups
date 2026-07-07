---
type: Setup
title: Setup
description: Local setup and validation notes for The Independent Home mockups.
resource: the-independent-home-mockups
tags: [setup, static-site, validation]
timestamp: 2026-07-06T00:00:00Z
---

# Setup

No dependency installation is required.

## Local Preview

Open `index.html` directly in a browser or serve the repository root with a static server.

```bash
python3 -m http.server 8000
```

## Validation

Lightweight validation available without installing dependencies:

```bash
git diff --check
```

No automated test, lint, or build command is configured.
