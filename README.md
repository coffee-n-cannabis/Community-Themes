# Community-Themes

Community CSS themes for UNIT3D Community Edition.  Designed as
**External overlays** — they layer on top of any UNIT3D base theme to
re-skin the palette, components, and effects without replacing the
underlying layout.

All themes are MIT-licensed.  Fork, remix, or build on freely.


## Usage

Pick a theme and grab its URL:

```
https://coffee-n-cannabis.github.io/Community-Themes/themes/matrix/matrix.css
https://coffee-n-cannabis.github.io/Community-Themes/themes/synthwave/synthwave.css
https://coffee-n-cannabis.github.io/Community-Themes/themes/rick-and-morty/rick-and-morty.css
```

These URLs work on any UNIT3D install whose CSP allows `*.github.io`
(the upstream default does).

In your UNIT3D site:

```
Settings -> General -> Style
```

1. Pick a **base theme** from the dropdown (see the pairing table below).
2. Paste the community theme URL into the **External CSS Stylesheet** field.
3. Save.
4. Hard refresh (Ctrl+F5 / Cmd+Shift+R).

The base theme provides the layout structure; the community theme
overlays the palette and components on top.

To revert: clear the field and save.  Community CSS never modifies your
saved settings — only what's rendered.


## Recommended base theme

| Community theme | Base theme | UNIT3D theme id | Why |
|-----------------|------------|-----------------|-----|
| Matrix          | Terminal   | 29              | Both CRT green-on-black — same family. |
| Synthwave       | Cyberpunk  | 26              | Shared neon-on-dark palette. |
| Rick & Morty    | Galactic   | 1               | Neutral dark base — cartoon palette pops. |

For a universal safe pick across any community theme, use **Galactic**.
It stays out of the way.


## Standalone CSS Stylesheet (not recommended)

UNIT3D also has a **Standalone CSS Stylesheet** field that *replaces*
the entire theme — `main.scss` doesn't load, the dropdown theme is
bypassed entirely, and only the URL you paste serves the page.

**These themes were authored as External overlays.**  They define
palette, components, and effects, but they do not include the structural
layout CSS (grid, flex, navigation scaffolding) that lives in
`main.scss`.  Pasted into Standalone, they give you the colors but not
the layout — the page renders as plain stacked text on a colored
background.

Use External mode + a base theme.  That is how these themes were
designed to work.


## Themes in this repository

- **themes/matrix/** — green-on-black CRT terminal.  Scanlines.  Glow.
- **themes/synthwave/** — 80s neon retrofuturism.  Hot pink, cyan, deep violet.
- **themes/rick-and-morty/** — portal cartoon palette.
- **themes/_template/** — skeleton for new submissions.

See [catalog.md](catalog.md) for the full index.


## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md).  Short version: fork, add your
theme under `themes/<name>/`, open a PR.  Use `themes/_template/` as a
skeleton.


## Where this lives

| Role             | Location                                          |
|------------------|---------------------------------------------------|
| Canonical source | `git.coffee-n-cannabis.com/CnC/Community-Themes`  |
| Public mirror    | `github.com/coffee-n-cannabis/Community-Themes`   |
| Pages CDN        | `coffee-n-cannabis.github.io/Community-Themes/`   |


## License

MIT.  See [LICENSE](LICENSE).
