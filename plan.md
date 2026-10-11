# Icon Studio 2026 — Master Plan & Architecture

> Authoritative architectural specification, project index, and execution roadmap for Icon Studio 2026.

Canonical logo specification: [`.lovable/prompts/02-logo-create.md`](./.lovable/prompts/02-logo-create.md).
Canonical memory specification: [`.lovable/prompts/01-write-memory.md`](./.lovable/prompts/01-write-memory.md).

---

## 1. Project Directory Status & Registry

Icon Studio maintains 5 active branding suites under [`Projects/`](./Projects/):

| Project | Sequence | Identity Concept | Status | Key Deliverables |
|---|---|---|---|---|
| **MacroMate** | `01-MacroMate` | Rounded "M" lettermark with play badge | Complete | 4 SVGs, 7 rasters, Palette, Tokens, Favicons |
| **MeetRecorder** | `01-MeetRecorder` | Geometric "M" tile with teal recording dot | Complete | 3 SVGs, 6 rasters, Palette, Tokens, Favicon |
| **LvExt (Default)** | `02-LvExt` | "L+X" monogram on pink-violet-indigo tile | Complete | 3 SVGs, 6 rasters, GIF animation, Tokens |
| **ScriptsFixer** | `02-ScriptsFixer` | `</>` code brackets with wrench badge + spark | Complete | 4 SVGs, 7 rasters, Palette, Tokens, Favicon |
| **LvExt (Reddish)** | `03-LvExt` | Coral/crimson monogram with golden connector | Complete | 3 SVGs, 6 rasters, Palette, Tokens |

---

## 2. Standardized Asset Specification

Every brand package generated under `Projects/{Seq}-{PascalCaseProjectName}/` adheres to the standardized output structure:

### 2.1 Vector Assets (`icons-svg/`)
- `Logo.svg`: Primary vector mark with rich color gradients.
- `Logo-Dark.svg`: High-contrast variant tailored for dark background presentation.
- `Logo-White.svg`: Monochrome clean white silhouette.
- `Logo-Animated.svg` (optional): Pure SMIL vector animation.

### 2.2 Raster Assets (`icons-image/`)
- `Logo-052.png`: 52×52 small toolbar preview.
- `Logo-128.png`: 128×128 standard extension / dock icon.
- `Logo-256.png`: 256×256 medium icon.
- `Logo-512.png`: 512×512 hi-res application icon.
- `Logo-1024-Light.png`: 1024×1024 mockup presentation on light background.
- `Logo-1024-Dark.png`: 1024×1024 mockup presentation on dark background.
- `Logo-Animated.gif` (optional): Looping preview GIF.

### 2.3 Design System & Theme Tokens (`colors-themes/`)
- `Palette.md`: Swatch table documenting HEX, HSL, and semantic application.
- `Tokens.json`: Flat PascalCase key-value mapping (`Primary`, `PrimaryGlow`, `Secondary`, `Accent`, `Background`, `Foreground`, `Muted`, `Border`).

### 2.4 Documentation & Previews
- `README.md`: Self-contained project documentation rendering all vectors, rasters, palette tables, and token snippets via relative GitHub markdown paths.

---

## 3. Phased Execution Protocol

Each brand identity is created through an automated phased cycle:

1. **Phase 0 — Capture & Confirm**: Capture `ProductName`, `ProductIdea`, `VoiceTone`, `SampleColors[]`. Determine next zero-padded `{Seq}`.
2. **Phase 1 — Scaffold**: Create `Projects/{Seq}-{PascalCaseProjectName}/` with `icons-svg/`, `icons-image/`, `colors-themes/`.
3. **Phase 2 — Vector Mark Creation**: Generate `Logo.svg`, `Logo-Dark.svg`, `Logo-White.svg`.
4. **Phase 3 — Raster Suite Generation**: Render 52px, 128px, 256px, 512px, and 1024px light/dark mockups.
5. **Phase 4 — Color & Token Generation**: Output `Palette.md` and `Tokens.json`.
6. **Phase 5 — Favicon & Animation**: Generate multi-res favicons and optional GIF animations.
7. **Phase 6 — README Assembly**: Build GitHub-optimized markdown preview.
8. **Phase 7 — Verification**: Validate relative links, file sizes, and asset integrity.

---

## 4. Completed Milestones

- [x] Initial workflow formalization and prompt specifications (`.lovable/prompts/`).
- [x] Project consolidation and deduplication across merged repositories.
- [x] MacroMate (`01-MacroMate`) canonical asset stabilization.
- [x] MeetRecorder (`01-MeetRecorder`) asset suite preservation.
- [x] LvExt (`02-LvExt` and `03-LvExt`) brand variants preservation.
- [x] ScriptsFixer (`02-ScriptsFixer`) brand assets and animations integration.
- [x] Master prompt index (`.lovable/prompts.md`) and root documentation unification.

---

## 5. Upcoming Roadmap

- [ ] Unified multi-brand web preview gallery in React/Vite.
- [ ] Automated export script for Chrome extension `manifest.json` generation across all projects.
- [ ] Open Graph (OG) social card image generation pipeline.
