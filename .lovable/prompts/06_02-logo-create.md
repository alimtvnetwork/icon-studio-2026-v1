# Logo Creation Instruction

Canonical workflow for any "create logo / make logo / logo / create icon / design logo / brand mark" request in this repo.

## Inputs (from user)
1. `ProductName` (required)
2. `ProductIdea` — short product idea
3. `VoiceTone` — playful, premium, technical, minimal, etc.
4. `SampleColors[]` — hex/HSL hints (optional)
5. `NeedsDarkWhiteVariants` (boolean) — **default: ON**

If any required input is missing → ask before scaffolding.

## Folder Structure (per project)
```
/ (repo root)
├── favicon.ico                 # regenerated per project
├── favicon.png
├── gif-animation.gif           # optional animation
└── Projects/
    └── {Seq}-{PascalCaseProjectName}/
        ├── README.md
        ├── icons-svg/
        │   ├── Logo.svg
        │   ├── Logo-Dark.svg          # if NeedsDarkWhiteVariants
        │   └── Logo-White.svg         # if NeedsDarkWhiteVariants
        ├── icons-image/
        │   ├── Logo-052.png           # 52px
        │   ├── Logo-128.png           # 128px
        │   ├── Logo-256.png           # 256px
        │   ├── Logo-512.png           # 512px standalone icon
        │   ├── Logo-1024-Light.png    # 1024px light-bg mockup
        │   └── Logo-1024-Dark.png     # 1024px dark-bg mockup
        └── colors-themes/
            ├── Palette.md
            └── Tokens.json            # flat PascalCase keys
```

### Naming rules
- Project folder: `{Seq}-{PascalCaseProjectName}` (e.g. `01-AcmePay`)
- Sequence: zero-padded 2 digits, auto-incremented from existing `Projects/`
- All file/folder names PascalCase where reasonable
- Never overwrite an existing project folder — always next sequence

## Phased Execution (advance only on user `next`)

### Phase 0 — Input Capture
Confirm all 5 inputs. Validate, ask if missing.

### Phase 1 — Project Scaffold
- Ensure `Projects/` exists
- Compute next `{Seq}` by scanning `Projects/`
- Create `Projects/{Seq}-{PascalCaseProjectName}/{icons-svg,icons-image,colors-themes}/`

### Phase 2 — SVG Icon Generation
- `icons-svg/Logo.svg` (primary)
- If `NeedsDarkWhiteVariants` (default true): `Logo-Dark.svg`, `Logo-White.svg`
- Clean viewBox, no embedded raster, accessible `<title>`

### Phase 3 — Raster Image Samples
Generate via image gen and save to `icons-image/`:
- `Logo-052.png`, `Logo-128.png`, `Logo-256.png`, `Logo-512.png`
- `Logo-1024-Light.png` (light-bg mockup)
- `Logo-1024-Dark.png` (dark-bg mockup)

### Phase 4 — Colors & Themes
- `colors-themes/Palette.md` — swatches with HEX + HSL
- `colors-themes/Tokens.json` — flat PascalCase keys:
  ```json
  {
    "Primary": "#...",
    "PrimaryGlow": "#...",
    "Background": "#...",
    "Foreground": "#...",
    "Accent": "#..."
  }
  ```

### Phase 5 — Favicon
- Generate `favicon.ico` + `favicon.png` at repo root (regenerated per project)
- Update `index.html` `<link rel="icon">` to `/favicon.png`

### Phase 6 — README
`Projects/{Seq}-{PascalCaseProjectName}/README.md` sections:
1. Overview (name, idea, voice/tone)
2. Logo Variants (embed all SVGs via relative paths)
3. Image Samples (embed all PNGs)
4. Color Palette (markdown swatches with hex + HSL)
5. Theme Tokens (link/show Tokens.json)
6. Favicon (preview)
7. Usage (how to import)

All paths relative so GitHub renders inline.

### Phase 7 — Acceptance Verification
Verify every acceptance criterion before declaring done.

## Acceptance Criteria
1. `Projects/{Seq}-{PascalCaseProjectName}/` exists with `icons-svg/`, `icons-image/`, `colors-themes/`, `README.md`
2. `Logo.svg` exists; if dark/white requested → both variants exist
3. `icons-image/` has full mixed raster set: 52, 128, 256, 512, 1024-Light, 1024-Dark
4. `Palette.md` + `Tokens.json` (flat PascalCase) exist
5. `favicon.ico`/`favicon.png` exist at repo root, referenced from `index.html`
6. README renders all assets via relative paths on GitHub
7. Instruction stored in `.lovable/prompts/02-logo-create.md` and indexed in `.lovable/prompts.md`
8. **No `mem://` writes for this instruction** — file system is single source of truth

## Coding Guidelines
Read `.lovable/coding-guidelines.md` and `/spec/**` before implementation.
Hard rules: functions ≤ 8 lines, files ≤ 100 lines, no nested/negative ifs, strict types (no `any`/`unknown`), no swallowed errors, no magic strings, `is`/`has` boolean prefixes, DRY first.

## Trigger Phrases
`create logo`, `make logo`, `logo`, `create icon`, `design logo`, `new logo`, `brand mark`
