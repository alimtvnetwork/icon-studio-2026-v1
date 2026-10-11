# Decision: Logo Spec Lives in File System, Not mem://

**Date:** This session
**Context:** User provided a comprehensive logo creation spec and explicitly instructed that it be saved to the project file system.

## Decision
The full logo creation spec lives ONLY in:
- `.lovable/prompts/02-logo-create.md` (authoritative)
- `plan.md` at repo root (mirror)

It is NOT mirrored in `mem://` beyond a one-line Core pointer.

## Rationale
- File system is the single source of truth
- `mem://` is for runtime rules, not full specs
- Next AI sessions need to read the file, not rely on memory injection
- Prevents drift between memory and file system

## Consequence
Any AI session starting fresh must read `.lovable/prompts/02-logo-create.md` or `plan.md` to understand the logo workflow.
