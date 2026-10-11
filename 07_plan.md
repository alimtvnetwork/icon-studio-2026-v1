# Logo Creation Workflow — Plan

Canonical spec: `.lovable/prompts/02-logo-create.md`. This plan is the phased
execution checklist Lovable runs whenever the user asks to create a logo.

## Resolved decisions (from user)
1. Favicon: repo-root, regenerated per project; `index.html` updated each time.
2. `gif-animation.gif`: repo-root, regenerated per project.
3. `Tokens.json` shape: flat PascalCase keys
   (`Primary`, `PrimaryGlow`, `Background`, `Foreground`, `Accent`).
4. Raster sample set (mixed):
   - `Logo-052.png` — 52×52 icon
   - `Logo-128.png` — 128×128 icon
   - `Logo-256.png` — 256×256 icon
   - `Logo-512.png` — 512×512 icon
   - `Logo-1024-Light.png` — 1024×1024 light-bg mockup
   - `Logo-1024-Dark.png` — 1024×1024 dark-bg mockup
5. Dark + white SVG variants: ON by default.
6. Instruction storage: project file system only (`.lovable/prompts/`).
   Never write logo rules to `mem://`.

## Inputs required from user (per logo task)
- `ProductName` (required)
- `ProductIdea` / short description (required)
- `VoiceTone` (required — e.g. playful, premium, technical)
- `SampleColors[]` (required — at least one hex or palette hint)
- `NeedsDarkWhiteVariants` (optional, default `true`)

If any required input is missing, ask before scaffolding.

## Phased execution (advance only when user says `next`)

### Phase 0 — Capture & confirm
- Validate inputs; determine next zero-padded sequence under `Projects/`.
- Echo back `{Seq}-{PascalCaseProductName}` and resolved palette.

### Phase 1 — Scaffold
- Create `Projects/{Seq}-{PascalCaseProductName}/` with subfolders
  `icons-svg/`, `icons-image/`, `colors-themes/`.

### Phase 2 — SVG icons
- `icons-svg/Logo.svg` (primary).
- If `NeedsDarkWhiteVariants` (default true): `Logo-Dark.svg`, `Logo-White.svg`.

### Phase 3 — Raster samples (6 files)
- `Logo-052.png`, `Logo-128.png`, `Logo-256.png`, `Logo-512.png`,
  `Logo-1024-Light.png`, `Logo-1024-Dark.png`.

### Phase 4 — Colors & themes
- `colors-themes/Palette.md` — HEX + HSL swatches.
- `colors-themes/Tokens.json` — flat PascalCase keys.

### Phase 5 — Favicon + animation (repo root)
- Generate `favicon.ico`, `favicon.png`, `gif-animation.gif` at repo root.
- Update `index.html` `<link rel="icon">`. Remove stale `public/favicon.ico`.

### Phase 6 — README
- `Projects/{Seq}-{PascalCaseProductName}/README.md` with sections:
  Overview, Logo Variants, Image Samples, Color Palette, Theme Tokens,
  Favicon, Animation, Usage. Relative paths only.

### Phase 7 — Verify
- Confirm acceptance criteria. Summarize created files.

## Hard rules
1. PascalCase for folder names, file names, and JSON keys.
2. Sequence numbers zero-padded two-digit (`01`, `02`, ...).
3. Never overwrite an existing project folder — always next sequence.
4. README uses relative paths.
5. Favicon + animation live at repo root, regenerated per project.
6. Wait for `next` between phases.
7. Project file system is the single source of truth — never persist logo
   rules to `mem://`.