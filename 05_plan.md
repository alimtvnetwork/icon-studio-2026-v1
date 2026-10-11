# Logo Creation — Plan

> **Source of truth:** [`.lovable/prompts/02-logo-create.md`](./.lovable/prompts/02-logo-create.md)
> Indexed in [`.lovable/prompts.md`](./.lovable/prompts.md). Not stored in `mem://`.

## Phases (run on user `next`)

- **Phase 0 — Spec Persistence** ✅
  Saved spec to `.lovable/prompts/02-logo-create.md`, indexed in `.lovable/prompts.md`, mirrored summary here.
- **Phase 1 — Scaffold** — create `Projects/{NN}-{PascalName}/` + subfolders.
- **Phase 2 — SVG icons** — `Logo.svg` (+ Dark/White variants by default).
- **Phase 3 — Raster set** — 52, 128, 256, 512, 1024-Light, 1024-Dark PNGs.
- **Phase 4 — Colors & Themes** — `Palette.md` + flat-PascalCase `Tokens.json`.
- **Phase 5 — Favicon + Animation** — `favicon.ico`, `favicon.png`, `gif-animation.gif` at repo root; update `index.html`.
- **Phase 6 — README** — embed all assets via relative paths.
- **Phase 7 — Verification** — check all acceptance criteria.

## Required Inputs

`ProductName`, `ProductIdea`, `VoiceTone`, `SampleColors[]`, optional `NeedsDarkWhiteVariants` (default ON).

## Status

Phase 0 complete. Waiting for the user to send `next` + the logo brief.
