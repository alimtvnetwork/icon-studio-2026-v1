# Lovable Prompt Index

Canonical index of saved prompt instructions. All prompts live in `.lovable/prompts/`.
Never duplicate these into `mem://` — the file system is the single source of truth.

| ID | File | Triggers | Purpose |
|---|------|----------|---------|
| 01 | [01-write-memory.md](./prompts/01-write-memory.md) | `write memory`, `end memory`, `update memory` | End-of-session memory persistence across AI sessions. |
| 02 | [02-logo-create.md](./prompts/02-logo-create.md) | `create logo`, `make logo`, `logo`, `create icon`, `make icon`, `design logo`, `new logo` | Generate a complete logo project (SVGs, raster set, palette, favicon, README) under `Projects/{NN}-{PascalName}/`. |
