# Logo Creation — Plan

Spec: `.lovable/prompts/02-logo-create.md` (file system is the single source of truth — no `mem://`).

## Phases (advance on user `next`)
1. **Scaffold** — `Projects/{NN}-{PascalCaseName}/` with `icons-svg/`, `icons-image/`, `colors-themes/`.
2. **SVG Icons** — `Logo.svg` (+ `Logo-Dark.svg`, `Logo-White.svg` by default).
3. **Raster Samples** — `Logo-052/128/256/512.png`, `Logo-1024-Light.png`, `Logo-1024-Dark.png`.
4. **Colors & Themes** — `Palette.md` + `Tokens.json` (flat PascalCase).
5. **Favicon + Animation** — regenerate `favicon.ico`, `favicon.png`, `gif-animation.gif` at repo root; wire favicon into `index.html`.
6. **README** — embed all assets via relative paths for GitHub preview.
7. **Verify** — acceptance criteria checklist.

## Inputs needed per request
- ProductName
- ProductIdea
- VoiceTone
- SampleColors[] (optional)
- NeedsDarkWhiteVariants (default: true)

## Defaults (resolved)
- Favicon: per-project, regenerated.
- Tokens.json: flat PascalCase.
- Raster set: 52, 128, 256, 512, 1024-Light, 1024-Dark.
- Dark/white variants: ON by default.
- `gif-animation.gif` at repo root per project.

## Status
- [x] Spec rewritten (file-system only)
- [x] Index updated
- [x] Plan saved
- [ ] Awaiting first logo task (`next` + product details)
