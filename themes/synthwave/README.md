# Synthwave

80s neon retrofuturism for UNIT3D. Deep purple/violet darks (`#0a0412`), hot-pink primary neon (`#ff00aa`), cyan accents (`#00fff5`), gradient sunset on buttons, **subtle retro grid floor** at the bottom of the viewport, soft text-glow on accents. Orbitron headings, system body.

**Author:** homie
**License:** MIT
**Best base in External mode:** Cyberpunk (UNIT3D theme id 26) — shared neon-on-dark palette, Synthwave's gradients layer naturally onto Cyberpunk's already-neon base. *(In **Standalone** mode the dropdown is ignored entirely — pick anything, doesn't matter. Pairing only applies to External mode or as a Standalone fallback.)*
**File:** [`synthwave.css`](synthwave.css)

## The vibe

- Deep cosmic-purple page with **two radial-gradient glows** baked into the background (cyan up top-left, pink down center-bottom).
- **Retro grid floor** at the bottom of the viewport via perspective-rotated repeating gradients (the classic Synthwave horizon).
- Buttons use a **pink → violet → blue sunset gradient** with pink glow.
- Orbitron headings in uppercase with hot-pink glow.
- Cyan links with soft glow on hover.
- Pill-shaped badges with neon outlines.

## Usage

Paste this raw URL into your UNIT3D **Settings → General → Style → Standalone CSS Stylesheet** field:

```
https://git.coffee-n-cannabis.com/CnC/Community-Themes/raw/branch/main/themes/synthwave/synthwave.css
```

Save. Done.

To layer it on top of the **Cyberpunk** base theme instead, paste the URL into **External CSS Stylesheet** and pick **Cyberpunk (26)** in the dropdown.

## Tuning

Palette at the top of `synthwave.css` as CSS custom properties. Override these in your own user CSS to remix:

| Variable | What it controls |
|---|---|
| `--sw-pink` | Primary neon (default `#ff00aa`) |
| `--sw-cyan` | Secondary neon (default `#00fff5`) |
| `--sw-violet` | Accent purple |
| `--sw-bg` | Page background |
| `--sw-sunset` | The gradient used on buttons |
| `--sw-glow-pink` / `--sw-glow-cyan` | Text/box glow shadows |
| `--sw-font-head` | Orbitron stack for headings |

To kill the grid floor (some find it busy on long pages), in your user CSS:

```css
body::before { display: none !important; }
```

## Known quirks

- Uses **Orbitron** from Google Fonts (one external `@import`). If your CSP blocks Google Fonts, the headings fall back to system sans cleanly.
- The grid-floor overlay sits at `z-index: 0` and uses `pointer-events: none` — should never interfere with content.
- Heavy on the pink glow by design. Lower `--sw-glow-pink` opacity in your user CSS if you want a calmer Synthwave.
- v1 of the rewrite — visual fidelity will improve as it's tested against more UNIT3D pages. PRs to polish specific components welcome.

## Credit

Inspired by 80s synthwave / outrun aesthetic. Rebuilt from scratch by homie for current UNIT3D BEM markup.
