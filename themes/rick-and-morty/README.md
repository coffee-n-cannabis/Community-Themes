# Rick & Morty

Portal-cartoon aesthetic for UNIT3D. **Portal-green** (`#97ce4c`) + **portal-blue** (`#00b4d8`) accents on dark blue-navy backgrounds, **chunky 3px cartoon borders** on panels, Nunito rounded body type with Orbitron headings that fade through the portal gradient. Bouncy buttons, wavy-underlined links, pill-shaped badges. Playful but not chaotic.

**Author:** homie
**License:** MIT
**Best paired with:** Galactic (UNIT3D theme id 1) — neutral dark base lets the bright cartoon palette pop without color conflicts. Also looks great as full Standalone.
**File:** [`rick-and-morty.css`](rick-and-morty.css)

## The vibe

- Dark blue-navy base with **portal-green + portal-blue glows** in opposite corners of the background.
- Panels wrapped in **thick portal-green borders** (cartoon outline feel).
- Headings use a **portal-green→portal-blue gradient text-fill** that reads like an opened portal.
- Buttons have **bouncy hover (lifts 1px)** and a soft inset shadow for a chunky cartoon button feel.
- Links hover **with a wavy underline** (the playful touch).
- Pill-shaped badges in the portal palette.
- Scrollbars are **portal-gradient** thumbs.

## Usage

Paste this raw URL into your UNIT3D **Settings → General → Style → Standalone CSS Stylesheet** field:

```
https://git.coffee-n-cannabis.com/CnC/Community-Themes/raw/branch/main/themes/rick-and-morty/rick-and-morty.css
```

Save. Done.

To layer it on top of the **Galactic** base theme instead, paste the URL into **External CSS Stylesheet** and pick **Galactic (1)** in the dropdown.

## Tuning

Palette at the top of `rick-and-morty.css` as CSS custom properties:

| Variable | What it controls |
|---|---|
| `--rm-portal-green` | The Rick green (default `#97ce4c`) |
| `--rm-portal-blue`  | The Rick blue (default `#00b4d8`) |
| `--rm-portal-acid`  | Acid-green accent for `code` and chat-typing indicator |
| `--rm-portal-pink`  | Danger / error accent |
| `--rm-border-thick` | Cartoon-border thickness (default `3px`) |
| `--rm-radius`       | Corner roundness (default `14px` — chunky) |
| `--rm-font-body`    | Nunito (rounded body) |
| `--rm-font-head`    | Orbitron (sharp headings) |

To dial back the chunky borders, drop `--rm-border-thick` to `2px` and `--rm-radius` to `8px` in your user CSS.

## Known quirks

- Uses **Nunito** and **Orbitron** from Google Fonts (one `@import`). Falls back to system sans cleanly if your CSP blocks Google Fonts.
- Gradient text-fill on h1/h2 requires `background-clip: text` (`-webkit-` prefixed) — supported by all modern browsers; degrades to solid foreground on very old ones.
- v1 of the rewrite — visual fidelity will improve as it's tested against more UNIT3D pages. PRs to polish specific components welcome.

## Credit

Inspired by the *Rick and Morty* portal palette / cartoon aesthetic. Rebuilt from scratch by homie for current UNIT3D BEM markup.
