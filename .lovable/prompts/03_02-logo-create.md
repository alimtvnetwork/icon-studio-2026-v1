# Logo Creation Workflow (Spec)

Triggers: `create logo`, `make logo`, `logo`, `new logo`, `design logo`, `create icon`

## Source of Truth
This spec lives **only in the project file system** at `.lovable/prompts/02-logo-create.md`, indexed by `.lovable/prompts.md`. **Never** persist this instruction to `mem://`.

## Coding Guidelines
Before any implementation, read `.lovable/coding-guidelines.md` and applicable `/spec/**` rules. Hard rules: functions ≤ 8 lines, files ≤ 100 lines, no nested/negative ifs, strict types (no `any`/`unknown`), no swallowed errors, no magic strings, definitions in their own files, `is`/`has` boolean prefixes, DRY first.

## Inputs (from user)
- `ProductName` (required)
- `ProductIdea` — short description (required)
- `VoiceTone` — voice/tone (required)
- `SampleColors[]` — palette hint HEX/HSL (optional, infer if missing)
- `NeedsDarkWhiteVariants` — boolean. **Default: ON**.

If any required input is missing → ask before generating.

## Folder Structure
```
/ (repo root)
├── favicon.ico                  # per-project, regenerated each new logo
├── favicon.png
├── gif-animation.gif            # animated icon at repo root
└── Projects/
    ├── 01-{PascalCaseProjectName}/
    │   ├── README.md
    │   ├── icons-svg/
    │   │   ├── Logo.svg
    │   │   ├── Logo-Dark.svg        (if NeedsDarkWhiteVariants)
    │   │   └── Logo-White.svg       (if NeedsDarkWhiteVariants)
    │   ├── icons-image/
    │   │   ├── Logo-052.png             # 52×52
    │   │   ├── Logo-128.png             # 128×128
    │   │   ├── Logo-256.png             # 256×256
    │   │   ├── Logo-512.png             # 512×512
    │   │   ├── Logo-1024-Light.png      # 1024×1024 light bg mockup
    │   │   └── Logo-1024-Dark.png       # 1024×1024 dark bg mockup
    │   └── colors-themes/
    │       ├── Palette.md
    │       └── Tokens.json
    ├── 02-{PascalCaseProjectName}/
    └── 03-{PascalCaseProjectName}/
```

### Naming
- Project folder: `{NN}-{PascalCaseProjectName}` — `NN` zero-padded, starts at `01`, increments by scanning `Projects/`.
- PascalCase for folders, files, JSON keys.
- **Never overwrite** an existing project folder — always next sequence.

## Actionable Phases

### Phase 1 — Scaffold
1. Ensure `Projects/` exists.
2. Determine next `NN` (max existing + 1, padded).
3. Create `Projects/{NN}-{PascalCaseName}/` with subfolders `icons-svg/`, `icons-image/`, `colors-themes/`.

### Phase 2 — SVG Icons
1. `icons-svg/Logo.svg` (clean vector, viewBox `0 0 512 512`, no raster embeds).
2. If `NeedsDarkWhiteVariants` (default true):
   - `Logo-Dark.svg` — for dark backgrounds.
   - `Logo-White.svg` — pure white/monochrome.

### Phase 3 — Raster Samples (mixed set)
Generate via imagegen:
1. `Logo-052.png` — 52×52
2. `Logo-128.png` — 128×128
3. `Logo-256.png` — 256×256
4. `Logo-512.png` — 512×512 icon
5. `Logo-1024-Light.png` — 1024×1024 light-bg mockup
6. `Logo-1024-Dark.png` — 1024×1024 dark-bg mockup

### Phase 4 — Colors & Themes
1. `colors-themes/Palette.md` — swatches: name, HEX, HSL, usage.
2. `colors-themes/Tokens.json` — flat PascalCase:
   ```json
   {
     "Primary": "#...",
     "PrimaryGlow": "#...",
     "Background": "#...",
     "Foreground": "#...",
     "Accent": "#...",
     "Muted": "#...",
     "Border": "#..."
   }
   ```

### Phase 5 — Favicon + Animation (repo root, per-project)
1. `favicon.png` (256×256) at repo root from the logo mark.
2. `favicon.ico` at repo root.
3. `gif-animation.gif` at repo root — animated version of the icon.
4. Update `index.html` `<link rel="icon">` to `/favicon.png` (remove conflicting `.ico` link if needed).

### Phase 6 — README
`Projects/{NN}-{PascalCaseName}/README.md` with sections: Overview, Logo Variants, Image Samples, Color Palette, Theme Tokens, Favicon, Animation, Usage. Embed all assets via **relative paths** so GitHub renders inline (favicon + gif via `../../favicon.png`, `../../gif-animation.gif`).

### Phase 7 — Instruction Persistence (file system only)
- Spec at `.lovable/prompts/02-logo-create.md`.
- Indexed in `.lovable/prompts.md` with triggers.
- **Do not** write to `mem://`.

## Acceptance Criteria
1. `Projects/{NN}-{PascalCaseName}/` exists with `icons-svg/`, `icons-image/`, `colors-themes/`, `README.md`.
2. `Logo.svg` present; dark/white variants when applicable.
3. `icons-image/` contains: 52, 128, 256, 512, 1024-Light, 1024-Dark.
4. `Palette.md` + `Tokens.json` (flat PascalCase) present.
5. `favicon.ico`, `favicon.png`, `gif-animation.gif` at repo root; favicon referenced in `index.html`.
6. README renders all assets via relative paths on GitHub.
7. Spec saved at `.lovable/prompts/02-logo-create.md` and indexed in `.lovable/prompts.md`.
8. No `mem://` entries for this instruction.

## Resolved FAQs
1. Favicon: **per-project**, regenerated each new logo.
2. Tokens.json: **flat PascalCase**.
3. Raster sizes: **52, 128, 256, 512, 1024-Light, 1024-Dark**.
4. Dark/white variants: **default ON**.

## Execution Protocol
- Plan in `plan.md` first.
- Wait for user `next` to advance phases.
- Each new logo request = new sequence folder, never overwrite.
- All animations and designs in one shot when possible.
