# Logo Creation Plan

Authoritative spec for how Lovable creates logos in this repo.
Single source of truth: this file + `plan.md` at repo root.
**Do NOT mirror to `mem://`** — file system only.

## 1. Trigger
User says: `create logo`, `make logo`, `design logo`, `new logo`, `logo for <name>`, `create icon`.

## 2. Inputs
| Key | Required | Notes |
|---|---|---|
| ProductName | yes | Converted to PascalCase |
| ProductIdea | yes | 1–3 sentences (voice/tone hint) |
| VoiceTone | yes | playful / clinical / premium / brutalist / ... |
| SampleColors[] | yes | hex or hint; expanded to full palette |
| NeedsDarkWhiteVariants | optional | **Default: TRUE** |

If anything required is missing, ask before scaffolding.

## 3. Folder Structure
```
/ (repo root)
├── favicon.ico                 # regenerated per project
├── favicon.png                 # regenerated per project
├── gif-animation.gif           # animated icon (latest project)
└── Projects/
    └── {Seq}-{PascalCaseProjectName}/
        ├── README.md
        ├── icons-svg/
        │   ├── Logo.svg
        │   ├── Logo-Dark.svg          # if NeedsDarkWhiteVariants
        │   ├── Logo-White.svg         # if NeedsDarkWhiteVariants
        │   └── Logo-Animated.svg      # SMIL animation
        ├── icons-image/
        │   ├── Logo-052.png
        │   ├── Logo-128.png
        │   ├── Logo-256.png
        │   ├── Logo-512.png
        │   ├── Logo-1024-Light.png
        │   ├── Logo-1024-Dark.png
        │   └── Logo-Animated.gif
        └── colors-themes/
            ├── Palette.md
            └── Tokens.json
```
- `{Seq}` = zero-padded 2-digit, auto-incremented (`01`, `02`, ...).
- `{PascalCaseProjectName}` from ProductName (e.g. `Acme Pay` → `AcmePay`).
- **Never overwrite** existing project folders — always create the next sequence.

## 4. Favicon Policy — Repo root, per-project regeneration
- `favicon.ico` + `favicon.png` live at **repo root**.
- Regenerated each time a new logo project is created (latest project wins).
- `index.html` `<link rel="icon">` references `/favicon.ico` and `/favicon.png`.
- `gif-animation.gif` at repo root mirrors the latest project's animated icon.

## 5. Tokens.json — Flat PascalCase
```json
{
  "Primary": "#RRGGBB",
  "PrimaryGlow": "#RRGGBB",
  "Secondary": "#RRGGBB",
  "Accent": "#RRGGBB",
  "Background": "#RRGGBB",
  "Foreground": "#RRGGBB",
  "Muted": "#RRGGBB",
  "Border": "#RRGGBB"
}
```
`Palette.md` shows same swatches with HEX + HSL + usage notes.

## 6. Raster Samples — Mixed Set
| File | Size | Purpose |
|---|---|---|
| Logo-052.png | 52×52 | favicon-tier preview |
| Logo-128.png | 128×128 | small UI |
| Logo-256.png | 256×256 | card / avatar |
| Logo-512.png | 512×512 | hi-res icon, transparent |
| Logo-1024-Light.png | 1024×1024 | logo on light bg |
| Logo-1024-Dark.png | 1024×1024 | logo on dark bg |
| Logo-Animated.gif | 512×512 | animated preview |

## 7. README.md Sections
1. Overview (name, idea, voice/tone)
2. Logo Variants (embed all SVGs incl. animated)
3. Image Samples (raster table)
4. Color Palette (HEX/HSL swatches)
5. Theme Tokens (link to Tokens.json)
6. Favicon (preview)
7. Usage (HTML / CSS / Tailwind / manifest snippets)

All paths **relative** so GitHub renders inline.

## 8. Execution — One Shot
Generate everything in a single pass: scaffold → SVGs (static + animated) →
rasters (52/128/256/512 + 1024 light/dark) → animated GIF → palette + tokens →
repo-root favicon + gif-animation.gif → update `index.html` → write `README.md`.
**No phased `next` gating** unless the user explicitly requests phased delivery.

## 9. Naming Rules
- PascalCase: folders, file stems, JSON keys.
- Sequence: zero-padded `01`, `02`, ...
- Raster sizes: 3-digit pad below 1000 (`Logo-052.png`); `Logo-1024-Light.png` / `Logo-1024-Dark.png`.
- No spaces in any path.

## 10. Acceptance Criteria
1. `Projects/{Seq}-{PascalCaseProjectName}/` exists with `icons-svg/`, `icons-image/`, `colors-themes/`, `README.md`.
2. `Logo.svg` exists; `Logo-Dark.svg` + `Logo-White.svg` by default; `Logo-Animated.svg` included.
3. 7 raster files in `icons-image/` (6 PNG + 1 GIF).
4. `Palette.md` + `Tokens.json` (flat PascalCase) exist.
5. `favicon.ico` + `favicon.png` + `gif-animation.gif` at repo root; `index.html` references favicon.
6. README renders on GitHub via relative paths.
7. Spec lives at `.lovable/prompts/02-logo-create.md`, indexed in `.lovable/prompts.md`, mirrored to root `plan.md`.
8. **Not stored in `mem://`** beyond a one-line pointer in `mem://index.md` Core.

## 11. Coding Guidelines (any helper scripts)
- Functions ≤ 8 lines, files ≤ 100 lines.
- No nested or negative ifs; strict types (no `any`/`unknown`).
- No swallowed errors, no magic strings.
- `is`/`has` prefixes for booleans. DRY first.

## 12. Out of Scope
- No logo registry / DB.
- No edits to `src/` design system unless asked.
- No `mem://` storage of the full spec.
