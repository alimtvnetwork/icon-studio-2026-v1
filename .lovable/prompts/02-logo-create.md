# 02 — Logo Creation

**Triggers:** `create logo`, `make logo`, `logo`, `create icon`, `make icon`, `design logo`, `new logo`, `brand mark`

This prompt is the single source of truth for every logo/icon request.
It lives in the project file system. Do **not** mirror it into `mem://`.

---

## 1. Inputs (from user)

| Field | Required | Default | Description |
|---|---|---|---|
| `ProductName` | yes | — | Name of product, converted to PascalCase |
| `ProductIdea` | yes | — | Short product concept, problem solved, functional context |
| `VoiceTone` | yes | — | Personality (e.g. playful & friendly, professional with quiet wink, modern tech-forward) |
| `SampleColors[]` | yes | — | Base color hint(s) expanded into cohesive palette |
| `NeedsDarkWhiteVariants` | no | **true** | Generates `Logo-Dark.svg` and `Logo-White.svg` |

If any required input is missing, ask before proceeding.

---

## 2. Outputs

a. Project folder under `Projects/{NN}-{PascalCaseProductName}/`
b. SVG icons in `icons-svg/` (`Logo.svg`, `Logo-Dark.svg`, `Logo-White.svg`, optional `Logo-Animated.svg`)
c. Raster samples in `icons-image/` (mixed set: 52, 128, 256, 512, 1024-Light, 1024-Dark, optional `Logo-Animated.gif`)
d. Color & theme tokens in `colors-themes/` (`Palette.md`, `Tokens.json`)
e. `favicon.ico` + `favicon.png` at **repo root** (per-project, regenerated)
f. `gif-animation.gif` at **repo root** (logo animation preview)
g. Project `README.md` rendering all assets via relative paths for GitHub markdown preview

---

## 3. Folder Structure

```
/ (repo root)
├── favicon.ico
├── favicon.png
├── gif-animation.gif
└── Projects/
    ├── 01-{PascalCaseProductName}/
    │   ├── README.md
    │   ├── favicon.ico
    │   ├── favicon.png
    │   ├── icons-svg/
    │   │   ├── Logo.svg
    │   │   ├── Logo-Dark.svg
    │   │   ├── Logo-White.svg
    │   │   └── Logo-Animated.svg
    │   ├── icons-image/
    │   │   ├── Logo-052.png
    │   │   ├── Logo-128.png
    │   │   ├── Logo-256.png
    │   │   ├── Logo-512.png
    │   │   ├── Logo-1024-Light.png
    │   │   ├── Logo-1024-Dark.png
    │   │   └── Logo-Animated.gif
    │   └── colors-themes/
    │       ├── Palette.md
    │       └── Tokens.json
    ├── 02-{PascalCaseProductName}/
    └── 03-{PascalCaseProductName}/
```

Rules:
1. PascalCase everywhere reasonable (folders, files, JSON keys/values).
2. Sequence is zero-padded two digits, starting at `01`.
3. Never overwrite an existing project folder — always create the next sequence.
4. Favicon and GIF live both inside project folder and mirrored to repo root for active preview.

---

## 4. Phased Execution (one phase per `next` from user)

### Phase 0 — Input Capture & Confirmation
- Validate inputs: `ProductName`, `ProductIdea`, `VoiceTone`, `SampleColors[]`, `NeedsDarkWhiteVariants`.
- Determine next zero-padded sequence by scanning `Projects/`.
- Echo back `{Seq}-{PascalCaseProductName}` and resolved palette to user.

### Phase 1 — Project Scaffold
- Create `Projects/{Seq}-{PascalCaseProductName}/`.
- Create subfolders: `icons-svg/`, `icons-image/`, `colors-themes/`.

### Phase 2 — SVG Icon Generation
- `icons-svg/Logo.svg` (primary, full color).
- If variants ON (default):
  - `icons-svg/Logo-Dark.svg` (for dark backgrounds).
  - `icons-svg/Logo-White.svg` (single-color white on dark/transparent).
- Optional: `icons-svg/Logo-Animated.svg` (SMIL, looping).
- Clean, semantic vector geometry, no embedded raster.

### Phase 3 — Raster Image Samples (mixed set)
- `Logo-052.png` — 52×52 icon
- `Logo-128.png` — 128×128 icon (Chrome toolbar / extension default)
- `Logo-256.png` — 256×256 icon
- `Logo-512.png` — 512×512 hi-res icon
- `Logo-1024-Light.png` — 1024×1024 mockup context on light background
- `Logo-1024-Dark.png` — 1024×1024 mockup context on dark background
- Optional: `Logo-Animated.gif` — animated loop preview

### Phase 4 — Colors & Themes
- `colors-themes/Palette.md` — human-readable swatch table with HEX, HSL, and semantic usage.
- `colors-themes/Tokens.json` — **flat PascalCase keys**:
  ```json
  {
    "Primary": "#...",
    "PrimaryGlow": "#...",
    "Secondary": "#...",
    "Accent": "#...",
    "Background": "#...",
    "Foreground": "#...",
    "Muted": "#...",
    "Border": "#..."
  }
  ```

### Phase 5 — Favicon + Animation
- Generate `favicon.ico` and `favicon.png` inside project folder and mirrored to repo root.
- Generate `gif-animation.gif` at repo root if animated variant is included.
- Update `index.html` `<link rel="icon">` to reference `/favicon.ico`.

### Phase 6 — README Generation
- Create `Projects/{Seq}-{PascalCaseProductName}/README.md`.
- Use **relative paths only** so GitHub renders all assets inline.
- Standard sections:
  1. **Overview** — product name, idea, voice/tone, identity summary
  2. **Logo Variants** — visual table of `Logo.svg`, `Logo-Dark.svg`, `Logo-White.svg`
  3. **Animated** (if present) — `Logo-Animated.svg` and `Logo-Animated.gif`
  4. **Image Samples** — table of raster icons and 1024 mockups
  5. **Color Palette** — table with HEX, HSL, and links to `Palette.md`
  6. **Theme Tokens** — reference to `Tokens.json`
  7. **Favicon** — preview and notes
  8. **Usage** — HTML, CSS custom properties, and Tailwind config snippets

### Phase 7 — Verification
- Confirm all acceptance criteria below pass and summarize created assets.

---

## 5. Acceptance Criteria

1. `Projects/{Seq}-{PascalCaseProductName}/` exists with `icons-svg/`, `icons-image/`, `colors-themes/`, and `README.md`.
2. `Logo.svg` exists; with variants ON (default), both `Logo-Dark.svg` and `Logo-White.svg` exist.
3. `icons-image/` contains the full raster set: 52, 128, 256, 512, 1024-Light, 1024-Dark.
4. `Palette.md` and `Tokens.json` exist; `Tokens.json` uses flat PascalCase keys.
5. `favicon.ico` and `favicon.png` exist at project level and repo root.
6. Project `README.md` renders all assets correctly on GitHub (relative paths, no broken links).
7. This prompt is saved at `.lovable/prompts/02-logo-create.md` and indexed in `.lovable/prompts.md`. **No entries in `mem://`.**

---

## 6. Resolved Decisions

| Decision | Resolved Value |
|---|---|
| Favicon Scope | Generated per project, mirrored to repo root |
| `Tokens.json` Shape | Flat PascalCase keys (`Primary`, `PrimaryGlow`, etc.) |
| Raster Sample Sizes | 52, 128, 256, 512, 1024-Light, 1024-Dark |
| Dark/White Variants Default | **ON** |
| Animation Assets | SVG animation (`Logo-Animated.svg`) & GIF (`Logo-Animated.gif`) |
| Instruction Storage | File system only (`.lovable/prompts/`), never `mem://` |
