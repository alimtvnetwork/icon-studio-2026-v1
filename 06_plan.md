# Logo Creation Spec & Plan

## Overview
Standard operating procedure for any "create a logo" / "make logo" / "logo" request in this repo. Each logo request scaffolds a self-contained project folder under `Projects/`, generates SVG + raster assets, color tokens, favicon, and a GitHub-rendering README.

## Inputs (collected from user)
1. `ProductName` (required) — converted to PascalCase
2. `ProductIdea` — short description
3. `VoiceTone` — e.g. playful, premium, technical, minimal
4. `SampleColors[]` — hex/HSL hints (optional)
5. `NeedsDarkWhiteVariants` (boolean) — **default: true**

If any required input is missing → ask before scaffolding.

## Folder Structure (per project)
```
/ (repo root)
├── favicon.ico                      # overwritten with active project's favicon
├── favicon.png
└── Projects/
    └── {Seq}-{PascalCaseProjectName}/
        ├── favicon.ico
        ├── favicon.png
        ├── README.md
        ├── icons-svg/
        │   ├── Logo.svg
        │   ├── Logo-Dark.svg        # if NeedsDarkWhiteVariants
        │   └── Logo-White.svg       # if NeedsDarkWhiteVariants
        ├── icons-image/
        │   ├── Logo-Sample-01.png   # 512×512 icon
        │   ├── Logo-Sample-02.png   # 1024×1024 light-bg mockup
        │   └── Logo-Sample-03.png   # 1024×1024 dark-bg mockup
        └── colors-themes/
            ├── Palette.md
            └── Tokens.json
```

### Naming rules
- Project folder: `{Seq}-{PascalCaseProjectName}` (e.g. `01-AcmePay`)
- Sequence: zero-padded 2 digits, auto-incremented from existing `Projects/` contents
- All files/folders: PascalCase where reasonable
- Never overwrite an existing project folder — always next sequence

## Phased Execution (advance only on user `next`)

### Phase 0 — Input Capture
Confirm `ProductName`, `ProductIdea`, `VoiceTone`, `SampleColors[]`, `NeedsDarkWhiteVariants`. Validate → ask if missing.

### Phase 1 — Project Scaffold
- Ensure `Projects/` exists
- Compute next `{Seq}` by scanning `Projects/`
- Create `Projects/{Seq}-{PascalCaseProjectName}/` with empty subfolders: `icons-svg/`, `icons-image/`, `colors-themes/`

### Phase 2 — SVG Icon Generation
- `icons-svg/Logo.svg` — primary
- If `NeedsDarkWhiteVariants` (default true): `Logo-Dark.svg`, `Logo-White.svg`
- Clean viewBox, no embedded raster, accessible `<title>`

### Phase 3 — Raster Image Samples
Generated via image gen (nano-banana family) and saved to `icons-image/`:
- `Logo-Sample-01.png` — 512×512 standalone icon
- `Logo-Sample-02.png` — 1024×1024 light-background mockup
- `Logo-Sample-03.png` — 1024×1024 dark-background mockup
Optional extra icon set: 52/128/256 if requested.

### Phase 4 — Colors & Themes
- `colors-themes/Palette.md` — human-readable swatches with HEX + HSL
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
- Generate `favicon.ico` + `favicon.png` inside the project folder
- Copy them to repo root (per-project: repo-root favicon reflects most-recently-created project)
- Update `index.html` `<link rel="icon">` to `/favicon.png`

### Phase 6 — README
`Projects/{Seq}-{PascalCaseProjectName}/README.md` with sections:
1. Overview (name, idea, voice/tone)
2. Logo Variants (embed all SVGs via relative paths)
3. Image Samples (embed 3 PNGs)
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
3. `icons-image/` has 2–3 raster samples at agreed dimensions
4. `Palette.md` + `Tokens.json` (flat PascalCase) exist
5. `favicon.ico`/`favicon.png` exist at repo root, referenced from `index.html`
6. README renders all assets via relative paths on GitHub
7. Instruction stored in memory (see Memory Persistence)
8. `mem://index.md` Core updated with one-liner

## Resolved Open Questions
1. Favicon — **per-project only** (repo root reflects active/most-recent)
2. `Tokens.json` schema — **flat PascalCase**
3. Raster sample sizes — **512 icon, 1024 light mockup, 1024 dark mockup** (optional 52/128/256 extra icon set)
4. Dark/white variants — **default ON**

## Trigger Phrases
`create logo`, `make logo`, `logo`, `design logo`, `new logo`, `brand mark`
