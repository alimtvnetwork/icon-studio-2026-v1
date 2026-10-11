# Coding Guidelines

> Read before writing any code. Also read: spec/, spec/error-manage/ (if present),
> language-specific guidelines, Boolean guidelines, Enum guidelines, error-management guidelines.

1. Functions ≤ 8 lines.
2. No nested ifs.
3. Ifs stay simple — prefer positive conditions, no negatives.
4. Follow Boolean guidelines: boolean names are prefixed `is` or `has`; no negative names.
5. Use proper types — never `any` / `unknown` / `interface{}` / wide-open types. `Generic<T>` is fine.
6. Never swallow errors — every `catch` logs per the error-management + logging guidelines.
7. No file or class > 80–100 lines.
8. No magic strings or numbers — use Enum or Constants.
9. Definitions live in their own files, not inline.
10. Reusability is the highest priority — keep code DRY.
11. React/TS components: as small as possible, reusable. For many components, draft a mermaid diagram in the plan first.
12. If `spec/error-manage/` exists, every error handler must follow it.
13. Prefer immutable, single-assignment variables (Rust-style). Mutate only loop indices or where strictly necessary.
14. Assets go in `/assets/XX-folder-name/XX-file-name.<ext>` with numeric sequence prefixes.
15. Enums and constants live in dedicated files, not inline.

## Logo Workflow Specific
- All paths relative in README.md so GitHub renders inline.
- PascalCase for folders, file stems, JSON keys.
- Sequence numbers: zero-padded 2-digit (`01`, `02`).
- Raster sizes: 3-digit pad below 1000 (`Logo-052.png`); `Logo-1024-Light.png` / `Logo-1024-Dark.png`.
- No spaces in any path.
