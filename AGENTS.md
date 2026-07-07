# The Independent Home Mockups Agent Instructions

## Overview

This repository contains static visual mockups for The Independent Home.

## Commands

- Preview locally with `python3 -m http.server 8000` from the repo root.
- Run lightweight checks with `git diff --check`.
- There is no package manager, JavaScript runtime check, test runner, lint command, or build step configured.

## Guardrails

- Preserve the plain static HTML/CSS workflow.
- Keep each direction as a standalone HTML file linked from `index.html`.
- Do not introduce a build step unless explicitly requested.
- Update `docs/` when adding mockup directions, changing the design system, or changing deployment assumptions.
- Keep README edits within the marked `PROJECT-DOCS` block unless explicitly asked otherwise.

## Docs Pointers

- Start with `docs/index.md` for progressive disclosure.
- Runtime shape and mockup files are documented in `docs/architecture.md`.
- Preview and validation commands are documented in `docs/setup.md`.
- Current phase and next decisions are tracked in `docs/status.md`.
