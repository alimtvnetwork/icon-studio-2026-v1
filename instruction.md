# AI Merge Consolidation Instruction & Verification Guide

This repository has been prepared by `gitmap merge-ai`. Multiple source repositories have been assembled into this staging tree with automated collision sequencing.

## Non-Negotiable Core Consolidation Rules:
1. **Preserve All Business Logic:** Do NOT delete features, endpoints, components, or data models. Consolidate overlapping files (`01_*`, `02_*`, `03_*`) into the single canonical file name (e.g. synthesize `01_App.tsx` and `02_App.tsx` into `App.tsx`).
2. **Asset & Media Preservation Invariant:** Never overwrite or delete distinct logos, icons, animations (`.gif`, `.svg`, `.png`, `.ico`), illustrations, or media assets. Preserve distinct assets side-by-side with descriptive semantic names (e.g. `logo-macromate.png`, `logo-animated.gif`, `logo-brand-builder.svg`) or in organized subfolders.
3. **Preserve Side-by-Side & Verify with Humans:** If conflicting assets, logos, brand elements, or themes exhibit stylistic or design differences, preserve both variations side-by-side and clearly annotate them for human stakeholder review rather than arbitrarily choosing one.
4. **Flatten Sequence Prefixes:** Once consolidated into canonical target files or side-by-side asset variants, remove temporary sequence prefixed files (`01_*`, `02_*`) so the repository strictly contains clean, canonical filenames.
5. **Reference Commit Metadata in Manifest:** Open `merge-ai-manifest.json` and inspect `repoSequence[].commitMetadata` (SHA, author, date, message, branch) to understand the origin context, recency, and author of each variant before making consolidation decisions.
6. **Zero Code Deletion:** When resolving duplicate utilities or components, favor additive composition, interface unions, and modern patterns.

## Folder Structure & Architectural Consolidation Advice:

### 1. Root Configuration & Manifests
- **`package.json` / `go.mod` / Build Manifests`:**
  - Create an additive union of all dependencies across source repositories. Where package versions differ, adopt the compatible newer version without dropping any required libraries.
  - Merge custom build, test, and dev scripts so all tools (vite, tailwind, linters) remain functional.
- **`README.md`:**
  - Synthesize a comprehensive monorepo or unified product overview documenting all incorporated submodules, features, and asset packages.
- **`tsconfig.json` / Linters / `.gitignore`:**
  - Merge path aliases, compiler flags, and ignore entries to ensure clean compilation across all merged source paths.

### 2. Source Code & Components (`src/`, `components/`, `lib/`)
- **Same-File / Same-Folder Collisions (`01_*`, `02_*`):**
  - Synthesize component hierarchies, routes, and state stores additively into the canonical file path.
  - If multiple sources contain distinct page views or feature workflows, integrate them as coherent routes, subpages, or navigation tabs rather than discarding one.
  - Update local imports to reference canonical consolidated modules.

### 3. Media Assets & Icons (`assets/`, `public/`, `icons/`)
- **Distinct Asset Preservation:**
  - Keep all unique icons, logos, GIFs, and SVGs.
  - For collisions on identical asset paths (e.g. `01_logo.png` vs `02_logo.png`):
    - Name them descriptively (e.g. `logo-<source>.png`) or place them in source-specific subdirectories under `assets/branding/` or `public/icons/`.
    - Provide a unified asset registry or catalog for downstream consumption.
  - When in doubt about brand or design preference, preserve all variants side-by-side and request human verification.

## Skipped Sources (Pre-Filter Intelligence):
The following source URLs were automatically skipped during pre-filtering:
- **File URL**: `https://github.com/alimtvnetwork/logo-1/blob/main/Projects/01-MacroMate/icons-image/Logo-Animated.gif` (Repository `alimtvnetwork/logo-1` is already included; file path: `Projects/01-MacroMate/icons-image/Logo-Animated.gif`)

## Detected File Collisions & Consolidation Guidance:

### `.lovable/prompts.md`
- **Type:** Source Code
- **Consolidation Advice:** Synthesize logic, functions, components, and routes additively into canonical file. Preserve all unique features without deleting business logic.
- **Sequenced Variants:**
  - Variant: `.lovable/01_prompts.md` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `.lovable/02_prompts.md` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)
  - Variant: `.lovable/03_prompts.md` (Source: `iconcraft-studio`, Commit: `bcaf1ffb`)
  - Variant: `.lovable/04_prompts.md` (Source: `brand-builder-studio`, Commit: `54945eb6`)
  - Variant: `.lovable/05_prompts.md` (Source: `brand-weaver`, Commit: `0b3ef66b`)
  - Variant: `.lovable/06_prompts.md` (Source: `macro-mate-logo-icon-27f183d0`, Commit: `124b4231`)
  - Variant: `.lovable/07_prompts.md` (Source: `brand-forge-studio`, Commit: `f6b80b17`)

### `.lovable/prompts/02-logo-create.md`
- **Type:** Source Code
- **Consolidation Advice:** Synthesize logic, functions, components, and routes additively into canonical file. Preserve all unique features without deleting business logic.
- **Sequenced Variants:**
  - Variant: `.lovable/prompts/01_02-logo-create.md` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `.lovable/prompts/02_02-logo-create.md` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)
  - Variant: `.lovable/prompts/03_02-logo-create.md` (Source: `iconcraft-studio`, Commit: `bcaf1ffb`)
  - Variant: `.lovable/prompts/04_02-logo-create.md` (Source: `brand-builder-studio`, Commit: `54945eb6`)
  - Variant: `.lovable/prompts/05_02-logo-create.md` (Source: `brand-weaver`, Commit: `0b3ef66b`)
  - Variant: `.lovable/prompts/06_02-logo-create.md` (Source: `macro-mate-logo-icon-27f183d0`, Commit: `124b4231`)
  - Variant: `.lovable/prompts/07_02-logo-create.md` (Source: `brand-forge-studio`, Commit: `f6b80b17`)

### `Projects/01-MacroMate/README.md`
- **Type:** Configuration / Manifest
- **Consolidation Advice:** Synthesize configuration additively into canonical file. Merge all unique dependencies, build scripts, and declarations.
- **Sequenced Variants:**
  - Variant: `Projects/01-MacroMate/01_README.md` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `Projects/01-MacroMate/02_README.md` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)

### `Projects/01-MacroMate/colors-themes/Palette.md`
- **Type:** Source Code
- **Consolidation Advice:** Synthesize logic, functions, components, and routes additively into canonical file. Preserve all unique features without deleting business logic.
- **Sequenced Variants:**
  - Variant: `Projects/01-MacroMate/colors-themes/01_Palette.md` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `Projects/01-MacroMate/colors-themes/02_Palette.md` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)

### `Projects/01-MacroMate/colors-themes/Tokens.json`
- **Type:** Source Code
- **Consolidation Advice:** Synthesize logic, functions, components, and routes additively into canonical file. Preserve all unique features without deleting business logic.
- **Sequenced Variants:**
  - Variant: `Projects/01-MacroMate/colors-themes/01_Tokens.json` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `Projects/01-MacroMate/colors-themes/02_Tokens.json` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)

### `Projects/01-MacroMate/favicon.ico`
- **Type:** Media Asset
- **Consolidation Advice:** Preserve distinct assets side-by-side using descriptive semantic filenames (or categorized subfolders). Do NOT overwrite or delete; verify design preference with human stakeholders.
- **Sequenced Variants:**
  - Variant: `Projects/01-MacroMate/01_favicon.ico` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `Projects/01-MacroMate/02_favicon.ico` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)

### `Projects/01-MacroMate/favicon.png`
- **Type:** Media Asset
- **Consolidation Advice:** Preserve distinct assets side-by-side using descriptive semantic filenames (or categorized subfolders). Do NOT overwrite or delete; verify design preference with human stakeholders.
- **Sequenced Variants:**
  - Variant: `Projects/01-MacroMate/01_favicon.png` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `Projects/01-MacroMate/02_favicon.png` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)

### `Projects/01-MacroMate/icons-image/Logo-128.png`
- **Type:** Media Asset
- **Consolidation Advice:** Preserve distinct assets side-by-side using descriptive semantic filenames (or categorized subfolders). Do NOT overwrite or delete; verify design preference with human stakeholders.
- **Sequenced Variants:**
  - Variant: `Projects/01-MacroMate/icons-image/01_Logo-128.png` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `Projects/01-MacroMate/icons-image/02_Logo-128.png` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)

### `Projects/01-MacroMate/icons-image/Logo-256.png`
- **Type:** Media Asset
- **Consolidation Advice:** Preserve distinct assets side-by-side using descriptive semantic filenames (or categorized subfolders). Do NOT overwrite or delete; verify design preference with human stakeholders.
- **Sequenced Variants:**
  - Variant: `Projects/01-MacroMate/icons-image/01_Logo-256.png` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `Projects/01-MacroMate/icons-image/02_Logo-256.png` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)

### `Projects/01-MacroMate/icons-image/Logo-512.png`
- **Type:** Media Asset
- **Consolidation Advice:** Preserve distinct assets side-by-side using descriptive semantic filenames (or categorized subfolders). Do NOT overwrite or delete; verify design preference with human stakeholders.
- **Sequenced Variants:**
  - Variant: `Projects/01-MacroMate/icons-image/01_Logo-512.png` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `Projects/01-MacroMate/icons-image/02_Logo-512.png` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)

### `Projects/01-MacroMate/icons-image/Logo-Animated.gif`
- **Type:** Media Asset
- **Consolidation Advice:** Preserve distinct assets side-by-side using descriptive semantic filenames (or categorized subfolders). Do NOT overwrite or delete; verify design preference with human stakeholders.
- **Sequenced Variants:**
  - Variant: `Projects/01-MacroMate/icons-image/01_Logo-Animated.gif` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `Projects/01-MacroMate/icons-image/02_Logo-Animated.gif` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)

### `Projects/01-MacroMate/icons-svg/Logo-Animated.svg`
- **Type:** Media Asset
- **Consolidation Advice:** Preserve distinct assets side-by-side using descriptive semantic filenames (or categorized subfolders). Do NOT overwrite or delete; verify design preference with human stakeholders.
- **Sequenced Variants:**
  - Variant: `Projects/01-MacroMate/icons-svg/01_Logo-Animated.svg` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `Projects/01-MacroMate/icons-svg/02_Logo-Animated.svg` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)

### `Projects/01-MacroMate/icons-svg/Logo-Dark.svg`
- **Type:** Media Asset
- **Consolidation Advice:** Preserve distinct assets side-by-side using descriptive semantic filenames (or categorized subfolders). Do NOT overwrite or delete; verify design preference with human stakeholders.
- **Sequenced Variants:**
  - Variant: `Projects/01-MacroMate/icons-svg/01_Logo-Dark.svg` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `Projects/01-MacroMate/icons-svg/02_Logo-Dark.svg` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)

### `Projects/01-MacroMate/icons-svg/Logo-White.svg`
- **Type:** Media Asset
- **Consolidation Advice:** Preserve distinct assets side-by-side using descriptive semantic filenames (or categorized subfolders). Do NOT overwrite or delete; verify design preference with human stakeholders.
- **Sequenced Variants:**
  - Variant: `Projects/01-MacroMate/icons-svg/01_Logo-White.svg` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `Projects/01-MacroMate/icons-svg/02_Logo-White.svg` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)

### `Projects/01-MacroMate/icons-svg/Logo.svg`
- **Type:** Media Asset
- **Consolidation Advice:** Preserve distinct assets side-by-side using descriptive semantic filenames (or categorized subfolders). Do NOT overwrite or delete; verify design preference with human stakeholders.
- **Sequenced Variants:**
  - Variant: `Projects/01-MacroMate/icons-svg/01_Logo.svg` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `Projects/01-MacroMate/icons-svg/02_Logo.svg` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)

### `README.md`
- **Type:** Configuration / Manifest
- **Consolidation Advice:** Synthesize configuration additively into canonical file. Merge all unique dependencies, build scripts, and declarations.
- **Sequenced Variants:**
  - Variant: `01_README.md` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `02_README.md` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)
  - Variant: `03_README.md` (Source: `iconcraft-studio`, Commit: `bcaf1ffb`)
  - Variant: `04_README.md` (Source: `brand-builder-studio`, Commit: `54945eb6`)
  - Variant: `05_README.md` (Source: `brand-weaver`, Commit: `0b3ef66b`)
  - Variant: `06_README.md` (Source: `macro-mate-logo-icon-27f183d0`, Commit: `124b4231`)
  - Variant: `07_README.md` (Source: `brand-forge-studio`, Commit: `f6b80b17`)

### `bun.lockb`
- **Type:** Source Code
- **Consolidation Advice:** Synthesize logic, functions, components, and routes additively into canonical file. Preserve all unique features without deleting business logic.
- **Sequenced Variants:**
  - Variant: `01_bun.lockb` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `02_bun.lockb` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)
  - Variant: `03_bun.lockb` (Source: `iconcraft-studio`, Commit: `bcaf1ffb`)
  - Variant: `04_bun.lockb` (Source: `brand-builder-studio`, Commit: `54945eb6`)
  - Variant: `05_bun.lockb` (Source: `brand-weaver`, Commit: `0b3ef66b`)
  - Variant: `06_bun.lockb` (Source: `macro-mate-logo-icon-27f183d0`, Commit: `124b4231`)
  - Variant: `07_bun.lockb` (Source: `brand-forge-studio`, Commit: `f6b80b17`)

### `components.json`
- **Type:** Source Code
- **Consolidation Advice:** Synthesize logic, functions, components, and routes additively into canonical file. Preserve all unique features without deleting business logic.
- **Sequenced Variants:**
  - Variant: `01_components.json` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `02_components.json` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)
  - Variant: `03_components.json` (Source: `iconcraft-studio`, Commit: `bcaf1ffb`)
  - Variant: `04_components.json` (Source: `brand-builder-studio`, Commit: `54945eb6`)
  - Variant: `05_components.json` (Source: `brand-weaver`, Commit: `0b3ef66b`)
  - Variant: `06_components.json` (Source: `macro-mate-logo-icon-27f183d0`, Commit: `124b4231`)
  - Variant: `07_components.json` (Source: `brand-forge-studio`, Commit: `f6b80b17`)

### `eslint.config.js`
- **Type:** Source Code
- **Consolidation Advice:** Synthesize logic, functions, components, and routes additively into canonical file. Preserve all unique features without deleting business logic.
- **Sequenced Variants:**
  - Variant: `01_eslint.config.js` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `02_eslint.config.js` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)
  - Variant: `03_eslint.config.js` (Source: `iconcraft-studio`, Commit: `bcaf1ffb`)
  - Variant: `04_eslint.config.js` (Source: `brand-builder-studio`, Commit: `54945eb6`)
  - Variant: `05_eslint.config.js` (Source: `brand-weaver`, Commit: `0b3ef66b`)
  - Variant: `06_eslint.config.js` (Source: `macro-mate-logo-icon-27f183d0`, Commit: `124b4231`)
  - Variant: `07_eslint.config.js` (Source: `brand-forge-studio`, Commit: `f6b80b17`)

### `favicon.ico`
- **Type:** Media Asset
- **Consolidation Advice:** Preserve distinct assets side-by-side using descriptive semantic filenames (or categorized subfolders). Do NOT overwrite or delete; verify design preference with human stakeholders.
- **Sequenced Variants:**
  - Variant: `02_favicon.ico` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)
  - Variant: `06_favicon.ico` (Source: `macro-mate-logo-icon-27f183d0`, Commit: `124b4231`)

### `favicon.png`
- **Type:** Media Asset
- **Consolidation Advice:** Preserve distinct assets side-by-side using descriptive semantic filenames (or categorized subfolders). Do NOT overwrite or delete; verify design preference with human stakeholders.
- **Sequenced Variants:**
  - Variant: `02_favicon.png` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)
  - Variant: `06_favicon.png` (Source: `macro-mate-logo-icon-27f183d0`, Commit: `124b4231`)

### `index.html`
- **Type:** Source Code
- **Consolidation Advice:** Synthesize logic, functions, components, and routes additively into canonical file. Preserve all unique features without deleting business logic.
- **Sequenced Variants:**
  - Variant: `01_index.html` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `02_index.html` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)
  - Variant: `03_index.html` (Source: `iconcraft-studio`, Commit: `bcaf1ffb`)
  - Variant: `04_index.html` (Source: `brand-builder-studio`, Commit: `54945eb6`)
  - Variant: `05_index.html` (Source: `brand-weaver`, Commit: `0b3ef66b`)
  - Variant: `06_index.html` (Source: `macro-mate-logo-icon-27f183d0`, Commit: `124b4231`)
  - Variant: `07_index.html` (Source: `brand-forge-studio`, Commit: `f6b80b17`)

### `package-lock.json`
- **Type:** Configuration / Manifest
- **Consolidation Advice:** Synthesize configuration additively into canonical file. Merge all unique dependencies, build scripts, and declarations.
- **Sequenced Variants:**
  - Variant: `01_package-lock.json` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `02_package-lock.json` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)
  - Variant: `03_package-lock.json` (Source: `iconcraft-studio`, Commit: `bcaf1ffb`)
  - Variant: `04_package-lock.json` (Source: `brand-builder-studio`, Commit: `54945eb6`)
  - Variant: `05_package-lock.json` (Source: `brand-weaver`, Commit: `0b3ef66b`)
  - Variant: `06_package-lock.json` (Source: `macro-mate-logo-icon-27f183d0`, Commit: `124b4231`)
  - Variant: `07_package-lock.json` (Source: `brand-forge-studio`, Commit: `f6b80b17`)

### `package.json`
- **Type:** Configuration / Manifest
- **Consolidation Advice:** Synthesize configuration additively into canonical file. Merge all unique dependencies, build scripts, and declarations.
- **Sequenced Variants:**
  - Variant: `01_package.json` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `02_package.json` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)
  - Variant: `03_package.json` (Source: `iconcraft-studio`, Commit: `bcaf1ffb`)
  - Variant: `04_package.json` (Source: `brand-builder-studio`, Commit: `54945eb6`)
  - Variant: `05_package.json` (Source: `brand-weaver`, Commit: `0b3ef66b`)
  - Variant: `06_package.json` (Source: `macro-mate-logo-icon-27f183d0`, Commit: `124b4231`)
  - Variant: `07_package.json` (Source: `brand-forge-studio`, Commit: `f6b80b17`)

### `plan.md`
- **Type:** Source Code
- **Consolidation Advice:** Synthesize logic, functions, components, and routes additively into canonical file. Preserve all unique features without deleting business logic.
- **Sequenced Variants:**
  - Variant: `01_plan.md` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `02_plan.md` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)
  - Variant: `03_plan.md` (Source: `iconcraft-studio`, Commit: `bcaf1ffb`)
  - Variant: `04_plan.md` (Source: `brand-builder-studio`, Commit: `54945eb6`)
  - Variant: `05_plan.md` (Source: `brand-weaver`, Commit: `0b3ef66b`)
  - Variant: `06_plan.md` (Source: `macro-mate-logo-icon-27f183d0`, Commit: `124b4231`)
  - Variant: `07_plan.md` (Source: `brand-forge-studio`, Commit: `f6b80b17`)

### `postcss.config.js`
- **Type:** Source Code
- **Consolidation Advice:** Synthesize logic, functions, components, and routes additively into canonical file. Preserve all unique features without deleting business logic.
- **Sequenced Variants:**
  - Variant: `01_postcss.config.js` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `02_postcss.config.js` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)
  - Variant: `03_postcss.config.js` (Source: `iconcraft-studio`, Commit: `bcaf1ffb`)
  - Variant: `04_postcss.config.js` (Source: `brand-builder-studio`, Commit: `54945eb6`)
  - Variant: `05_postcss.config.js` (Source: `brand-weaver`, Commit: `0b3ef66b`)
  - Variant: `06_postcss.config.js` (Source: `macro-mate-logo-icon-27f183d0`, Commit: `124b4231`)
  - Variant: `07_postcss.config.js` (Source: `brand-forge-studio`, Commit: `f6b80b17`)

### `public/favicon.ico`
- **Type:** Media Asset
- **Consolidation Advice:** Preserve distinct assets side-by-side using descriptive semantic filenames (or categorized subfolders). Do NOT overwrite or delete; verify design preference with human stakeholders.
- **Sequenced Variants:**
  - Variant: `public/01_favicon.ico` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `public/02_favicon.ico` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)
  - Variant: `public/03_favicon.ico` (Source: `iconcraft-studio`, Commit: `bcaf1ffb`)
  - Variant: `public/04_favicon.ico` (Source: `brand-builder-studio`, Commit: `54945eb6`)
  - Variant: `public/05_favicon.ico` (Source: `brand-weaver`, Commit: `0b3ef66b`)
  - Variant: `public/06_favicon.ico` (Source: `macro-mate-logo-icon-27f183d0`, Commit: `124b4231`)
  - Variant: `public/07_favicon.ico` (Source: `brand-forge-studio`, Commit: `f6b80b17`)

### `public/placeholder.svg`
- **Type:** Media Asset
- **Consolidation Advice:** Preserve distinct assets side-by-side using descriptive semantic filenames (or categorized subfolders). Do NOT overwrite or delete; verify design preference with human stakeholders.
- **Sequenced Variants:**
  - Variant: `public/01_placeholder.svg` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `public/02_placeholder.svg` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)
  - Variant: `public/03_placeholder.svg` (Source: `iconcraft-studio`, Commit: `bcaf1ffb`)
  - Variant: `public/04_placeholder.svg` (Source: `brand-builder-studio`, Commit: `54945eb6`)
  - Variant: `public/05_placeholder.svg` (Source: `brand-weaver`, Commit: `0b3ef66b`)
  - Variant: `public/06_placeholder.svg` (Source: `macro-mate-logo-icon-27f183d0`, Commit: `124b4231`)
  - Variant: `public/07_placeholder.svg` (Source: `brand-forge-studio`, Commit: `f6b80b17`)

### `public/robots.txt`
- **Type:** Source Code
- **Consolidation Advice:** Synthesize logic, functions, components, and routes additively into canonical file. Preserve all unique features without deleting business logic.
- **Sequenced Variants:**
  - Variant: `public/01_robots.txt` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `public/02_robots.txt` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)
  - Variant: `public/03_robots.txt` (Source: `iconcraft-studio`, Commit: `bcaf1ffb`)
  - Variant: `public/04_robots.txt` (Source: `brand-builder-studio`, Commit: `54945eb6`)
  - Variant: `public/05_robots.txt` (Source: `brand-weaver`, Commit: `0b3ef66b`)
  - Variant: `public/06_robots.txt` (Source: `macro-mate-logo-icon-27f183d0`, Commit: `124b4231`)
  - Variant: `public/07_robots.txt` (Source: `brand-forge-studio`, Commit: `f6b80b17`)

### `src/App.css`
- **Type:** Source Code
- **Consolidation Advice:** Synthesize logic, functions, components, and routes additively into canonical file. Preserve all unique features without deleting business logic.
- **Sequenced Variants:**
  - Variant: `src/01_App.css` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `src/02_App.css` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)
  - Variant: `src/03_App.css` (Source: `iconcraft-studio`, Commit: `bcaf1ffb`)
  - Variant: `src/04_App.css` (Source: `brand-builder-studio`, Commit: `54945eb6`)
  - Variant: `src/05_App.css` (Source: `brand-weaver`, Commit: `0b3ef66b`)
  - Variant: `src/06_App.css` (Source: `macro-mate-logo-icon-27f183d0`, Commit: `124b4231`)
  - Variant: `src/07_App.css` (Source: `brand-forge-studio`, Commit: `f6b80b17`)

### `src/App.tsx`
- **Type:** Source Code
- **Consolidation Advice:** Synthesize logic, functions, components, and routes additively into canonical file. Preserve all unique features without deleting business logic.
- **Sequenced Variants:**
  - Variant: `src/01_App.tsx` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `src/02_App.tsx` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)
  - Variant: `src/03_App.tsx` (Source: `iconcraft-studio`, Commit: `bcaf1ffb`)
  - Variant: `src/04_App.tsx` (Source: `brand-builder-studio`, Commit: `54945eb6`)
  - Variant: `src/05_App.tsx` (Source: `brand-weaver`, Commit: `0b3ef66b`)
  - Variant: `src/06_App.tsx` (Source: `macro-mate-logo-icon-27f183d0`, Commit: `124b4231`)
  - Variant: `src/07_App.tsx` (Source: `brand-forge-studio`, Commit: `f6b80b17`)

### `src/components/NavLink.tsx`
- **Type:** Source Code
- **Consolidation Advice:** Synthesize logic, functions, components, and routes additively into canonical file. Preserve all unique features without deleting business logic.
- **Sequenced Variants:**
  - Variant: `src/components/01_NavLink.tsx` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `src/components/02_NavLink.tsx` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)
  - Variant: `src/components/03_NavLink.tsx` (Source: `iconcraft-studio`, Commit: `bcaf1ffb`)
  - Variant: `src/components/04_NavLink.tsx` (Source: `brand-builder-studio`, Commit: `54945eb6`)
  - Variant: `src/components/05_NavLink.tsx` (Source: `brand-weaver`, Commit: `0b3ef66b`)
  - Variant: `src/components/06_NavLink.tsx` (Source: `macro-mate-logo-icon-27f183d0`, Commit: `124b4231`)
  - Variant: `src/components/07_NavLink.tsx` (Source: `brand-forge-studio`, Commit: `f6b80b17`)

### `src/components/ui/accordion.tsx`
- **Type:** Source Code
- **Consolidation Advice:** Synthesize logic, functions, components, and routes additively into canonical file. Preserve all unique features without deleting business logic.
- **Sequenced Variants:**
  - Variant: `src/components/ui/01_accordion.tsx` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `src/components/ui/02_accordion.tsx` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)
  - Variant: `src/components/ui/03_accordion.tsx` (Source: `iconcraft-studio`, Commit: `bcaf1ffb`)
  - Variant: `src/components/ui/04_accordion.tsx` (Source: `brand-builder-studio`, Commit: `54945eb6`)
  - Variant: `src/components/ui/05_accordion.tsx` (Source: `brand-weaver`, Commit: `0b3ef66b`)
  - Variant: `src/components/ui/06_accordion.tsx` (Source: `macro-mate-logo-icon-27f183d0`, Commit: `124b4231`)
  - Variant: `src/components/ui/07_accordion.tsx` (Source: `brand-forge-studio`, Commit: `f6b80b17`)

### `src/components/ui/alert-dialog.tsx`
- **Type:** Source Code
- **Consolidation Advice:** Synthesize logic, functions, components, and routes additively into canonical file. Preserve all unique features without deleting business logic.
- **Sequenced Variants:**
  - Variant: `src/components/ui/01_alert-dialog.tsx` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `src/components/ui/02_alert-dialog.tsx` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)
  - Variant: `src/components/ui/03_alert-dialog.tsx` (Source: `iconcraft-studio`, Commit: `bcaf1ffb`)
  - Variant: `src/components/ui/04_alert-dialog.tsx` (Source: `brand-builder-studio`, Commit: `54945eb6`)
  - Variant: `src/components/ui/05_alert-dialog.tsx` (Source: `brand-weaver`, Commit: `0b3ef66b`)
  - Variant: `src/components/ui/06_alert-dialog.tsx` (Source: `macro-mate-logo-icon-27f183d0`, Commit: `124b4231`)
  - Variant: `src/components/ui/07_alert-dialog.tsx` (Source: `brand-forge-studio`, Commit: `f6b80b17`)

### `src/components/ui/alert.tsx`
- **Type:** Source Code
- **Consolidation Advice:** Synthesize logic, functions, components, and routes additively into canonical file. Preserve all unique features without deleting business logic.
- **Sequenced Variants:**
  - Variant: `src/components/ui/01_alert.tsx` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `src/components/ui/02_alert.tsx` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)
  - Variant: `src/components/ui/03_alert.tsx` (Source: `iconcraft-studio`, Commit: `bcaf1ffb`)
  - Variant: `src/components/ui/04_alert.tsx` (Source: `brand-builder-studio`, Commit: `54945eb6`)
  - Variant: `src/components/ui/05_alert.tsx` (Source: `brand-weaver`, Commit: `0b3ef66b`)
  - Variant: `src/components/ui/06_alert.tsx` (Source: `macro-mate-logo-icon-27f183d0`, Commit: `124b4231`)
  - Variant: `src/components/ui/07_alert.tsx` (Source: `brand-forge-studio`, Commit: `f6b80b17`)

### `src/components/ui/aspect-ratio.tsx`
- **Type:** Source Code
- **Consolidation Advice:** Synthesize logic, functions, components, and routes additively into canonical file. Preserve all unique features without deleting business logic.
- **Sequenced Variants:**
  - Variant: `src/components/ui/01_aspect-ratio.tsx` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `src/components/ui/02_aspect-ratio.tsx` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)
  - Variant: `src/components/ui/03_aspect-ratio.tsx` (Source: `iconcraft-studio`, Commit: `bcaf1ffb`)
  - Variant: `src/components/ui/04_aspect-ratio.tsx` (Source: `brand-builder-studio`, Commit: `54945eb6`)
  - Variant: `src/components/ui/05_aspect-ratio.tsx` (Source: `brand-weaver`, Commit: `0b3ef66b`)
  - Variant: `src/components/ui/06_aspect-ratio.tsx` (Source: `macro-mate-logo-icon-27f183d0`, Commit: `124b4231`)
  - Variant: `src/components/ui/07_aspect-ratio.tsx` (Source: `brand-forge-studio`, Commit: `f6b80b17`)

### `src/components/ui/avatar.tsx`
- **Type:** Source Code
- **Consolidation Advice:** Synthesize logic, functions, components, and routes additively into canonical file. Preserve all unique features without deleting business logic.
- **Sequenced Variants:**
  - Variant: `src/components/ui/01_avatar.tsx` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `src/components/ui/02_avatar.tsx` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)
  - Variant: `src/components/ui/03_avatar.tsx` (Source: `iconcraft-studio`, Commit: `bcaf1ffb`)
  - Variant: `src/components/ui/04_avatar.tsx` (Source: `brand-builder-studio`, Commit: `54945eb6`)
  - Variant: `src/components/ui/05_avatar.tsx` (Source: `brand-weaver`, Commit: `0b3ef66b`)
  - Variant: `src/components/ui/06_avatar.tsx` (Source: `macro-mate-logo-icon-27f183d0`, Commit: `124b4231`)
  - Variant: `src/components/ui/07_avatar.tsx` (Source: `brand-forge-studio`, Commit: `f6b80b17`)

### `src/components/ui/badge.tsx`
- **Type:** Source Code
- **Consolidation Advice:** Synthesize logic, functions, components, and routes additively into canonical file. Preserve all unique features without deleting business logic.
- **Sequenced Variants:**
  - Variant: `src/components/ui/01_badge.tsx` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `src/components/ui/02_badge.tsx` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)
  - Variant: `src/components/ui/03_badge.tsx` (Source: `iconcraft-studio`, Commit: `bcaf1ffb`)
  - Variant: `src/components/ui/04_badge.tsx` (Source: `brand-builder-studio`, Commit: `54945eb6`)
  - Variant: `src/components/ui/05_badge.tsx` (Source: `brand-weaver`, Commit: `0b3ef66b`)
  - Variant: `src/components/ui/06_badge.tsx` (Source: `macro-mate-logo-icon-27f183d0`, Commit: `124b4231`)
  - Variant: `src/components/ui/07_badge.tsx` (Source: `brand-forge-studio`, Commit: `f6b80b17`)

### `src/components/ui/breadcrumb.tsx`
- **Type:** Source Code
- **Consolidation Advice:** Synthesize logic, functions, components, and routes additively into canonical file. Preserve all unique features without deleting business logic.
- **Sequenced Variants:**
  - Variant: `src/components/ui/01_breadcrumb.tsx` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `src/components/ui/02_breadcrumb.tsx` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)
  - Variant: `src/components/ui/03_breadcrumb.tsx` (Source: `iconcraft-studio`, Commit: `bcaf1ffb`)
  - Variant: `src/components/ui/04_breadcrumb.tsx` (Source: `brand-builder-studio`, Commit: `54945eb6`)
  - Variant: `src/components/ui/05_breadcrumb.tsx` (Source: `brand-weaver`, Commit: `0b3ef66b`)
  - Variant: `src/components/ui/06_breadcrumb.tsx` (Source: `macro-mate-logo-icon-27f183d0`, Commit: `124b4231`)
  - Variant: `src/components/ui/07_breadcrumb.tsx` (Source: `brand-forge-studio`, Commit: `f6b80b17`)

### `src/components/ui/button.tsx`
- **Type:** Source Code
- **Consolidation Advice:** Synthesize logic, functions, components, and routes additively into canonical file. Preserve all unique features without deleting business logic.
- **Sequenced Variants:**
  - Variant: `src/components/ui/01_button.tsx` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `src/components/ui/02_button.tsx` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)
  - Variant: `src/components/ui/03_button.tsx` (Source: `iconcraft-studio`, Commit: `bcaf1ffb`)
  - Variant: `src/components/ui/04_button.tsx` (Source: `brand-builder-studio`, Commit: `54945eb6`)
  - Variant: `src/components/ui/05_button.tsx` (Source: `brand-weaver`, Commit: `0b3ef66b`)
  - Variant: `src/components/ui/06_button.tsx` (Source: `macro-mate-logo-icon-27f183d0`, Commit: `124b4231`)
  - Variant: `src/components/ui/07_button.tsx` (Source: `brand-forge-studio`, Commit: `f6b80b17`)

### `src/components/ui/calendar.tsx`
- **Type:** Source Code
- **Consolidation Advice:** Synthesize logic, functions, components, and routes additively into canonical file. Preserve all unique features without deleting business logic.
- **Sequenced Variants:**
  - Variant: `src/components/ui/01_calendar.tsx` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `src/components/ui/02_calendar.tsx` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)
  - Variant: `src/components/ui/03_calendar.tsx` (Source: `iconcraft-studio`, Commit: `bcaf1ffb`)
  - Variant: `src/components/ui/04_calendar.tsx` (Source: `brand-builder-studio`, Commit: `54945eb6`)
  - Variant: `src/components/ui/05_calendar.tsx` (Source: `brand-weaver`, Commit: `0b3ef66b`)
  - Variant: `src/components/ui/06_calendar.tsx` (Source: `macro-mate-logo-icon-27f183d0`, Commit: `124b4231`)
  - Variant: `src/components/ui/07_calendar.tsx` (Source: `brand-forge-studio`, Commit: `f6b80b17`)

### `src/components/ui/card.tsx`
- **Type:** Source Code
- **Consolidation Advice:** Synthesize logic, functions, components, and routes additively into canonical file. Preserve all unique features without deleting business logic.
- **Sequenced Variants:**
  - Variant: `src/components/ui/01_card.tsx` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `src/components/ui/02_card.tsx` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)
  - Variant: `src/components/ui/03_card.tsx` (Source: `iconcraft-studio`, Commit: `bcaf1ffb`)
  - Variant: `src/components/ui/04_card.tsx` (Source: `brand-builder-studio`, Commit: `54945eb6`)
  - Variant: `src/components/ui/05_card.tsx` (Source: `brand-weaver`, Commit: `0b3ef66b`)
  - Variant: `src/components/ui/06_card.tsx` (Source: `macro-mate-logo-icon-27f183d0`, Commit: `124b4231`)
  - Variant: `src/components/ui/07_card.tsx` (Source: `brand-forge-studio`, Commit: `f6b80b17`)

### `src/components/ui/carousel.tsx`
- **Type:** Source Code
- **Consolidation Advice:** Synthesize logic, functions, components, and routes additively into canonical file. Preserve all unique features without deleting business logic.
- **Sequenced Variants:**
  - Variant: `src/components/ui/01_carousel.tsx` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `src/components/ui/02_carousel.tsx` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)
  - Variant: `src/components/ui/03_carousel.tsx` (Source: `iconcraft-studio`, Commit: `bcaf1ffb`)
  - Variant: `src/components/ui/04_carousel.tsx` (Source: `brand-builder-studio`, Commit: `54945eb6`)
  - Variant: `src/components/ui/05_carousel.tsx` (Source: `brand-weaver`, Commit: `0b3ef66b`)
  - Variant: `src/components/ui/06_carousel.tsx` (Source: `macro-mate-logo-icon-27f183d0`, Commit: `124b4231`)
  - Variant: `src/components/ui/07_carousel.tsx` (Source: `brand-forge-studio`, Commit: `f6b80b17`)

### `src/components/ui/chart.tsx`
- **Type:** Source Code
- **Consolidation Advice:** Synthesize logic, functions, components, and routes additively into canonical file. Preserve all unique features without deleting business logic.
- **Sequenced Variants:**
  - Variant: `src/components/ui/01_chart.tsx` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `src/components/ui/02_chart.tsx` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)
  - Variant: `src/components/ui/03_chart.tsx` (Source: `iconcraft-studio`, Commit: `bcaf1ffb`)
  - Variant: `src/components/ui/04_chart.tsx` (Source: `brand-builder-studio`, Commit: `54945eb6`)
  - Variant: `src/components/ui/05_chart.tsx` (Source: `brand-weaver`, Commit: `0b3ef66b`)
  - Variant: `src/components/ui/06_chart.tsx` (Source: `macro-mate-logo-icon-27f183d0`, Commit: `124b4231`)
  - Variant: `src/components/ui/07_chart.tsx` (Source: `brand-forge-studio`, Commit: `f6b80b17`)

### `src/components/ui/checkbox.tsx`
- **Type:** Source Code
- **Consolidation Advice:** Synthesize logic, functions, components, and routes additively into canonical file. Preserve all unique features without deleting business logic.
- **Sequenced Variants:**
  - Variant: `src/components/ui/01_checkbox.tsx` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `src/components/ui/02_checkbox.tsx` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)
  - Variant: `src/components/ui/03_checkbox.tsx` (Source: `iconcraft-studio`, Commit: `bcaf1ffb`)
  - Variant: `src/components/ui/04_checkbox.tsx` (Source: `brand-builder-studio`, Commit: `54945eb6`)
  - Variant: `src/components/ui/05_checkbox.tsx` (Source: `brand-weaver`, Commit: `0b3ef66b`)
  - Variant: `src/components/ui/06_checkbox.tsx` (Source: `macro-mate-logo-icon-27f183d0`, Commit: `124b4231`)
  - Variant: `src/components/ui/07_checkbox.tsx` (Source: `brand-forge-studio`, Commit: `f6b80b17`)

### `src/components/ui/collapsible.tsx`
- **Type:** Source Code
- **Consolidation Advice:** Synthesize logic, functions, components, and routes additively into canonical file. Preserve all unique features without deleting business logic.
- **Sequenced Variants:**
  - Variant: `src/components/ui/01_collapsible.tsx` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `src/components/ui/02_collapsible.tsx` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)
  - Variant: `src/components/ui/03_collapsible.tsx` (Source: `iconcraft-studio`, Commit: `bcaf1ffb`)
  - Variant: `src/components/ui/04_collapsible.tsx` (Source: `brand-builder-studio`, Commit: `54945eb6`)
  - Variant: `src/components/ui/05_collapsible.tsx` (Source: `brand-weaver`, Commit: `0b3ef66b`)
  - Variant: `src/components/ui/06_collapsible.tsx` (Source: `macro-mate-logo-icon-27f183d0`, Commit: `124b4231`)
  - Variant: `src/components/ui/07_collapsible.tsx` (Source: `brand-forge-studio`, Commit: `f6b80b17`)

### `src/components/ui/command.tsx`
- **Type:** Source Code
- **Consolidation Advice:** Synthesize logic, functions, components, and routes additively into canonical file. Preserve all unique features without deleting business logic.
- **Sequenced Variants:**
  - Variant: `src/components/ui/01_command.tsx` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `src/components/ui/02_command.tsx` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)
  - Variant: `src/components/ui/03_command.tsx` (Source: `iconcraft-studio`, Commit: `bcaf1ffb`)
  - Variant: `src/components/ui/04_command.tsx` (Source: `brand-builder-studio`, Commit: `54945eb6`)
  - Variant: `src/components/ui/05_command.tsx` (Source: `brand-weaver`, Commit: `0b3ef66b`)
  - Variant: `src/components/ui/06_command.tsx` (Source: `macro-mate-logo-icon-27f183d0`, Commit: `124b4231`)
  - Variant: `src/components/ui/07_command.tsx` (Source: `brand-forge-studio`, Commit: `f6b80b17`)

### `src/components/ui/context-menu.tsx`
- **Type:** Source Code
- **Consolidation Advice:** Synthesize logic, functions, components, and routes additively into canonical file. Preserve all unique features without deleting business logic.
- **Sequenced Variants:**
  - Variant: `src/components/ui/01_context-menu.tsx` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `src/components/ui/02_context-menu.tsx` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)
  - Variant: `src/components/ui/03_context-menu.tsx` (Source: `iconcraft-studio`, Commit: `bcaf1ffb`)
  - Variant: `src/components/ui/04_context-menu.tsx` (Source: `brand-builder-studio`, Commit: `54945eb6`)
  - Variant: `src/components/ui/05_context-menu.tsx` (Source: `brand-weaver`, Commit: `0b3ef66b`)
  - Variant: `src/components/ui/06_context-menu.tsx` (Source: `macro-mate-logo-icon-27f183d0`, Commit: `124b4231`)
  - Variant: `src/components/ui/07_context-menu.tsx` (Source: `brand-forge-studio`, Commit: `f6b80b17`)

### `src/components/ui/dialog.tsx`
- **Type:** Source Code
- **Consolidation Advice:** Synthesize logic, functions, components, and routes additively into canonical file. Preserve all unique features without deleting business logic.
- **Sequenced Variants:**
  - Variant: `src/components/ui/01_dialog.tsx` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `src/components/ui/02_dialog.tsx` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)
  - Variant: `src/components/ui/03_dialog.tsx` (Source: `iconcraft-studio`, Commit: `bcaf1ffb`)
  - Variant: `src/components/ui/04_dialog.tsx` (Source: `brand-builder-studio`, Commit: `54945eb6`)
  - Variant: `src/components/ui/05_dialog.tsx` (Source: `brand-weaver`, Commit: `0b3ef66b`)
  - Variant: `src/components/ui/06_dialog.tsx` (Source: `macro-mate-logo-icon-27f183d0`, Commit: `124b4231`)
  - Variant: `src/components/ui/07_dialog.tsx` (Source: `brand-forge-studio`, Commit: `f6b80b17`)

### `src/components/ui/drawer.tsx`
- **Type:** Source Code
- **Consolidation Advice:** Synthesize logic, functions, components, and routes additively into canonical file. Preserve all unique features without deleting business logic.
- **Sequenced Variants:**
  - Variant: `src/components/ui/01_drawer.tsx` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `src/components/ui/02_drawer.tsx` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)
  - Variant: `src/components/ui/03_drawer.tsx` (Source: `iconcraft-studio`, Commit: `bcaf1ffb`)
  - Variant: `src/components/ui/04_drawer.tsx` (Source: `brand-builder-studio`, Commit: `54945eb6`)
  - Variant: `src/components/ui/05_drawer.tsx` (Source: `brand-weaver`, Commit: `0b3ef66b`)
  - Variant: `src/components/ui/06_drawer.tsx` (Source: `macro-mate-logo-icon-27f183d0`, Commit: `124b4231`)
  - Variant: `src/components/ui/07_drawer.tsx` (Source: `brand-forge-studio`, Commit: `f6b80b17`)

### `src/components/ui/dropdown-menu.tsx`
- **Type:** Source Code
- **Consolidation Advice:** Synthesize logic, functions, components, and routes additively into canonical file. Preserve all unique features without deleting business logic.
- **Sequenced Variants:**
  - Variant: `src/components/ui/01_dropdown-menu.tsx` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `src/components/ui/02_dropdown-menu.tsx` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)
  - Variant: `src/components/ui/03_dropdown-menu.tsx` (Source: `iconcraft-studio`, Commit: `bcaf1ffb`)
  - Variant: `src/components/ui/04_dropdown-menu.tsx` (Source: `brand-builder-studio`, Commit: `54945eb6`)
  - Variant: `src/components/ui/05_dropdown-menu.tsx` (Source: `brand-weaver`, Commit: `0b3ef66b`)
  - Variant: `src/components/ui/06_dropdown-menu.tsx` (Source: `macro-mate-logo-icon-27f183d0`, Commit: `124b4231`)
  - Variant: `src/components/ui/07_dropdown-menu.tsx` (Source: `brand-forge-studio`, Commit: `f6b80b17`)

### `src/components/ui/form.tsx`
- **Type:** Source Code
- **Consolidation Advice:** Synthesize logic, functions, components, and routes additively into canonical file. Preserve all unique features without deleting business logic.
- **Sequenced Variants:**
  - Variant: `src/components/ui/01_form.tsx` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `src/components/ui/02_form.tsx` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)
  - Variant: `src/components/ui/03_form.tsx` (Source: `iconcraft-studio`, Commit: `bcaf1ffb`)
  - Variant: `src/components/ui/04_form.tsx` (Source: `brand-builder-studio`, Commit: `54945eb6`)
  - Variant: `src/components/ui/05_form.tsx` (Source: `brand-weaver`, Commit: `0b3ef66b`)
  - Variant: `src/components/ui/06_form.tsx` (Source: `macro-mate-logo-icon-27f183d0`, Commit: `124b4231`)
  - Variant: `src/components/ui/07_form.tsx` (Source: `brand-forge-studio`, Commit: `f6b80b17`)

### `src/components/ui/hover-card.tsx`
- **Type:** Source Code
- **Consolidation Advice:** Synthesize logic, functions, components, and routes additively into canonical file. Preserve all unique features without deleting business logic.
- **Sequenced Variants:**
  - Variant: `src/components/ui/01_hover-card.tsx` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `src/components/ui/02_hover-card.tsx` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)
  - Variant: `src/components/ui/03_hover-card.tsx` (Source: `iconcraft-studio`, Commit: `bcaf1ffb`)
  - Variant: `src/components/ui/04_hover-card.tsx` (Source: `brand-builder-studio`, Commit: `54945eb6`)
  - Variant: `src/components/ui/05_hover-card.tsx` (Source: `brand-weaver`, Commit: `0b3ef66b`)
  - Variant: `src/components/ui/06_hover-card.tsx` (Source: `macro-mate-logo-icon-27f183d0`, Commit: `124b4231`)
  - Variant: `src/components/ui/07_hover-card.tsx` (Source: `brand-forge-studio`, Commit: `f6b80b17`)

### `src/components/ui/input-otp.tsx`
- **Type:** Source Code
- **Consolidation Advice:** Synthesize logic, functions, components, and routes additively into canonical file. Preserve all unique features without deleting business logic.
- **Sequenced Variants:**
  - Variant: `src/components/ui/01_input-otp.tsx` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `src/components/ui/02_input-otp.tsx` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)
  - Variant: `src/components/ui/03_input-otp.tsx` (Source: `iconcraft-studio`, Commit: `bcaf1ffb`)
  - Variant: `src/components/ui/04_input-otp.tsx` (Source: `brand-builder-studio`, Commit: `54945eb6`)
  - Variant: `src/components/ui/05_input-otp.tsx` (Source: `brand-weaver`, Commit: `0b3ef66b`)
  - Variant: `src/components/ui/06_input-otp.tsx` (Source: `macro-mate-logo-icon-27f183d0`, Commit: `124b4231`)
  - Variant: `src/components/ui/07_input-otp.tsx` (Source: `brand-forge-studio`, Commit: `f6b80b17`)

### `src/components/ui/input.tsx`
- **Type:** Source Code
- **Consolidation Advice:** Synthesize logic, functions, components, and routes additively into canonical file. Preserve all unique features without deleting business logic.
- **Sequenced Variants:**
  - Variant: `src/components/ui/01_input.tsx` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `src/components/ui/02_input.tsx` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)
  - Variant: `src/components/ui/03_input.tsx` (Source: `iconcraft-studio`, Commit: `bcaf1ffb`)
  - Variant: `src/components/ui/04_input.tsx` (Source: `brand-builder-studio`, Commit: `54945eb6`)
  - Variant: `src/components/ui/05_input.tsx` (Source: `brand-weaver`, Commit: `0b3ef66b`)
  - Variant: `src/components/ui/06_input.tsx` (Source: `macro-mate-logo-icon-27f183d0`, Commit: `124b4231`)
  - Variant: `src/components/ui/07_input.tsx` (Source: `brand-forge-studio`, Commit: `f6b80b17`)

### `src/components/ui/label.tsx`
- **Type:** Source Code
- **Consolidation Advice:** Synthesize logic, functions, components, and routes additively into canonical file. Preserve all unique features without deleting business logic.
- **Sequenced Variants:**
  - Variant: `src/components/ui/01_label.tsx` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `src/components/ui/02_label.tsx` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)
  - Variant: `src/components/ui/03_label.tsx` (Source: `iconcraft-studio`, Commit: `bcaf1ffb`)
  - Variant: `src/components/ui/04_label.tsx` (Source: `brand-builder-studio`, Commit: `54945eb6`)
  - Variant: `src/components/ui/05_label.tsx` (Source: `brand-weaver`, Commit: `0b3ef66b`)
  - Variant: `src/components/ui/06_label.tsx` (Source: `macro-mate-logo-icon-27f183d0`, Commit: `124b4231`)
  - Variant: `src/components/ui/07_label.tsx` (Source: `brand-forge-studio`, Commit: `f6b80b17`)

### `src/components/ui/menubar.tsx`
- **Type:** Source Code
- **Consolidation Advice:** Synthesize logic, functions, components, and routes additively into canonical file. Preserve all unique features without deleting business logic.
- **Sequenced Variants:**
  - Variant: `src/components/ui/01_menubar.tsx` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `src/components/ui/02_menubar.tsx` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)
  - Variant: `src/components/ui/03_menubar.tsx` (Source: `iconcraft-studio`, Commit: `bcaf1ffb`)
  - Variant: `src/components/ui/04_menubar.tsx` (Source: `brand-builder-studio`, Commit: `54945eb6`)
  - Variant: `src/components/ui/05_menubar.tsx` (Source: `brand-weaver`, Commit: `0b3ef66b`)
  - Variant: `src/components/ui/06_menubar.tsx` (Source: `macro-mate-logo-icon-27f183d0`, Commit: `124b4231`)
  - Variant: `src/components/ui/07_menubar.tsx` (Source: `brand-forge-studio`, Commit: `f6b80b17`)

### `src/components/ui/navigation-menu.tsx`
- **Type:** Source Code
- **Consolidation Advice:** Synthesize logic, functions, components, and routes additively into canonical file. Preserve all unique features without deleting business logic.
- **Sequenced Variants:**
  - Variant: `src/components/ui/01_navigation-menu.tsx` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `src/components/ui/02_navigation-menu.tsx` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)
  - Variant: `src/components/ui/03_navigation-menu.tsx` (Source: `iconcraft-studio`, Commit: `bcaf1ffb`)
  - Variant: `src/components/ui/04_navigation-menu.tsx` (Source: `brand-builder-studio`, Commit: `54945eb6`)
  - Variant: `src/components/ui/05_navigation-menu.tsx` (Source: `brand-weaver`, Commit: `0b3ef66b`)
  - Variant: `src/components/ui/06_navigation-menu.tsx` (Source: `macro-mate-logo-icon-27f183d0`, Commit: `124b4231`)
  - Variant: `src/components/ui/07_navigation-menu.tsx` (Source: `brand-forge-studio`, Commit: `f6b80b17`)

### `src/components/ui/pagination.tsx`
- **Type:** Source Code
- **Consolidation Advice:** Synthesize logic, functions, components, and routes additively into canonical file. Preserve all unique features without deleting business logic.
- **Sequenced Variants:**
  - Variant: `src/components/ui/01_pagination.tsx` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `src/components/ui/02_pagination.tsx` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)
  - Variant: `src/components/ui/03_pagination.tsx` (Source: `iconcraft-studio`, Commit: `bcaf1ffb`)
  - Variant: `src/components/ui/04_pagination.tsx` (Source: `brand-builder-studio`, Commit: `54945eb6`)
  - Variant: `src/components/ui/05_pagination.tsx` (Source: `brand-weaver`, Commit: `0b3ef66b`)
  - Variant: `src/components/ui/06_pagination.tsx` (Source: `macro-mate-logo-icon-27f183d0`, Commit: `124b4231`)
  - Variant: `src/components/ui/07_pagination.tsx` (Source: `brand-forge-studio`, Commit: `f6b80b17`)

### `src/components/ui/popover.tsx`
- **Type:** Source Code
- **Consolidation Advice:** Synthesize logic, functions, components, and routes additively into canonical file. Preserve all unique features without deleting business logic.
- **Sequenced Variants:**
  - Variant: `src/components/ui/01_popover.tsx` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `src/components/ui/02_popover.tsx` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)
  - Variant: `src/components/ui/03_popover.tsx` (Source: `iconcraft-studio`, Commit: `bcaf1ffb`)
  - Variant: `src/components/ui/04_popover.tsx` (Source: `brand-builder-studio`, Commit: `54945eb6`)
  - Variant: `src/components/ui/05_popover.tsx` (Source: `brand-weaver`, Commit: `0b3ef66b`)
  - Variant: `src/components/ui/06_popover.tsx` (Source: `macro-mate-logo-icon-27f183d0`, Commit: `124b4231`)
  - Variant: `src/components/ui/07_popover.tsx` (Source: `brand-forge-studio`, Commit: `f6b80b17`)

### `src/components/ui/progress.tsx`
- **Type:** Source Code
- **Consolidation Advice:** Synthesize logic, functions, components, and routes additively into canonical file. Preserve all unique features without deleting business logic.
- **Sequenced Variants:**
  - Variant: `src/components/ui/01_progress.tsx` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `src/components/ui/02_progress.tsx` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)
  - Variant: `src/components/ui/03_progress.tsx` (Source: `iconcraft-studio`, Commit: `bcaf1ffb`)
  - Variant: `src/components/ui/04_progress.tsx` (Source: `brand-builder-studio`, Commit: `54945eb6`)
  - Variant: `src/components/ui/05_progress.tsx` (Source: `brand-weaver`, Commit: `0b3ef66b`)
  - Variant: `src/components/ui/06_progress.tsx` (Source: `macro-mate-logo-icon-27f183d0`, Commit: `124b4231`)
  - Variant: `src/components/ui/07_progress.tsx` (Source: `brand-forge-studio`, Commit: `f6b80b17`)

### `src/components/ui/radio-group.tsx`
- **Type:** Source Code
- **Consolidation Advice:** Synthesize logic, functions, components, and routes additively into canonical file. Preserve all unique features without deleting business logic.
- **Sequenced Variants:**
  - Variant: `src/components/ui/01_radio-group.tsx` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `src/components/ui/02_radio-group.tsx` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)
  - Variant: `src/components/ui/03_radio-group.tsx` (Source: `iconcraft-studio`, Commit: `bcaf1ffb`)
  - Variant: `src/components/ui/04_radio-group.tsx` (Source: `brand-builder-studio`, Commit: `54945eb6`)
  - Variant: `src/components/ui/05_radio-group.tsx` (Source: `brand-weaver`, Commit: `0b3ef66b`)
  - Variant: `src/components/ui/06_radio-group.tsx` (Source: `macro-mate-logo-icon-27f183d0`, Commit: `124b4231`)
  - Variant: `src/components/ui/07_radio-group.tsx` (Source: `brand-forge-studio`, Commit: `f6b80b17`)

### `src/components/ui/resizable.tsx`
- **Type:** Source Code
- **Consolidation Advice:** Synthesize logic, functions, components, and routes additively into canonical file. Preserve all unique features without deleting business logic.
- **Sequenced Variants:**
  - Variant: `src/components/ui/01_resizable.tsx` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `src/components/ui/02_resizable.tsx` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)
  - Variant: `src/components/ui/03_resizable.tsx` (Source: `iconcraft-studio`, Commit: `bcaf1ffb`)
  - Variant: `src/components/ui/04_resizable.tsx` (Source: `brand-builder-studio`, Commit: `54945eb6`)
  - Variant: `src/components/ui/05_resizable.tsx` (Source: `brand-weaver`, Commit: `0b3ef66b`)
  - Variant: `src/components/ui/06_resizable.tsx` (Source: `macro-mate-logo-icon-27f183d0`, Commit: `124b4231`)
  - Variant: `src/components/ui/07_resizable.tsx` (Source: `brand-forge-studio`, Commit: `f6b80b17`)

### `src/components/ui/scroll-area.tsx`
- **Type:** Source Code
- **Consolidation Advice:** Synthesize logic, functions, components, and routes additively into canonical file. Preserve all unique features without deleting business logic.
- **Sequenced Variants:**
  - Variant: `src/components/ui/01_scroll-area.tsx` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `src/components/ui/02_scroll-area.tsx` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)
  - Variant: `src/components/ui/03_scroll-area.tsx` (Source: `iconcraft-studio`, Commit: `bcaf1ffb`)
  - Variant: `src/components/ui/04_scroll-area.tsx` (Source: `brand-builder-studio`, Commit: `54945eb6`)
  - Variant: `src/components/ui/05_scroll-area.tsx` (Source: `brand-weaver`, Commit: `0b3ef66b`)
  - Variant: `src/components/ui/06_scroll-area.tsx` (Source: `macro-mate-logo-icon-27f183d0`, Commit: `124b4231`)
  - Variant: `src/components/ui/07_scroll-area.tsx` (Source: `brand-forge-studio`, Commit: `f6b80b17`)

### `src/components/ui/select.tsx`
- **Type:** Source Code
- **Consolidation Advice:** Synthesize logic, functions, components, and routes additively into canonical file. Preserve all unique features without deleting business logic.
- **Sequenced Variants:**
  - Variant: `src/components/ui/01_select.tsx` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `src/components/ui/02_select.tsx` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)
  - Variant: `src/components/ui/03_select.tsx` (Source: `iconcraft-studio`, Commit: `bcaf1ffb`)
  - Variant: `src/components/ui/04_select.tsx` (Source: `brand-builder-studio`, Commit: `54945eb6`)
  - Variant: `src/components/ui/05_select.tsx` (Source: `brand-weaver`, Commit: `0b3ef66b`)
  - Variant: `src/components/ui/06_select.tsx` (Source: `macro-mate-logo-icon-27f183d0`, Commit: `124b4231`)
  - Variant: `src/components/ui/07_select.tsx` (Source: `brand-forge-studio`, Commit: `f6b80b17`)

### `src/components/ui/separator.tsx`
- **Type:** Source Code
- **Consolidation Advice:** Synthesize logic, functions, components, and routes additively into canonical file. Preserve all unique features without deleting business logic.
- **Sequenced Variants:**
  - Variant: `src/components/ui/01_separator.tsx` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `src/components/ui/02_separator.tsx` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)
  - Variant: `src/components/ui/03_separator.tsx` (Source: `iconcraft-studio`, Commit: `bcaf1ffb`)
  - Variant: `src/components/ui/04_separator.tsx` (Source: `brand-builder-studio`, Commit: `54945eb6`)
  - Variant: `src/components/ui/05_separator.tsx` (Source: `brand-weaver`, Commit: `0b3ef66b`)
  - Variant: `src/components/ui/06_separator.tsx` (Source: `macro-mate-logo-icon-27f183d0`, Commit: `124b4231`)
  - Variant: `src/components/ui/07_separator.tsx` (Source: `brand-forge-studio`, Commit: `f6b80b17`)

### `src/components/ui/sheet.tsx`
- **Type:** Source Code
- **Consolidation Advice:** Synthesize logic, functions, components, and routes additively into canonical file. Preserve all unique features without deleting business logic.
- **Sequenced Variants:**
  - Variant: `src/components/ui/01_sheet.tsx` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `src/components/ui/02_sheet.tsx` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)
  - Variant: `src/components/ui/03_sheet.tsx` (Source: `iconcraft-studio`, Commit: `bcaf1ffb`)
  - Variant: `src/components/ui/04_sheet.tsx` (Source: `brand-builder-studio`, Commit: `54945eb6`)
  - Variant: `src/components/ui/05_sheet.tsx` (Source: `brand-weaver`, Commit: `0b3ef66b`)
  - Variant: `src/components/ui/06_sheet.tsx` (Source: `macro-mate-logo-icon-27f183d0`, Commit: `124b4231`)
  - Variant: `src/components/ui/07_sheet.tsx` (Source: `brand-forge-studio`, Commit: `f6b80b17`)

### `src/components/ui/sidebar.tsx`
- **Type:** Source Code
- **Consolidation Advice:** Synthesize logic, functions, components, and routes additively into canonical file. Preserve all unique features without deleting business logic.
- **Sequenced Variants:**
  - Variant: `src/components/ui/01_sidebar.tsx` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `src/components/ui/02_sidebar.tsx` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)
  - Variant: `src/components/ui/03_sidebar.tsx` (Source: `iconcraft-studio`, Commit: `bcaf1ffb`)
  - Variant: `src/components/ui/04_sidebar.tsx` (Source: `brand-builder-studio`, Commit: `54945eb6`)
  - Variant: `src/components/ui/05_sidebar.tsx` (Source: `brand-weaver`, Commit: `0b3ef66b`)
  - Variant: `src/components/ui/06_sidebar.tsx` (Source: `macro-mate-logo-icon-27f183d0`, Commit: `124b4231`)
  - Variant: `src/components/ui/07_sidebar.tsx` (Source: `brand-forge-studio`, Commit: `f6b80b17`)

### `src/components/ui/skeleton.tsx`
- **Type:** Source Code
- **Consolidation Advice:** Synthesize logic, functions, components, and routes additively into canonical file. Preserve all unique features without deleting business logic.
- **Sequenced Variants:**
  - Variant: `src/components/ui/01_skeleton.tsx` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `src/components/ui/02_skeleton.tsx` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)
  - Variant: `src/components/ui/03_skeleton.tsx` (Source: `iconcraft-studio`, Commit: `bcaf1ffb`)
  - Variant: `src/components/ui/04_skeleton.tsx` (Source: `brand-builder-studio`, Commit: `54945eb6`)
  - Variant: `src/components/ui/05_skeleton.tsx` (Source: `brand-weaver`, Commit: `0b3ef66b`)
  - Variant: `src/components/ui/06_skeleton.tsx` (Source: `macro-mate-logo-icon-27f183d0`, Commit: `124b4231`)
  - Variant: `src/components/ui/07_skeleton.tsx` (Source: `brand-forge-studio`, Commit: `f6b80b17`)

### `src/components/ui/slider.tsx`
- **Type:** Source Code
- **Consolidation Advice:** Synthesize logic, functions, components, and routes additively into canonical file. Preserve all unique features without deleting business logic.
- **Sequenced Variants:**
  - Variant: `src/components/ui/01_slider.tsx` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `src/components/ui/02_slider.tsx` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)
  - Variant: `src/components/ui/03_slider.tsx` (Source: `iconcraft-studio`, Commit: `bcaf1ffb`)
  - Variant: `src/components/ui/04_slider.tsx` (Source: `brand-builder-studio`, Commit: `54945eb6`)
  - Variant: `src/components/ui/05_slider.tsx` (Source: `brand-weaver`, Commit: `0b3ef66b`)
  - Variant: `src/components/ui/06_slider.tsx` (Source: `macro-mate-logo-icon-27f183d0`, Commit: `124b4231`)
  - Variant: `src/components/ui/07_slider.tsx` (Source: `brand-forge-studio`, Commit: `f6b80b17`)

### `src/components/ui/sonner.tsx`
- **Type:** Source Code
- **Consolidation Advice:** Synthesize logic, functions, components, and routes additively into canonical file. Preserve all unique features without deleting business logic.
- **Sequenced Variants:**
  - Variant: `src/components/ui/01_sonner.tsx` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `src/components/ui/02_sonner.tsx` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)
  - Variant: `src/components/ui/03_sonner.tsx` (Source: `iconcraft-studio`, Commit: `bcaf1ffb`)
  - Variant: `src/components/ui/04_sonner.tsx` (Source: `brand-builder-studio`, Commit: `54945eb6`)
  - Variant: `src/components/ui/05_sonner.tsx` (Source: `brand-weaver`, Commit: `0b3ef66b`)
  - Variant: `src/components/ui/06_sonner.tsx` (Source: `macro-mate-logo-icon-27f183d0`, Commit: `124b4231`)
  - Variant: `src/components/ui/07_sonner.tsx` (Source: `brand-forge-studio`, Commit: `f6b80b17`)

### `src/components/ui/switch.tsx`
- **Type:** Source Code
- **Consolidation Advice:** Synthesize logic, functions, components, and routes additively into canonical file. Preserve all unique features without deleting business logic.
- **Sequenced Variants:**
  - Variant: `src/components/ui/01_switch.tsx` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `src/components/ui/02_switch.tsx` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)
  - Variant: `src/components/ui/03_switch.tsx` (Source: `iconcraft-studio`, Commit: `bcaf1ffb`)
  - Variant: `src/components/ui/04_switch.tsx` (Source: `brand-builder-studio`, Commit: `54945eb6`)
  - Variant: `src/components/ui/05_switch.tsx` (Source: `brand-weaver`, Commit: `0b3ef66b`)
  - Variant: `src/components/ui/06_switch.tsx` (Source: `macro-mate-logo-icon-27f183d0`, Commit: `124b4231`)
  - Variant: `src/components/ui/07_switch.tsx` (Source: `brand-forge-studio`, Commit: `f6b80b17`)

### `src/components/ui/table.tsx`
- **Type:** Source Code
- **Consolidation Advice:** Synthesize logic, functions, components, and routes additively into canonical file. Preserve all unique features without deleting business logic.
- **Sequenced Variants:**
  - Variant: `src/components/ui/01_table.tsx` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `src/components/ui/02_table.tsx` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)
  - Variant: `src/components/ui/03_table.tsx` (Source: `iconcraft-studio`, Commit: `bcaf1ffb`)
  - Variant: `src/components/ui/04_table.tsx` (Source: `brand-builder-studio`, Commit: `54945eb6`)
  - Variant: `src/components/ui/05_table.tsx` (Source: `brand-weaver`, Commit: `0b3ef66b`)
  - Variant: `src/components/ui/06_table.tsx` (Source: `macro-mate-logo-icon-27f183d0`, Commit: `124b4231`)
  - Variant: `src/components/ui/07_table.tsx` (Source: `brand-forge-studio`, Commit: `f6b80b17`)

### `src/components/ui/tabs.tsx`
- **Type:** Source Code
- **Consolidation Advice:** Synthesize logic, functions, components, and routes additively into canonical file. Preserve all unique features without deleting business logic.
- **Sequenced Variants:**
  - Variant: `src/components/ui/01_tabs.tsx` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `src/components/ui/02_tabs.tsx` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)
  - Variant: `src/components/ui/03_tabs.tsx` (Source: `iconcraft-studio`, Commit: `bcaf1ffb`)
  - Variant: `src/components/ui/04_tabs.tsx` (Source: `brand-builder-studio`, Commit: `54945eb6`)
  - Variant: `src/components/ui/05_tabs.tsx` (Source: `brand-weaver`, Commit: `0b3ef66b`)
  - Variant: `src/components/ui/06_tabs.tsx` (Source: `macro-mate-logo-icon-27f183d0`, Commit: `124b4231`)
  - Variant: `src/components/ui/07_tabs.tsx` (Source: `brand-forge-studio`, Commit: `f6b80b17`)

### `src/components/ui/textarea.tsx`
- **Type:** Source Code
- **Consolidation Advice:** Synthesize logic, functions, components, and routes additively into canonical file. Preserve all unique features without deleting business logic.
- **Sequenced Variants:**
  - Variant: `src/components/ui/01_textarea.tsx` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `src/components/ui/02_textarea.tsx` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)
  - Variant: `src/components/ui/03_textarea.tsx` (Source: `iconcraft-studio`, Commit: `bcaf1ffb`)
  - Variant: `src/components/ui/04_textarea.tsx` (Source: `brand-builder-studio`, Commit: `54945eb6`)
  - Variant: `src/components/ui/05_textarea.tsx` (Source: `brand-weaver`, Commit: `0b3ef66b`)
  - Variant: `src/components/ui/06_textarea.tsx` (Source: `macro-mate-logo-icon-27f183d0`, Commit: `124b4231`)
  - Variant: `src/components/ui/07_textarea.tsx` (Source: `brand-forge-studio`, Commit: `f6b80b17`)

### `src/components/ui/toast.tsx`
- **Type:** Source Code
- **Consolidation Advice:** Synthesize logic, functions, components, and routes additively into canonical file. Preserve all unique features without deleting business logic.
- **Sequenced Variants:**
  - Variant: `src/components/ui/01_toast.tsx` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `src/components/ui/02_toast.tsx` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)
  - Variant: `src/components/ui/03_toast.tsx` (Source: `iconcraft-studio`, Commit: `bcaf1ffb`)
  - Variant: `src/components/ui/04_toast.tsx` (Source: `brand-builder-studio`, Commit: `54945eb6`)
  - Variant: `src/components/ui/05_toast.tsx` (Source: `brand-weaver`, Commit: `0b3ef66b`)
  - Variant: `src/components/ui/06_toast.tsx` (Source: `macro-mate-logo-icon-27f183d0`, Commit: `124b4231`)
  - Variant: `src/components/ui/07_toast.tsx` (Source: `brand-forge-studio`, Commit: `f6b80b17`)

### `src/components/ui/toaster.tsx`
- **Type:** Source Code
- **Consolidation Advice:** Synthesize logic, functions, components, and routes additively into canonical file. Preserve all unique features without deleting business logic.
- **Sequenced Variants:**
  - Variant: `src/components/ui/01_toaster.tsx` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `src/components/ui/02_toaster.tsx` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)
  - Variant: `src/components/ui/03_toaster.tsx` (Source: `iconcraft-studio`, Commit: `bcaf1ffb`)
  - Variant: `src/components/ui/04_toaster.tsx` (Source: `brand-builder-studio`, Commit: `54945eb6`)
  - Variant: `src/components/ui/05_toaster.tsx` (Source: `brand-weaver`, Commit: `0b3ef66b`)
  - Variant: `src/components/ui/06_toaster.tsx` (Source: `macro-mate-logo-icon-27f183d0`, Commit: `124b4231`)
  - Variant: `src/components/ui/07_toaster.tsx` (Source: `brand-forge-studio`, Commit: `f6b80b17`)

### `src/components/ui/toggle-group.tsx`
- **Type:** Source Code
- **Consolidation Advice:** Synthesize logic, functions, components, and routes additively into canonical file. Preserve all unique features without deleting business logic.
- **Sequenced Variants:**
  - Variant: `src/components/ui/01_toggle-group.tsx` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `src/components/ui/02_toggle-group.tsx` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)
  - Variant: `src/components/ui/03_toggle-group.tsx` (Source: `iconcraft-studio`, Commit: `bcaf1ffb`)
  - Variant: `src/components/ui/04_toggle-group.tsx` (Source: `brand-builder-studio`, Commit: `54945eb6`)
  - Variant: `src/components/ui/05_toggle-group.tsx` (Source: `brand-weaver`, Commit: `0b3ef66b`)
  - Variant: `src/components/ui/06_toggle-group.tsx` (Source: `macro-mate-logo-icon-27f183d0`, Commit: `124b4231`)
  - Variant: `src/components/ui/07_toggle-group.tsx` (Source: `brand-forge-studio`, Commit: `f6b80b17`)

### `src/components/ui/toggle.tsx`
- **Type:** Source Code
- **Consolidation Advice:** Synthesize logic, functions, components, and routes additively into canonical file. Preserve all unique features without deleting business logic.
- **Sequenced Variants:**
  - Variant: `src/components/ui/01_toggle.tsx` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `src/components/ui/02_toggle.tsx` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)
  - Variant: `src/components/ui/03_toggle.tsx` (Source: `iconcraft-studio`, Commit: `bcaf1ffb`)
  - Variant: `src/components/ui/04_toggle.tsx` (Source: `brand-builder-studio`, Commit: `54945eb6`)
  - Variant: `src/components/ui/05_toggle.tsx` (Source: `brand-weaver`, Commit: `0b3ef66b`)
  - Variant: `src/components/ui/06_toggle.tsx` (Source: `macro-mate-logo-icon-27f183d0`, Commit: `124b4231`)
  - Variant: `src/components/ui/07_toggle.tsx` (Source: `brand-forge-studio`, Commit: `f6b80b17`)

### `src/components/ui/tooltip.tsx`
- **Type:** Source Code
- **Consolidation Advice:** Synthesize logic, functions, components, and routes additively into canonical file. Preserve all unique features without deleting business logic.
- **Sequenced Variants:**
  - Variant: `src/components/ui/01_tooltip.tsx` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `src/components/ui/02_tooltip.tsx` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)
  - Variant: `src/components/ui/03_tooltip.tsx` (Source: `iconcraft-studio`, Commit: `bcaf1ffb`)
  - Variant: `src/components/ui/04_tooltip.tsx` (Source: `brand-builder-studio`, Commit: `54945eb6`)
  - Variant: `src/components/ui/05_tooltip.tsx` (Source: `brand-weaver`, Commit: `0b3ef66b`)
  - Variant: `src/components/ui/06_tooltip.tsx` (Source: `macro-mate-logo-icon-27f183d0`, Commit: `124b4231`)
  - Variant: `src/components/ui/07_tooltip.tsx` (Source: `brand-forge-studio`, Commit: `f6b80b17`)

### `src/components/ui/use-toast.ts`
- **Type:** Source Code
- **Consolidation Advice:** Synthesize logic, functions, components, and routes additively into canonical file. Preserve all unique features without deleting business logic.
- **Sequenced Variants:**
  - Variant: `src/components/ui/01_use-toast.ts` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `src/components/ui/02_use-toast.ts` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)
  - Variant: `src/components/ui/03_use-toast.ts` (Source: `iconcraft-studio`, Commit: `bcaf1ffb`)
  - Variant: `src/components/ui/04_use-toast.ts` (Source: `brand-builder-studio`, Commit: `54945eb6`)
  - Variant: `src/components/ui/05_use-toast.ts` (Source: `brand-weaver`, Commit: `0b3ef66b`)
  - Variant: `src/components/ui/06_use-toast.ts` (Source: `macro-mate-logo-icon-27f183d0`, Commit: `124b4231`)
  - Variant: `src/components/ui/07_use-toast.ts` (Source: `brand-forge-studio`, Commit: `f6b80b17`)

### `src/hooks/use-mobile.tsx`
- **Type:** Source Code
- **Consolidation Advice:** Synthesize logic, functions, components, and routes additively into canonical file. Preserve all unique features without deleting business logic.
- **Sequenced Variants:**
  - Variant: `src/hooks/01_use-mobile.tsx` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `src/hooks/02_use-mobile.tsx` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)
  - Variant: `src/hooks/03_use-mobile.tsx` (Source: `iconcraft-studio`, Commit: `bcaf1ffb`)
  - Variant: `src/hooks/04_use-mobile.tsx` (Source: `brand-builder-studio`, Commit: `54945eb6`)
  - Variant: `src/hooks/05_use-mobile.tsx` (Source: `brand-weaver`, Commit: `0b3ef66b`)
  - Variant: `src/hooks/06_use-mobile.tsx` (Source: `macro-mate-logo-icon-27f183d0`, Commit: `124b4231`)
  - Variant: `src/hooks/07_use-mobile.tsx` (Source: `brand-forge-studio`, Commit: `f6b80b17`)

### `src/hooks/use-toast.ts`
- **Type:** Source Code
- **Consolidation Advice:** Synthesize logic, functions, components, and routes additively into canonical file. Preserve all unique features without deleting business logic.
- **Sequenced Variants:**
  - Variant: `src/hooks/01_use-toast.ts` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `src/hooks/02_use-toast.ts` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)
  - Variant: `src/hooks/03_use-toast.ts` (Source: `iconcraft-studio`, Commit: `bcaf1ffb`)
  - Variant: `src/hooks/04_use-toast.ts` (Source: `brand-builder-studio`, Commit: `54945eb6`)
  - Variant: `src/hooks/05_use-toast.ts` (Source: `brand-weaver`, Commit: `0b3ef66b`)
  - Variant: `src/hooks/06_use-toast.ts` (Source: `macro-mate-logo-icon-27f183d0`, Commit: `124b4231`)
  - Variant: `src/hooks/07_use-toast.ts` (Source: `brand-forge-studio`, Commit: `f6b80b17`)

### `src/index.css`
- **Type:** Source Code
- **Consolidation Advice:** Synthesize logic, functions, components, and routes additively into canonical file. Preserve all unique features without deleting business logic.
- **Sequenced Variants:**
  - Variant: `src/01_index.css` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `src/02_index.css` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)
  - Variant: `src/03_index.css` (Source: `iconcraft-studio`, Commit: `bcaf1ffb`)
  - Variant: `src/04_index.css` (Source: `brand-builder-studio`, Commit: `54945eb6`)
  - Variant: `src/05_index.css` (Source: `brand-weaver`, Commit: `0b3ef66b`)
  - Variant: `src/06_index.css` (Source: `macro-mate-logo-icon-27f183d0`, Commit: `124b4231`)
  - Variant: `src/07_index.css` (Source: `brand-forge-studio`, Commit: `f6b80b17`)

### `src/lib/utils.ts`
- **Type:** Source Code
- **Consolidation Advice:** Synthesize logic, functions, components, and routes additively into canonical file. Preserve all unique features without deleting business logic.
- **Sequenced Variants:**
  - Variant: `src/lib/01_utils.ts` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `src/lib/02_utils.ts` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)
  - Variant: `src/lib/03_utils.ts` (Source: `iconcraft-studio`, Commit: `bcaf1ffb`)
  - Variant: `src/lib/04_utils.ts` (Source: `brand-builder-studio`, Commit: `54945eb6`)
  - Variant: `src/lib/05_utils.ts` (Source: `brand-weaver`, Commit: `0b3ef66b`)
  - Variant: `src/lib/06_utils.ts` (Source: `macro-mate-logo-icon-27f183d0`, Commit: `124b4231`)
  - Variant: `src/lib/07_utils.ts` (Source: `brand-forge-studio`, Commit: `f6b80b17`)

### `src/main.tsx`
- **Type:** Source Code
- **Consolidation Advice:** Synthesize logic, functions, components, and routes additively into canonical file. Preserve all unique features without deleting business logic.
- **Sequenced Variants:**
  - Variant: `src/01_main.tsx` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `src/02_main.tsx` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)
  - Variant: `src/03_main.tsx` (Source: `iconcraft-studio`, Commit: `bcaf1ffb`)
  - Variant: `src/04_main.tsx` (Source: `brand-builder-studio`, Commit: `54945eb6`)
  - Variant: `src/05_main.tsx` (Source: `brand-weaver`, Commit: `0b3ef66b`)
  - Variant: `src/06_main.tsx` (Source: `macro-mate-logo-icon-27f183d0`, Commit: `124b4231`)
  - Variant: `src/07_main.tsx` (Source: `brand-forge-studio`, Commit: `f6b80b17`)

### `src/pages/Index.tsx`
- **Type:** Source Code
- **Consolidation Advice:** Synthesize logic, functions, components, and routes additively into canonical file. Preserve all unique features without deleting business logic.
- **Sequenced Variants:**
  - Variant: `src/pages/01_Index.tsx` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `src/pages/02_Index.tsx` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)
  - Variant: `src/pages/03_Index.tsx` (Source: `iconcraft-studio`, Commit: `bcaf1ffb`)
  - Variant: `src/pages/04_Index.tsx` (Source: `brand-builder-studio`, Commit: `54945eb6`)
  - Variant: `src/pages/05_Index.tsx` (Source: `brand-weaver`, Commit: `0b3ef66b`)
  - Variant: `src/pages/06_Index.tsx` (Source: `macro-mate-logo-icon-27f183d0`, Commit: `124b4231`)
  - Variant: `src/pages/07_Index.tsx` (Source: `brand-forge-studio`, Commit: `f6b80b17`)

### `src/pages/NotFound.tsx`
- **Type:** Source Code
- **Consolidation Advice:** Synthesize logic, functions, components, and routes additively into canonical file. Preserve all unique features without deleting business logic.
- **Sequenced Variants:**
  - Variant: `src/pages/01_NotFound.tsx` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `src/pages/02_NotFound.tsx` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)
  - Variant: `src/pages/03_NotFound.tsx` (Source: `iconcraft-studio`, Commit: `bcaf1ffb`)
  - Variant: `src/pages/04_NotFound.tsx` (Source: `brand-builder-studio`, Commit: `54945eb6`)
  - Variant: `src/pages/05_NotFound.tsx` (Source: `brand-weaver`, Commit: `0b3ef66b`)
  - Variant: `src/pages/06_NotFound.tsx` (Source: `macro-mate-logo-icon-27f183d0`, Commit: `124b4231`)
  - Variant: `src/pages/07_NotFound.tsx` (Source: `brand-forge-studio`, Commit: `f6b80b17`)

### `src/test/example.test.ts`
- **Type:** Source Code
- **Consolidation Advice:** Synthesize logic, functions, components, and routes additively into canonical file. Preserve all unique features without deleting business logic.
- **Sequenced Variants:**
  - Variant: `src/test/01_example.test.ts` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `src/test/02_example.test.ts` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)
  - Variant: `src/test/03_example.test.ts` (Source: `iconcraft-studio`, Commit: `bcaf1ffb`)
  - Variant: `src/test/04_example.test.ts` (Source: `brand-builder-studio`, Commit: `54945eb6`)
  - Variant: `src/test/05_example.test.ts` (Source: `brand-weaver`, Commit: `0b3ef66b`)
  - Variant: `src/test/06_example.test.ts` (Source: `macro-mate-logo-icon-27f183d0`, Commit: `124b4231`)
  - Variant: `src/test/07_example.test.ts` (Source: `brand-forge-studio`, Commit: `f6b80b17`)

### `src/test/setup.ts`
- **Type:** Source Code
- **Consolidation Advice:** Synthesize logic, functions, components, and routes additively into canonical file. Preserve all unique features without deleting business logic.
- **Sequenced Variants:**
  - Variant: `src/test/01_setup.ts` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `src/test/02_setup.ts` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)
  - Variant: `src/test/03_setup.ts` (Source: `iconcraft-studio`, Commit: `bcaf1ffb`)
  - Variant: `src/test/04_setup.ts` (Source: `brand-builder-studio`, Commit: `54945eb6`)
  - Variant: `src/test/05_setup.ts` (Source: `brand-weaver`, Commit: `0b3ef66b`)
  - Variant: `src/test/06_setup.ts` (Source: `macro-mate-logo-icon-27f183d0`, Commit: `124b4231`)
  - Variant: `src/test/07_setup.ts` (Source: `brand-forge-studio`, Commit: `f6b80b17`)

### `src/vite-env.d.ts`
- **Type:** Source Code
- **Consolidation Advice:** Synthesize logic, functions, components, and routes additively into canonical file. Preserve all unique features without deleting business logic.
- **Sequenced Variants:**
  - Variant: `src/01_vite-env.d.ts` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `src/02_vite-env.d.ts` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)
  - Variant: `src/03_vite-env.d.ts` (Source: `iconcraft-studio`, Commit: `bcaf1ffb`)
  - Variant: `src/04_vite-env.d.ts` (Source: `brand-builder-studio`, Commit: `54945eb6`)
  - Variant: `src/05_vite-env.d.ts` (Source: `brand-weaver`, Commit: `0b3ef66b`)
  - Variant: `src/06_vite-env.d.ts` (Source: `macro-mate-logo-icon-27f183d0`, Commit: `124b4231`)
  - Variant: `src/07_vite-env.d.ts` (Source: `brand-forge-studio`, Commit: `f6b80b17`)

### `tailwind.config.ts`
- **Type:** Configuration / Manifest
- **Consolidation Advice:** Synthesize configuration additively into canonical file. Merge all unique dependencies, build scripts, and declarations.
- **Sequenced Variants:**
  - Variant: `01_tailwind.config.ts` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `02_tailwind.config.ts` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)
  - Variant: `03_tailwind.config.ts` (Source: `iconcraft-studio`, Commit: `bcaf1ffb`)
  - Variant: `04_tailwind.config.ts` (Source: `brand-builder-studio`, Commit: `54945eb6`)
  - Variant: `05_tailwind.config.ts` (Source: `brand-weaver`, Commit: `0b3ef66b`)
  - Variant: `06_tailwind.config.ts` (Source: `macro-mate-logo-icon-27f183d0`, Commit: `124b4231`)
  - Variant: `07_tailwind.config.ts` (Source: `brand-forge-studio`, Commit: `f6b80b17`)

### `tsconfig.app.json`
- **Type:** Source Code
- **Consolidation Advice:** Synthesize logic, functions, components, and routes additively into canonical file. Preserve all unique features without deleting business logic.
- **Sequenced Variants:**
  - Variant: `01_tsconfig.app.json` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `02_tsconfig.app.json` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)
  - Variant: `03_tsconfig.app.json` (Source: `iconcraft-studio`, Commit: `bcaf1ffb`)
  - Variant: `04_tsconfig.app.json` (Source: `brand-builder-studio`, Commit: `54945eb6`)
  - Variant: `05_tsconfig.app.json` (Source: `brand-weaver`, Commit: `0b3ef66b`)
  - Variant: `06_tsconfig.app.json` (Source: `macro-mate-logo-icon-27f183d0`, Commit: `124b4231`)
  - Variant: `07_tsconfig.app.json` (Source: `brand-forge-studio`, Commit: `f6b80b17`)

### `tsconfig.json`
- **Type:** Configuration / Manifest
- **Consolidation Advice:** Synthesize configuration additively into canonical file. Merge all unique dependencies, build scripts, and declarations.
- **Sequenced Variants:**
  - Variant: `01_tsconfig.json` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `02_tsconfig.json` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)
  - Variant: `03_tsconfig.json` (Source: `iconcraft-studio`, Commit: `bcaf1ffb`)
  - Variant: `04_tsconfig.json` (Source: `brand-builder-studio`, Commit: `54945eb6`)
  - Variant: `05_tsconfig.json` (Source: `brand-weaver`, Commit: `0b3ef66b`)
  - Variant: `06_tsconfig.json` (Source: `macro-mate-logo-icon-27f183d0`, Commit: `124b4231`)
  - Variant: `07_tsconfig.json` (Source: `brand-forge-studio`, Commit: `f6b80b17`)

### `tsconfig.node.json`
- **Type:** Source Code
- **Consolidation Advice:** Synthesize logic, functions, components, and routes additively into canonical file. Preserve all unique features without deleting business logic.
- **Sequenced Variants:**
  - Variant: `01_tsconfig.node.json` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `02_tsconfig.node.json` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)
  - Variant: `03_tsconfig.node.json` (Source: `iconcraft-studio`, Commit: `bcaf1ffb`)
  - Variant: `04_tsconfig.node.json` (Source: `brand-builder-studio`, Commit: `54945eb6`)
  - Variant: `05_tsconfig.node.json` (Source: `brand-weaver`, Commit: `0b3ef66b`)
  - Variant: `06_tsconfig.node.json` (Source: `macro-mate-logo-icon-27f183d0`, Commit: `124b4231`)
  - Variant: `07_tsconfig.node.json` (Source: `brand-forge-studio`, Commit: `f6b80b17`)

### `vite.config.ts`
- **Type:** Configuration / Manifest
- **Consolidation Advice:** Synthesize configuration additively into canonical file. Merge all unique dependencies, build scripts, and declarations.
- **Sequenced Variants:**
  - Variant: `01_vite.config.ts` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `02_vite.config.ts` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)
  - Variant: `03_vite.config.ts` (Source: `iconcraft-studio`, Commit: `bcaf1ffb`)
  - Variant: `04_vite.config.ts` (Source: `brand-builder-studio`, Commit: `54945eb6`)
  - Variant: `05_vite.config.ts` (Source: `brand-weaver`, Commit: `0b3ef66b`)
  - Variant: `06_vite.config.ts` (Source: `macro-mate-logo-icon-27f183d0`, Commit: `124b4231`)
  - Variant: `07_vite.config.ts` (Source: `brand-forge-studio`, Commit: `f6b80b17`)

### `vitest.config.ts`
- **Type:** Source Code
- **Consolidation Advice:** Synthesize logic, functions, components, and routes additively into canonical file. Preserve all unique features without deleting business logic.
- **Sequenced Variants:**
  - Variant: `01_vitest.config.ts` (Source: `logo-1`, Commit: `c23b83d1`)
  - Variant: `02_vitest.config.ts` (Source: `macro-mate-scripts-fixer-logo-icon`, Commit: `7bd95b99`)
  - Variant: `03_vitest.config.ts` (Source: `iconcraft-studio`, Commit: `bcaf1ffb`)
  - Variant: `04_vitest.config.ts` (Source: `brand-builder-studio`, Commit: `54945eb6`)
  - Variant: `05_vitest.config.ts` (Source: `brand-weaver`, Commit: `0b3ef66b`)
  - Variant: `06_vitest.config.ts` (Source: `macro-mate-logo-icon-27f183d0`, Commit: `124b4231`)
  - Variant: `07_vitest.config.ts` (Source: `brand-forge-studio`, Commit: `f6b80b17`)


## Step-by-Step AI Action Checklist:
- [ ] Read `merge-ai-manifest.json` and inspect `repoSequence[].commitMetadata` and `fileCollisions`.
- [ ] For each collision:
  - [ ] Analyze differences between sequenced variants (`01_<file>`, `02_<file>`, etc.).
  - [ ] For code/config: Synthesize unified implementation into `<file>`.
  - [ ] For visual assets: Preserve distinct media variants side-by-side with descriptive names; verify ambiguities with humans.
  - [ ] Delete temporary sequenced files (`01_*`, `02_*`) after verified synthesis.
- [ ] Ensure non-colliding files maintain correct imports and package names.
- [ ] Verify that no sequenced files remain in the repository tree.
- [ ] Update `merge-ai-manifest.json` setting `fileCollisions[].status = "consolidated"`.
- [ ] Stage and commit the consolidated repository:
      `gitmap cpf "merge-ai - consolidate multi-repo merge into unified codebase"`
