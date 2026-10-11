# Execution Plan: file-synchronization-and-structure-optimization

## User Request (Verbatim)
# File Synchronization and Structure Optimization: high priority instruction, non-negotiable task

Can you please follow through this? There is an instruction in the file. Follow through and make it flat. Flat and compact by synchronizing the other files which are similar. So only keep the different ones with the folder structure and the ideas. And finally, let me know that it is done.

## slug: file-synchronization-and-structure-optimization

# Actionable Items Must Follow Non-Negotiable

1. Write spec under 02-spec/21-app/file-synchronization-and-structure-optimization/ and enqueue plan task in .ai-memory/plans/file-synchronization-and-structure-optimization.md (subtasks in .ai-memory/plans/subtasks/file-synchronization-and-structure-optimization/) first
2. Search codebase exclusively via GitMap (gitmap aum search, gitmap find, gitmap cat, gitmap ps, gitmap py, gitmap llm train); TOTAL BAN on rg, ripgrep, grep, git grep, Select-String
3. Strictly use relative Git paths (02-spec/..., .ai-memory/..., cmd/...); only add the relative paths, never add the absolute path during your work, and ensure this is respected on the release page and in release notes as well
4. Use `gitmap` AI agents to enter data
5. Task completion includes committing and pushing to Git
6. Synchronize files to make them flat and compact, keeping only the different ones with the folder structure and ideas.

## Subtasks
1. `Task-01`: Spec & Plan Enqueueing (`02-spec/21-app/file-synchronization-and-structure-optimization/`, `.ai-memory/plans/`)
2. `Task-02`: Source Code & Config Flattening (`src/`, `public/`, root configs)
3. `Task-03`: Projects & Lovable Deduplication (`Projects/01-MacroMate`, `.lovable/`, `merge-ai-manifest.json`)
4. `Task-04`: Verification, Cleanup of Prefixed Artifacts & Atomic GitMap Commit/Push

## Acceptance Criteria
- [ ] Canonical root files exist: `package.json`, `index.html`, `vite.config.ts`, `tailwind.config.ts`, `tsconfig.json`, `README.md`, `plan.md`.
- [ ] Canonical `src/` files exist: `src/App.tsx`, `src/App.css`, `src/index.css`, `src/main.tsx`, `src/components/`, `src/hooks/`, `src/lib/`, `src/pages/`, `src/test/`.
- [ ] No temporary sequence prefixes (`01_*` through `07_*`) remain in the repository.
- [ ] `Projects/` retains all 5 distinct project folders and ideas (`01-MacroMate`, `01-MeetRecorder`, `02-LvExt`, `02-ScriptsFixer`, `03-LvExt`).
- [ ] `merge-ai-manifest.json` updated with `consolidated` status for all collisions.
- [ ] Atomic commit and push executed using GitMap hyphen-separated command (`gitmap cpf "<module> - <summary>"`).
