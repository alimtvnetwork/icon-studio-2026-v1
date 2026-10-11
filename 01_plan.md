# Logo Creation Plan

Authoritative spec for how Lovable creates logos in this repo.
Mirrored at `.lovable/prompts/02-logo-create.md` and referenced by `mem://index.md`.

## 1. Trigger
User says: `create logo`, `make logo`, `design logo`, `new logo`, `logo for <name>`.

## 2. Inputs
| Key | Required | Notes |
|---|---|---|
| ProductName | yes | Converted to PascalCase |
| ProductIdea | yes | 1–3 sentences |
| VoiceTone | yes | playful / clinical / premium / brutalist / ... |
| SampleColors[] | yes | hex or hint; expanded to full palette |
| NeedsDarkWhiteVariants | optional | **Default: TRUE** |

If anything required is missing, ask before scaffolding.

## 3. Folder Structure
```
/Projects/{Seq}-{PascalCaseProjectName}/
  favicon.ico
  favicon.png
  README.md
  icons-svg/
    Logo.svg
    Logo-Dark.svg          # if NeedsDarkWhiteVariants
    Logo-White.svg         # if NeedsDarkWhiteVariants
  icons-image/
    Logo-52.png
    Logo-128.png
    Logo-256.png
    Logo-512.png
    Logo-Mockup-Light-1024.png
    Logo-Mockup-Dark-1024.png
  colors-themes/
    Palette.md
    Tokens.json
```
- `{Seq}` = zero-padded 2-digit, auto-incremented (`01`, `02`, ...).
- `{PascalCaseProjectName}` from ProductName (e.g. `Acme Pay` → `AcmePay`).
- **Never overwrite** existing project folders.

## 4. Favicon Policy — Per-project only
- Lives inside `Projects/{Seq}-{Name}/`.
- Repo-root favicon and `index.html` are **NOT** touched by logo creation.
- Only if user later says "set as active favicon", copy to repo root + update `index.html`.

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
| Logo-52.png | 52×52 | favicon-tier preview |
| Logo-128.png | 128×128 | small UI |
| Logo-256.png | 256×256 | card / avatar |
| Logo-512.png | 512×512 | hi-res icon, transparent |
| Logo-Mockup-Light-1024.png | 1024×1024 | logo on light bg |
| Logo-Mockup-Dark-1024.png | 1024×1024 | logo on dark bg |

## 7. README.md Sections
1. Overview (name, idea, voice/tone)
2. Logo Variants (embed all SVGs)
3. Image Samples (table of 6 rasters)
4. Color Palette (swatch table HEX/HSL)
5. Theme Tokens (link to Tokens.json)
6. Favicon (preview)
7. Usage (HTML / CSS / Tailwind snippets)

All paths **relative** so GitHub renders inline.

## 8. Phased Execution (driven by `next`)
| Phase | Action |
|---|---|
| 0 | Spec + memory + plan.md written ✅ |
| 1 | Capture brief for an icon |
| 2 | Scaffold project folder + colors-themes/ |
| 3 | Generate icons-svg/ (Logo + Dark/White) |
| 4 | Generate icons-image/ raster set |
| 5 | Generate per-project favicon.ico + favicon.png |
| 6 | Write README.md, verify links |

Each phase ends with a short summary and waits for `next`.

## 9. Naming Rules
- PascalCase: folders, file stems, JSON keys.
- Sequence: zero-padded `01`, `02`, ...
- No spaces in any path.

## 10. Acceptance Criteria
1. Folder + exact subfolders exist.
2. Logo.svg exists; Dark + White by default.
3. 6 raster files in icons-image/.
4. Palette.md + Tokens.json (flat PascalCase) exist.
5. favicon.ico + favicon.png inside the project folder.
6. README renders on GitHub via relative paths.
7. Instruction at `.lovable/prompts/02-logo-create.md`, indexed in `.lovable/prompts.md`.
8. `mem://index.md` Core has the logo-creation rule.

## 11. Out of Scope
- No logo registry / DB.
- No repo-root index.html favicon edits during logo runs.
- No edits to `src/` design system unless asked.
