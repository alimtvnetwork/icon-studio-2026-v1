# 02 — Logo Creation

**Triggers:** `create logo`, `make logo`, `logo`, `create icon`, `make icon`

This prompt is the single source of truth for every logo/icon request.
It lives in the project file system. Do **not** mirror it into `mem://`.

---

## 1. Inputs (from user)

| Field | Required | Default |
|---|---|---|
| `ProductName` | yes | — |
| `ProductIdea` (short) | yes | — |
| `VoiceTone` | yes | — |
| `SampleColors[]` | yes | — |
| `NeedsDarkWhiteVariants` | no | **true** |

If any required input is missing, ask before proceeding.

---

## 2. Outputs

a. Project folder under `Projects/`
b. SVG icons in `icons-svg/` (`Logo.svg`, `Logo-Dark.svg`, `Logo-White.svg`)
c. Raster samples in `icons-image/` (mixed set, see §4)
d. Color & theme tokens in `colors-themes/` (`Palette.md`, `Tokens.json`)
e. `favicon.ico` + `favicon.png` at **repo root** (per-project, regenerated)
f. `gif-animation.gif` at **repo root** (logo animation)
g. Project `README.md` rendering all assets via relative paths

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
    │   ├── icons-svg/
    │   │   ├── Logo.svg
    │   │   ├── Logo-Dark.svg
    │   │   └── Logo-White.svg
    │   ├── icons-image/
    │   │   ├── Logo-052.png
    │   │   ├── Logo-128.png
    │   │   ├── Logo-256.png
    │   │   ├── Logo-512.png
    │   │   ├── Logo-1024-Light.png
    │   │   └── Logo-1024-Dark.png
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
4. Favicon and GIF live at repo root only; regenerated per project.

---

## 4. Phased Execution (one phase per `next` from user)

### Phase 1 — Input Capture & Scaffold
- Validate inputs; ask for missing fields.
- Detect/create `Projects/`.
- Determine next zero-padded sequence by listing existing `Projects/NN-*`.
- Create `Projects/{NN}-{PascalCaseProductName}/` with the three subfolders.

### Phase 2 — SVG Icon Generation
- `icons-svg/Logo.svg` (primary, full color).
- If variants ON (default): `Logo-Dark.svg` (for light bg) + `Logo-White.svg` (for dark bg).
- Clean, optimized, no embedded raster.

### Phase 3 — Raster Image Samples (mixed set)
- `Logo-052.png` — 52×52
- `Logo-128.png` — 128×128
- `Logo-256.png` — 256×256
- `Logo-512.png` — 512×512 (icon)
- `Logo-1024-Light.png` — 1024×1024 mockup on light bg
- `Logo-1024-Dark.png` — 1024×1024 mockup on dark bg

### Phase 4 — Colors & Themes
- `Palette.md` — swatches with HEX + HSL.
- `Tokens.json` — **flat PascalCase keys**:
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

### Phase 5 — Favicon + Animation
- Generate `favicon.ico` and `favicon.png` at repo root (overwrite previous).
- Generate `gif-animation.gif` at repo root (logo animation, looping, tasteful).
- Update `index.html` `<link rel="icon">` to reference the new favicon.

### Phase 6 — README Generation
- Create `Projects/{NN}-{PascalCaseProductName}/README.md`.
- Use **relative paths only** so GitHub renders inline.
- Sections (in order):
  1. **Overview** — product name, idea, voice/tone
  2. **Logo Variants** — embed `Logo.svg`, `Logo-Dark.svg`, `Logo-White.svg`
  3. **Image Samples** — embed all 6 PNGs
  4. **Animation** — embed `../../gif-animation.gif`
  5. **Color Palette** — swatches with HEX/HSL
  6. **Theme Tokens** — code block of `Tokens.json`
  7. **Favicon** — preview + path note
  8. **Usage** — short guidance per variant

### Phase 7 — Verification
Confirm all acceptance criteria below pass.

---

## 5. Acceptance Criteria

1. `Projects/{NN}-{PascalCaseProductName}/` exists with `icons-svg/`, `icons-image/`, `colors-themes/`, plus `README.md`.
2. `Logo.svg` exists; with variants ON, both `Logo-Dark.svg` and `Logo-White.svg` exist.
3. `icons-image/` contains the full mixed raster set: 52, 128, 256, 512, 1024-Light, 1024-Dark.
4. `Palette.md` and `Tokens.json` exist; `Tokens.json` uses flat PascalCase keys.
5. `favicon.ico` and `favicon.png` exist at repo root and are referenced from `index.html`.
6. `gif-animation.gif` exists at repo root.
7. Project `README.md` renders all assets correctly on GitHub (relative paths).
8. This prompt is saved at `.lovable/prompts/02-logo-create.md` and indexed in `.lovable/prompts.md`. **No entries in `mem://`.**

---

## 6. Resolved Defaults

| Decision | Value |
|---|---|
| Favicon scope | Per-project; regenerated at repo root |
| `Tokens.json` schema | Flat PascalCase |
| Raster sample sizes | 52, 128, 256, 512, 1024-Light, 1024-Dark |
| Dark/white variants default | ON |
| Animation | `gif-animation.gif` at repo root |

---

## 7. Coding Guidelines (apply when generating any code)

Read `.lovable/coding-guidelines.md` and `/spec/**` first. Hard rules:
- Functions ≤ 8 lines, files ≤ 100 lines
- No nested or negative `if`s
- Strict types — no `any` / `unknown` / bare `interface{}`
- No swallowed errors, no magic strings
- One definition per file
- Boolean prefixes: `is` / `has`
- DRY first

---

## 8. Continuation Protocol

- Spec is persisted. Wait for user `next` + brief (ProductName, ProductIdea, VoiceTone, SampleColors, optional variants flag).
- Execute Phases 1–7 in order. Pause only on missing required input.
