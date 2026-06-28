# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this is

A static personal portfolio site for Ronnakorn Khansamrong (BossTheDev2209). No build system, no framework, no package manager — just `index.html`, `style.css`, and local assets. Open `index.html` directly in a browser to preview.

## Running locally

```
# Any of these work — just open the file
start index.html          # Windows
python -m http.server     # serves at localhost:8000 (avoids some CORS quirks with local fonts)
```

## Architecture

Single-page layout with five `<section>` elements in order: `#hero`, `#about`, `#projects`, `#skills`, `#footer`. Sticky nav links scroll to each.

**CSS design tokens** live in `:root` in `style.css`:
- `--color-bg` / `--color-text` / `--color-muted` / `--color-accent` (#f27830 orange)
- Background body color is `#fffdf7` (warm white), set directly on `body`, not via the token.

**Font:** LINE Seed Sans TH, self-hosted in `fonts/` as woff/woff2 in 5 weights (100, 400, 700, 800, 900). Already wired up via `@font-face` — don't add Google Fonts or external font CDNs.

**Skills section marquee:** Two identical `.skills-list` divs (second has `aria-hidden="true"`) — this is the CSS infinite-scroll pattern. The scroll animation CSS still needs to be added to `style.css`.

**Projects section:** Currently 5 placeholder cards in a `grid-template-columns: repeat(5,1fr)` grid. Cards need real project data (name, description, link, preview image). The grid has no responsive breakpoints yet.

**Images in repo:**
- `Sigma_PotatoIRL.jpg` — used in Hero and as placeholder for all project cards
- `Sigma_Potato แหก.JPG` — used in About section (filename contains Thai characters and a space — keep as-is)
- `2173.jpg` — unused, may be intended for future use

## Known gaps / in-progress

- No JavaScript at all yet
- No mobile/responsive CSS (project grid will overflow on small screens)
- Skills marquee animation not yet written — **this is where we left off**
- Project cards are all placeholders

## Learning goal

This project is a deliberate learning vehicle. Each part of the site is an opportunity to cover a different frontend concept — by the end, Ronnakorn should have solid hands-on understanding of all the basics: HTML structure, CSS layout (flexbox, grid), styling patterns, animations, responsive design, and eventually JavaScript interactivity. Don't rush to finish the site; go deep on each section before moving on.

## Teaching approach (important)

Ronnakorn is a beginner learning by doing. The role is mentor, not ghost-writer:

- **Guide what to do and why** — explain the concept, name the property/technique, point at the right direction
- **Don't write the code for them** — let them attempt it first, then review and correct
- Ask "what do you think X does?" before explaining
- When they're stuck, give the smallest useful hint, not the full solution
- Praise what's working before pointing out what needs fixing
- Use analogies over jargon when introducing new concepts
