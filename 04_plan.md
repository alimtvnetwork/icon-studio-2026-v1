# Logo Project Plan

## Spec
Canonical spec: [.lovable/prompts/02-logo-create.md](./.lovable/prompts/02-logo-create.md).
Index: [.lovable/prompts.md](./.lovable/prompts.md).

> Spec lives in the file system only — **not** in `mem://`.

## Resolved Decisions
1. **Favicon scope** → per-project; root `favicon.ico` / `favicon.png` regenerated each project.
2. **`gif-animation.gif`** → repo root, regenerated per project.
3. **`Tokens.json`** → flat PascalCase (`Primary`, `PrimaryGlow`, `Background`, `Foreground`, `Accent`, `Muted`, `Border`).
4. **Raster sizes** → 52, 128, 256, 512, 1024-Light, 1024-Dark (6 files).
5. **Dark/White variants** → default **ON**.
6. **Coding guidelines** → read `.lovable/coding-guidelines.md` + `/spec/**` before any code.

## Folder Convention
```
Projects/{Seq}-{PascalCaseProjectName}/
  ├── README.md
  ├── icons-svg/   (Logo.svg [+ Logo-Dark.svg, Logo-White.svg])
  ├── icons-image/ (Logo-052/128/256/512.png, Logo-1024-Light.png, Logo-1024-Dark.png)
  └── colors-themes/ (Palette.md, Tokens.json)
gif-animation.gif, favicon.ico, favicon.png  (repo root, latest project)
```

## Sequence Tracker
Next sequence: **01**

| Seq | ProductName | Status |
|-----|-------------|--------|
| 01  | _pending_   | _awaiting `next` + brief_ |

## Phase Execution (driven by user `next`)
- [ ] Phase 0 — Capture inputs (ProductName, ProductIdea, VoiceTone, SampleColors, NeedsDarkWhiteVariants)
- [ ] Phase 1 — Scaffold `Projects/{Seq}-{Name}/` + subfolders
- [ ] Phase 2 — Generate SVG logo(s)
- [ ] Phase 3 — Generate 6 raster samples
- [ ] Phase 4 — Generate `Palette.md` + `Tokens.json`
- [ ] Phase 5 — Generate root favicon + update `index.html`
- [ ] Phase 6 — Generate root `gif-animation.gif`
- [ ] Phase 7 — Generate project `README.md`
- [ ] Phase 8 — QA: verify all files exist, README links resolve
