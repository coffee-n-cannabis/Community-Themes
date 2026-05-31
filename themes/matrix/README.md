# Matrix

Green-on-black CRT terminal aesthetic for UNIT3D. Classic `#00ff41` Matrix green on pure black, monospace typography throughout, **scanline overlay** that lays a subtle CRT pattern over the whole page, soft green glow on interactive elements.

**Author:** homie
**License:** MIT
**Best base in External mode:** Terminal (UNIT3D theme id 29) — both are CRT green-on-black aesthetics; the base structure complements Matrix's overrides naturally. *(In **Standalone** mode the dropdown is ignored entirely — pick anything, doesn't matter. Pairing only applies to External mode or as a Standalone fallback.)*
**File:** [`matrix.css`](matrix.css)

## The vibe

- Pure black background (`#000`), no compromises.
- Monospace everywhere — body text, headings, inputs, buttons.
- **Scanlines** over the whole page via a fixed `repeating-linear-gradient` overlay.
- Subtle CRT vignette to deepen the "old monitor" feel.
- Soft green glow (`text-shadow` + focus-state `box-shadow`) on interactive elements.
- Headings prefixed with `> ` like terminal prompts.
- Blinking caret on focused inputs.

## Usage

Paste this raw URL into your UNIT3D **Settings → General → Style → Standalone CSS Stylesheet** field:

```
https://git.coffee-n-cannabis.com/CnC/Community-Themes/raw/branch/main/themes/matrix/matrix.css
```

Save. Done.

To layer it on top of the **Terminal** base theme instead, paste the same URL into **External CSS Stylesheet** and pick **Terminal (29)** in the dropdown — gives you the best blend of base structure + Matrix overlay.

## Tuning

The palette lives at the top of `matrix.css` as CSS custom properties. Drop these into your own user CSS to remix without forking the file:

| Variable | What it controls |
|---|---|
| `--matrix-fg` | The signature green (default `#00ff41`) |
| `--matrix-bg` | Page background (default pure black) |
| `--matrix-panel` | Panel surfaces |
| `--matrix-border` | Default border green |
| `--matrix-glow` | Glow box-shadow on focus + headings |
| `--matrix-font` | Monospace stack |

To kill the scanlines (some find them busy), in your user CSS:

```css
body::before, body::after { display: none !important; }
```

## Known quirks

- Heavy on the green — by design. If you want a calmer Matrix, lower `--matrix-fg` brightness or use it as **External CSS** on the Terminal base.
- The scanline overlay uses `mix-blend-mode: screen` — degraded but not broken on browsers that don't support it.
- v1 of the rewrite — visual fidelity will improve as it's tested against more UNIT3D pages. PRs to polish specific components welcome.

## Credit

Inspired by *The Matrix* CRT aesthetic. Rebuilt from scratch by homie for current UNIT3D BEM markup.
