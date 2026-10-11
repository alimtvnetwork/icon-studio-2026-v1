# Logo Creation Instruction (Canonical Spec)

Triggers: `create logo`, `make logo`, `logo`, `new logo`, `design logo`, `create icon`

> Source of truth: this file. **Do NOT mirror this spec into `mem://`** — project file system only.
> Before any implementation, read `.lovable/coding-guidelines.md` plus boolean / language / enum / error-management guidelines under `/spec/**`. Hard rules: functions ≤ 8 lines, files ≤ 100 lines, no nested or negative ifs, strict types (no `any` / `unknown` / `interface{}`), no swallowed errors, no magic strings, definitions in their own files, `is` / `has` boolean prefixes, DRY first.

## Inputs (provided by user)
- `ProductName` (required)
- `ProductIdea` — short description, voice, tone (required)
- `VoiceTone` — e.g. playful, premium, technical (required)
- `SampleColors[]` — hex/HSL hints (optional; ask if missing)
- `NeedsDarkWhiteVariants` (boolean, **default: ON**)

If any required input is missing, ask before generating.

## Outputs
- Project folder under `Projects/`
- SVG icons (primary + dark/white when applicable)
- 6 raster image samples (mixed sizes)
- Color & theme tokens
- `gif-animation.gif` at **repo root** (animation for the icon, regenerated per project)
- `favicon.ico` + `favicon.png` at **repo root** (regenerated per project)
- `README.md` inside the project folder, rendering all assets via relative paths

## Folder Structure
```
/ (repo root)
├── gif-animation.gif            # animation for the latest project icon
├── favicon.ico                  # regenerated per project
├── favicon.png                  # regenerated per project
└── Projects/
    └── {Seq}-{PascalCaseProjectName}/
        ├── README.md
        ├── icons-svg/
        │   ├── Logo.svg
        │   ├── Logo-Dark.svg     # if NeedsDarkWhiteVariants
        │   └── Logo-White.svg    # if NeedsDarkWhiteVariants
        ├── icons-image/
        │   ├── Logo-052.png            # 52×52
        │   ├── Logo-128.png            # 128×128
        │   ├── Logo-256.png            # 256×256
        │   ├── Logo-512.png            # 512×512 icon
        │   ├── Logo-1024-Light.png     # 1024×1024 light-background mockup
        │   └── Logo-1024-Dark.png      # 1024×1024 dark-background mockup
        └── colors-themes/
            ├── Palette.md
            └── Tokens.json
```

## Naming Rules
- Project folder: `{Seq}-{PascalCaseProjectName}` (e.g. `01-AcmePay`)
- `Seq` is zero-padded 2-digit, starting at `01`, **never reused**
- All folder/file names use PascalCase where reasonable
- Never overwrite an existing project folder — always create the next sequence

## Tokens.json Schema (flat PascalCase)
```json
{
  "Primary": "#RRGGBB",
  "PrimaryGlow": "#RRGGBB",
  "Background": "#RRGGBB",
  "Foreground": "#RRGGBB",
  "Accent": "#RRGGBB",
  "Muted": "#RRGGBB",
  "Border": "#RRGGBB"
}
```

## Repo-Root Assets (regenerated per project)
- `favicon.ico` + `favicon.png` — update `<link rel="icon">` in `index.html` to `/favicon.png`
- `gif-animation.gif` — short looping animation of the icon (subtle reveal / pulse / morph)

## README.md (per project) — required sections
1. Overview (ProductName, ProductIdea, VoiceTone)
2. Logo Variants (embed all SVGs)
3. Image Samples (embed all rasters)
4. Color Palette (swatches w/ HEX + HSL)
5. Theme Tokens (Tokens.json snippet)
6. Favicon (preview)
7. Animation (embed `../../gif-animation.gif`)
8. Usage (how to import / embed)

All paths relative so GitHub renders inline.

## Phased Execution Protocol
The user drives progress via `next`. Each phase = one tool batch + brief confirmation, then wait.

- Phase 0: Capture inputs / confirm; reserve sequence number
- Phase 1: Scaffold `Projects/{Seq}-{Name}/` + subfolders
- Phase 2: Generate `Logo.svg` (+ Dark/White if needed)
- Phase 3: Generate 6 raster samples (52, 128, 256, 512, 1024-Light, 1024-Dark)
- Phase 4: Generate `Palette.md` + `Tokens.json`
- Phase 5: Generate root `favicon.ico` + `favicon.png`, update `index.html`
- Phase 6: Generate root `gif-animation.gif`
- Phase 7: Generate project `README.md`
- Phase 8: Final QA — verify all files, no broken links

> **Finalize directive**: when executing, generate all animations and designs in one shot as much as possible within each phase batch.

## Acceptance Criteria
1. `Projects/{Seq}-{PascalCaseProjectName}/` exists with subfolders `icons-svg/`, `icons-image/`, `colors-themes/`, plus `README.md`.
2. `Logo.svg` exists; `Logo-Dark.svg` + `Logo-White.svg` exist when default-ON.
3. `icons-image/` contains all 6 rasters: `Logo-052`, `Logo-128`, `Logo-256`, `Logo-512`, `Logo-1024-Light`, `Logo-1024-Dark`.
4. `Palette.md` + `Tokens.json` exist; flat PascalCase keys.
5. `favicon.ico` + `favicon.png` + `gif-animation.gif` at repo root; favicon referenced from `index.html`.
6. README renders all assets via relative paths (no broken links on GitHub).
7. This spec lives at `.lovable/prompts/02-logo-create.md` and is indexed in `.lovable/prompts.md`.
8. No `mem://` entries store this instruction — file system is the single source of truth.

## Important
- PascalCase everywhere reasonable
- Sequence numbers zero-padded, monotonically increasing, never reused
- README uses relative paths only
- Favicon + gif-animation always at repo root, regenerated per project
- Never overwrite an existing project folder
- Dark + white variants default ON unless user opts out
- All prompts live under `.lovable/prompts/`; never in `mem://`
