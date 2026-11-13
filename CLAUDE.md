# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Git workflow

- Every feature or fix gets its own branch — never commit directly to `main`.
- Committing is fine to do automatically, without asking first.
- Pushing is never automatic — always ask for explicit confirmation before running `git push`, regardless of branch.

## What this is

Awesome Weather is a curated "awesome list" (no application code) of weather-related resources: official alert institutions, numerical models, storm/lightning tracking, air quality/fire monitoring, interactive visualizations, satellite/radar, crisis-monitoring (MSGU/VISOV) resources, and developer APIs. Content is in French, targeted at weather enthusiasts, developers, and crisis-monitoring volunteers.

## Source of truth

`README.md` is the single source of truth. `docs/index.md` is auto-generated from it by `.github/workflows/sync-pages-from-readme.yml` (GitHub Pages) — **never edit `docs/index.md` directly**, changes will be overwritten.

## Structure

- `README.md` — the list itself, organized by section (see its table of contents).
- `guides/` — longer-form usage guides for individual resources (e.g. `guides/vigicrues.md`).
- `assets/` — images (banner, etc.) referenced from the README.
- `CONTRIBUTING.md` — contribution format/process for adding new entries.
- `.markdownlint-cli2.jsonc` — markdown linting config; run via the `.github` CI workflow.

## Conventions

- Each entry follows the existing format: `[Name][ref-key] - Description. *Pricing · Coverage*`, with reference-style links collected at the bottom of the relevant README section.
- Keep the table of contents in `README.md` in sync with section headers when adding/renaming a section.
- Respect `<!-- PAGES-SKIP-START -->` — content after it (Contribuer/GitHub Pages sections) is intentionally excluded from the generated Pages site.

## Workflow git

Règles générales dans `~/.claude/CLAUDE.md`. Pour ce dépôt, `main` est la branche de production : un push peut déclencher une mise en ligne, et GitHub ne la protège pas (offre gratuite, dépôt privé).

- Jamais de commit ni de push direct sur `main`, jamais de force-push.
- Une branche par sujet depuis `origin/main` à jour : `git switch -c <type>/<sujet> origin/main`.
- `git add <fichiers>` uniquement, jamais `git add -A` ni `git add .`. Un worktree par session si plusieurs sessions travaillent ici.
- Livraison par pull request (`gh pr create --base main`). Ne pas fusionner sans l'accord explicite de Quentin.
- Demander confirmation avant tout `git push`.
