# Project Overview

This is a **logo creation workflow repository** managed by Lovable.

## Purpose
A standardized, repeatable process for generating professional logos, favicons, color palettes, and animated brand assets for any product or project.

## How It Works
1. User triggers logo creation with product name, idea, voice/tone, and sample colors.
2. Lovable follows `.lovable/prompts/02-logo-create.md` to generate everything in one shot.
3. Output lands in `Projects/{Seq}-{PascalCaseName}/` with SVGs, PNGs, GIFs, palette, tokens, and README.
4. Root `favicon.ico`, `favicon.png`, and `gif-animation.gif` are regenerated to match the latest project.

## Active Projects
| Seq | Name | Status |
|-----|------|--------|
| 01 | MacroMate | Completed |
| 02 | ScriptsFixer | Completed (redesigned to fix collision) |

## Key Files
- `.lovable/prompts/02-logo-create.md` — The authoritative spec
- `plan.md` (root) — Mirror of the spec
- `Projects/` — All generated logo projects
