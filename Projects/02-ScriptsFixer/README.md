# ScriptsFixer

<p align="center">
  <img src="./icons-image/Logo-Animated.gif" alt="ScriptsFixer animated logo" width="200" height="200" />
</p>

## Overview

**ScriptsFixer** is a developer tool that finds and repairs broken scripts — fast. The mark pairs a clean `</>` code-bracket lockup with a small **wrench badge** and a yellow spark: code on the left, repair on the right. Pro tone with a subtle wink.

- **Voice / Tone**: Professional with a quiet wink
- **Concept**: `</>` brackets + wrench fix-badge
- **Palette**: Indigo → Violet → Pink (carried over from the original rocket icon, refined)
- **Animation**: Brackets trace in → slash drops → wrench badge pops → spark + pulse loop

## Logo Variants

| Primary | Dark | White |
|---|---|---|
| <img src="./icons-svg/Logo.svg" width="128" /> | <img src="./icons-svg/Logo-Dark.svg" width="128" /> | <img src="./icons-svg/Logo-White.svg" width="128" style="background:#0F172A" /> |
| `icons-svg/Logo.svg` | `icons-svg/Logo-Dark.svg` | `icons-svg/Logo-White.svg` |

### Animated

| Animated SVG (SMIL, loops) | Animated GIF preview |
|---|---|
| <img src="./icons-svg/Logo-Animated.svg" width="160" /> | <img src="./icons-image/Logo-Animated.gif" width="160" /> |

## Image Samples

| File | Size | Preview |
|---|---|---|
| `Logo-052.png` | 52×52 | <img src="./icons-image/Logo-052.png" width="52" /> |
| `Logo-128.png` | 128×128 | <img src="./icons-image/Logo-128.png" width="96" /> |
| `Logo-256.png` | 256×256 | <img src="./icons-image/Logo-256.png" width="128" /> |
| `Logo-512.png` | 512×512 | <img src="./icons-image/Logo-512.png" width="160" /> |
| `Logo-1024-Light.png` | 1024×1024 | <img src="./icons-image/Logo-1024-Light.png" width="240" /> |
| `Logo-1024-Dark.png` | 1024×1024 | <img src="./icons-image/Logo-1024-Dark.png" width="240" /> |

## Color Palette

| Token | HEX | HSL |
|---|---|---|
| Primary | `#8B5CF6` | `258 90% 66%` |
| PrimaryGlow | `#A78BFA` | `258 90% 76%` |
| Secondary | `#6366F1` | `239 84% 67%` |
| Accent | `#EC4899` | `330 81% 60%` |
| Background | `#FFFFFF` | `0 0% 100%` |
| Foreground | `#0F172A` | `222 47% 11%` |
| Muted | `#F1F5F9` | `210 40% 96%` |
| Border | `#E2E8F0` | `214 32% 91%` |

Full reference: [`colors-themes/Palette.md`](./colors-themes/Palette.md)

## Theme Tokens

Machine-readable tokens (flat PascalCase): [`colors-themes/Tokens.json`](./colors-themes/Tokens.json)

## Favicon

<p>
  <img src="../../favicon.png" alt="favicon" width="64" height="64" />
</p>

Repo-root assets (regenerated per project — ScriptsFixer is current):
- [`/favicon.ico`](../../favicon.ico) — multi-size (16/32/48/64)
- [`/favicon.png`](../../favicon.png) — 256×256
- [`/gif-animation.gif`](../../gif-animation.gif) — animated icon

## Usage

**HTML**
```html
<link rel="icon" type="image/x-icon" href="/favicon.ico" />
<img src="/Projects/02-ScriptsFixer/icons-svg/Logo.svg" alt="ScriptsFixer" width="64" height="64" />
```

**CSS**
```css
:root {
  --sf-primary: #8B5CF6;
  --sf-secondary: #6366F1;
  --sf-accent: #EC4899;
}
```

**Tailwind (`tailwind.config.ts`)**
```ts
theme: {
  extend: {
    colors: {
      scriptsfixer: {
        DEFAULT: "#8B5CF6",
        indigo: "#6366F1",
        spark: "#EC4899",
      },
    },
  },
},
```