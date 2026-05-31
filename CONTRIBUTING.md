# Contributing a theme

Open to anyone. A few principles up front:

- **Original work or properly credited.** If you didn't write it from scratch, credit the source in your theme's `README.md`. Don't strip authorship off someone else's work.
- **Standalone-safe.** Your theme should be designed primarily for the **Standalone CSS** field (full replacement). Note in your theme's README if it works as **External CSS** (layered) instead — that's a useful flavor, just be explicit.
- **No external network dependencies** beyond webfonts. Don't pull JS, don't `@import` someone else's stylesheet from a third-party CDN that could disappear.
- **Self-contained per theme.** Everything for one theme lives in `themes/your-theme-name/` — its CSS, its README, its screenshot. No cross-theme imports.

## How to submit

1. **Fork** this repo to your own Gitea account (or wherever).
2. **Copy** `themes/_template/` to `themes/<your-theme-name>/` (kebab-case, no spaces).
3. **Rename** `theme.css` → `<your-theme-name>.css`. Customize it.
4. **Edit** the `README.md` inside your theme dir — fill in description, author, screenshot, license.
5. **Add a `preview.png`** — at minimum a screenshot of the home/torrents page using your theme. ~1200px wide is good.
6. **Add your theme to** [`catalog.md`](catalog.md) — one row in the table.
7. **Open a PR.**

## What we're looking for in a theme

- Targets current UNIT3D BEM markup (`panelV2`, `panel__heading`, `form__group`, `nav-tabV2`, `breadcrumbV2`, etc.). Themes built for old markup will fight the layout.
- Uses **CSS custom properties** for the palette near the top of the file — makes the theme tunable in one spot and easy for others to remix.
- Coverage of the essentials: body/typography, panels, forms, buttons, tables, nav, chatbox, footer. Doesn't have to be exhaustive — the base theme covers the rest in External mode.
- A clear visual identity. "Dark blue with slightly different accents" is fine but boring. Bring a vibe.

## What gets rejected

- Themes that target removed/old markup (broken on render).
- Themes that ship third-party JS or call external APIs.
- Themes presented as original work when they're forked from someone else without credit.
- Themes that resell anything that's free upstream or claim authorship of community work.

## Iterating on existing themes

PRs to improve the seed themes (Matrix / Synthwave / Rick & Morty) are very welcome — visual polish, broader component coverage, accessibility fixes, browser-quirk patches.

## Code of conduct

Be cool. Credit work. Don't ship malware. That's the whole thing.
