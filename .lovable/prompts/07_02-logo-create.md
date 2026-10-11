# Prompt 02 — Logo Create (verbatim spec)

Triggers: `create logo`, `make logo`, `logo`, `design logo`, `generate logo`, `create icon`

Source of truth: this file. Do NOT mirror these rules to `mem://`.

## Inputs (provided by user)
- `ProductName` (required)
- `ProductIdea` / short product idea (required)
- `VoiceTone` (required — e.g. playful, premium, technical)
- `SampleColors[]` (required — at least one hex or palette hint)
- `NeedsDarkWhiteVariants` (optional, default `true`)

If any required input is missing, ask before scaffolding.

## Outputs
- Project folder under `Projects/`
- SVG icons in `icons-svg/`
- Raster image samples in `icons-image/` (mixed size set)
- Dark + white SVG variants when required (default ON)
- Color and theme tokens in `colors-themes/`
- Per-project `README.md` rendering all assets via relative paths
- Repo-root `favicon.ico` + `favicon.png` (regenerated per project)
- Repo-root `gif-animation.gif` (regenerated per project)
- `index.html` `<link rel="icon">` updated to point at the new favicon

## Folder Structure
```
/ (repo root)
├── favicon.ico              # regenerated per project
├── favicon.png              # regenerated per project
├── gif-animation.gif        # regenerated per project
└── Projects/
    ├── 01-{PascalCaseProjectName}/
    │   ├── README.md
    │   ├── icons-svg/
    │   │   ├── Logo.svg
    │   │   ├── Logo-Dark.svg
    │   │   └── Logo-White.svg
    │   ├── icons-image/
    │   │   ├── Logo-052.png        # 52×52 icon
    │   │   ├── Logo-128.png        # 128×128 icon
    │   │   ├── Logo-256.png        # 256×256 icon
    │   │   ├── Logo-512.png        # 512×512 icon
    │   │   ├── Logo-1024-Light.png # 1024×1024 light-bg mockup
    │   │   └── Logo-1024-Dark.png  # 1024×1024 dark-bg mockup
    │   └── colors-themes/
    │       ├── Palette.md
    │       └── Tokens.json
    ├── 02-{PascalCaseProjectName}/
    └── 03-{PascalCaseProjectName}/
```

## Resolved decisions
1. Favicon: **repo root**, regenerated per project. `index.html` is updated to
   reference the new files. Delete any stale `public/favicon.ico` so the
   browser does not auto-serve the old one.
2. `gif-animation.gif`: **repo root**, regenerated per project (same scope as
   favicon).
3. `Tokens.json`: flat PascalCase keys
   (`Primary`, `PrimaryGlow`, `Background`, `Foreground`, `Accent`).
4. Raster sample set (mixed): `Logo-052.png`, `Logo-128.png`, `Logo-256.png`,
   `Logo-512.png`, `Logo-1024-Light.png`, `Logo-1024-Dark.png`.
5. Dark + white SVG variants: ON by default.
6. Instruction storage: project file system only (`.lovable/prompts/`).
   Never write logo rules to `mem://`.

## Phased execution (advance only when user says `next`)

### Phase 0 — Capture & confirm
- Validate inputs; ask for any missing required input.
- Determine next zero-padded sequence by scanning `Projects/`.
- Echo back `{Seq}-{PascalCaseProductName}` and resolved palette.

### Phase 1 — Scaffold
- Create `Projects/{Seq}-{PascalCaseProductName}/` with subfolders
  `icons-svg/`, `icons-image/`, `colors-themes/`.
- Never overwrite an existing project folder.

### Phase 2 — SVG icons
- `icons-svg/Logo.svg` (primary, full color).
- If `NeedsDarkWhiteVariants` (default true):
  - `icons-svg/Logo-Dark.svg` (for dark backgrounds)
  - `icons-svg/Logo-White.svg` (single-color white)

### Phase 3 — Raster samples
- Generate the full mixed set listed under Folder Structure (6 files).

### Phase 4 — Colors & themes
- `colors-themes/Palette.md` — swatches with HEX + HSL.
- `colors-themes/Tokens.json` — flat PascalCase keys.

### Phase 5 — Favicon + animation (repo root)
- Generate `favicon.ico` and `favicon.png` at repo root.
- Generate `gif-animation.gif` at repo root.
- Update `index.html` `<link rel="icon">` to reference the new favicon.
- Delete any stale `public/favicon.ico` if present.

### Phase 6 — README
- `Projects/{Seq}-{PascalCaseProductName}/README.md` with sections:
  Overview, Logo Variants, Image Samples, Color Palette, Theme Tokens,
  Favicon, Animation, Usage. All asset refs use **relative paths** so GitHub
  renders inline.

### Phase 7 — Verify
- Confirm acceptance criteria. Summarize created files.

## Hard rules
1. PascalCase for folder names, file names, and JSON keys.
2. Sequence numbers zero-padded two-digit (`01`, `02`, ...).
3. Never overwrite an existing project folder — always create the next sequence.
4. README uses relative paths.
5. Favicon + animation live at repo root, regenerated per project.
6. Wait for `next` between phases.
7. Do NOT persist logo rules to `mem://` — file system is the single source
   of truth.
8. Apply project coding guidelines from `.lovable/coding-guidelines.md` and
   `/spec/**` when those files exist (functions ≤8 lines, files ≤100 lines,
   no `any`/`unknown`, `is`/`has` boolean prefixes, no swallowed errors,
   no magic strings, DRY).

## Acceptance criteria
1. `Projects/{Seq}-{PascalCaseProductName}/` exists with `icons-svg/`,
   `icons-image/`, `colors-themes/`, and `README.md`.
2. `Logo.svg` exists; if dark/white requested (default ON), both
   `Logo-Dark.svg` and `Logo-White.svg` exist.
3. `icons-image/` contains all 6 raster samples at the specified sizes.
4. `Palette.md` and `Tokens.json` exist; `Tokens.json` uses PascalCase keys.
5. `favicon.ico`, `favicon.png`, and `gif-animation.gif` exist at repo root
   and `index.html` references the new favicon.
6. README renders all assets correctly on GitHub via relative paths.
7. This prompt remains saved at `.lovable/prompts/02-logo-create.md` and
   indexed in `.lovable/prompts.md`.
8. No logo-workflow entries are stored in `mem://`.