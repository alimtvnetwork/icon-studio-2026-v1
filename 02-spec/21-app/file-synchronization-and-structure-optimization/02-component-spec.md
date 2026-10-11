# Component and Consolidation Specification: File Synchronization and Structure Optimization

## Scope of Consolidation

### 1. Root Configuration Files
All root configuration files across sequences `01_` through `07_` have verified identical SHA content hashes:
- `package.json`: Contains identical scripts (`dev`, `build`, `lint`, `test`) and React 18 / Vite / Tailwind / Shadcn UI dependencies. Collapsed to `package.json`.
- `package-lock.json` & `bun.lockb`: Collapsed to canonical lockfiles.
- `components.json`, `eslint.config.js`, `postcss.config.js`, `tailwind.config.ts`, `tsconfig*.json`, `vite.config.ts`, `vitest.config.ts`: Collapsed to root canonical files.
- `index.html`: Synthesize modern HTML shell with `<link rel="icon">` references and Lovable root script.
- `README.md` & `plan.md`: Synthesized into single canonical documents highlighting all 7 submodules and projects.

### 2. Source Tree (`src/`)
Every source file in `src/` has 100% identical SHA content across all 7 versions:
- `src/App.css` and `src/App.tsx`
- `src/index.css` and `src/main.tsx`
- `src/vite-env.d.ts`
- `src/components/NavLink.tsx`
- `src/components/ui/*.tsx` (48 components: accordion, alert-dialog, alert, aspect-ratio, avatar, badge, breadcrumb, button, calendar, card, carousel, chart, checkbox, collapsible, command, context-menu, dialog, drawer, dropdown-menu, form, hover-card, input-otp, input, label, menubar, navigation-menu, pagination, popover, progress, radio-group, resizable, scroll-area, select, separator, sheet, sidebar, skeleton, slider, sonner, switch, table, tabs, textarea, toast, toaster, toggle-group, toggle, tooltip, use-toast)
- `src/hooks/use-mobile.tsx` and `src/hooks/use-toast.ts`
- `src/lib/utils.ts`
- `src/pages/Index.tsx` and `src/pages/NotFound.tsx`
- `src/test/example.test.ts` and `src/test/setup.ts`

Consolidation Action: Copy canonical version to target un-prefixed path, verify content integrity, and remove all `01_*` .. `07_*` prefixed duplicates.

### 3. Public Directory (`public/`)
- `robots.txt`: Identical across all versions. Flattened to `public/robots.txt`.
- `placeholder.svg`: Identical across all versions. Flattened to `public/placeholder.svg`.
- `favicon.ico` & `favicon.png`: Standardized to canonical public favicon.

### 4. Projects Directory (`Projects/`)
- `Projects/01-MacroMate/`:
  - `01_README.md` and `02_README.md` synthesized into `README.md`.
  - `01_Palette.md` and `02_Palette.md` deduplicated into `colors-themes/Palette.md`.
  - `01_Tokens.json` and `02_Tokens.json` deduplicated into `colors-themes/Tokens.json`.
  - All media assets in `icons-image/` and `icons-svg/` deduplicated into un-prefixed names (`Logo.svg`, `Logo-Dark.svg`, `Logo-White.svg`, `Logo-Animated.svg`, `Logo-Animated.gif`, `Logo-128.png`, `Logo-256.png`, `Logo-512.png`, `Logo-052.png`, `Logo-1024-Light.png`, `Logo-1024-Dark.png`).
- `Projects/01-MeetRecorder/`: Retained intact.
- `Projects/02-LvExt/`: Retained intact.
- `Projects/02-ScriptsFixer/`: Retained intact.
- `Projects/03-LvExt/`: Retained intact.

### 5. Lovable Memories (`.lovable/`)
- `.lovable/prompts.md`: Synthesize unified prompt trigger index.
- `.lovable/prompts/02-logo-create.md`: Synthesize unified Logo Creation spec preserving key insights from all 7 variants.
- Delete temporary sequenced files `.lovable/01_prompts.md` .. `07_prompts.md` and `.lovable/prompts/01_02-logo-create.md` .. `07_02-logo-create.md`.

### 6. Manifest (`merge-ai-manifest.json`)
Update all entries in `fileCollisions[].status` from `pending` to `consolidated`.
