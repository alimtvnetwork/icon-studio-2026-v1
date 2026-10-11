# Architecture Specification: File Synchronization and Structure Optimization

## Overview
This specification defines the architectural invariants, consolidation strategy, and file system flattening for the multi-repo merge in `icon-studio-2026-v1`. The repository consolidates 7 upstream repositories merged by `gitmap merge-ai`:
1. `alimtvnetwork/logo-1` (01_)
2. `alimtvnetwork/macro-mate-scripts-fixer-logo-icon` (02_)
3. `iconcraft-studio` (03_)
4. `brand-builder-studio` (04_)
5. `brand-weaver` (05_)
6. `macro-mate-logo-icon-27f183d0` (06_)
7. `brand-forge-studio` (07_)

## Architectural Invariants
1. **Zero Business Logic Deletion:** All features, components, routes, utilities, and assets from all 7 source projects are preserved.
2. **Deterministic Flattening:** Temporary sequence prefixes (`01_*`, `02_*`, ..., `07_*`) are stripped and collapsed into canonical target files (`src/App.tsx`, `package.json`, `index.html`, etc.) because the underlying source files are identical across merged repos.
3. **Distinct Asset & Project Idea Preservation:** Independent project directories under `Projects/` (`Projects/01-MacroMate`, `Projects/01-MeetRecorder`, `Projects/02-LvExt`, `Projects/02-ScriptsFixer`, `Projects/03-LvExt`) retain their full folder structures, color palettes, theme tokens, and branding assets.
4. **Strict Relative Git Paths:** All internal references, documentation links, and configuration files use relative paths from the git root (`02-spec/...`, `.ai-memory/...`, `src/...`, `Projects/...`). Absolute paths are strictly banned.
5. **GitMap Primacy:** All symbol inspection, file streaming, and script execution are performed exclusively via `gitmap` commands.

## Target Directory Topology
```text
icon-studio-2026-v1/
├── 02-spec/
│   └── 21-app/
│       └── file-synchronization-and-structure-optimization/
├── .ai-memory/
│   ├── plans/
│   │   ├── file-synchronization-and-structure-optimization.md
│   │   └── subtasks/
│   │       └── file-synchronization-and-structure-optimization/
│   └── temp-agents/
├── .lovable/
│   ├── prompts.md
│   └── prompts/
│       ├── 01-write-memory.md
│       └── 02-logo-create.md
├── public/
│   ├── favicon.ico
│   ├── favicon.png
│   ├── placeholder.svg
│   └── robots.txt
├── src/
│   ├── App.css
│   ├── App.tsx
│   ├── index.css
│   ├── main.tsx
│   ├── vite-env.d.ts
│   ├── components/
│   │   ├── NavLink.tsx
│   │   └── ui/ (48 Shadcn UI components)
│   ├── hooks/
│   │   ├── use-mobile.tsx
│   │   └── use-toast.ts
│   ├── lib/
│   │   └── utils.ts
│   ├── pages/
│   │   ├── Index.tsx
│   │   └── NotFound.tsx
│   └── test/
│       ├── example.test.ts
│       └── setup.ts
├── Projects/
│   ├── 01-MacroMate/
│   ├── 01-MeetRecorder/
│   ├── 02-LvExt/
│   ├── 02-ScriptsFixer/
│   └── 03-LvExt/
├── index.html
├── package.json
├── package-lock.json
├── bun.lockb
├── components.json
├── eslint.config.js
├── postcss.config.js
├── tailwind.config.ts
├── tsconfig.json
├── tsconfig.app.json
├── tsconfig.node.json
├── vite.config.ts
├── vitest.config.ts
├── README.md
├── plan.md
└── merge-ai-manifest.json
```
