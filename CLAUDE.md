# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this is

A single-page [Quarto](https://quarto.org) static website — an independent fan tribute to Roger Federer. Content is prose and hand-maintained Markdown tables; there is no application code, data pipeline, or test suite. `my-website.R` is a stub and is not part of the build.

## Commands

```sh
quarto preview          # live-reloading local preview
quarto render           # build the static site into _site/
```

There is no lint or test step. Verify changes by rendering and checking the output in `_site/`.

## Architecture

- **`_quarto.yml`** is the single source of site-wide configuration: navbar entries, HTML format options (theme `cosmo`, right-hand TOC capped at depth 2, full page layout), and the footer. The navbar links are in-page anchors (`index.qmd#career`, etc.); renaming a section heading means updating the matching `navbar.left` href.
- **One content page**: `index.qmd`. All content lives here as `#`-level sections — Career, Grand Slam titles, Rivalries, Legacy — each with `##` subsections. The intro (hero, at-a-glance stats, bio) sits above the first `#` section and the fan-tribute `callout-note` closes the page.
- **`styles.css`** holds all custom styling, layered on top of the `cosmo` Bootstrap theme. It defines the site's CSS custom properties (`--rf-red`, `--rf-navy`, `--rf-cream`) and the custom component classes used via Quarto fenced divs.
- **`_site/`** and `.quarto/` are build output / cache — both gitignored. Never edit files in them by hand.

### Custom content components

Pages compose visual elements with Quarto fenced divs that map to classes in `styles.css`:

- `::: {.rf-hero}` — the dark gradient banner block at the top of the page.
- `::: {.rf-stats}` wrapping several `::: {.rf-stat}` blocks — the responsive stat-card grid. Inside each card, `[20]{.num}` is the big number and `[label text]{.label}` is the caption.

Reuse these rather than inventing new markup so styling stays consistent across the page.

## Content conventions

- Scope is Federer's career **through his September 2022 retirement**; stats are presented as final career totals, sourced from public records (ATP Tour, Wikipedia). The footer and the closing `callout-note` state this framing — keep them consistent if facts change.
- Scores and tables use en-dashes (`–`), not hyphens, between game and set numbers.
##New Things
- Add some color and edit the titles