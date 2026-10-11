# Logo Creation Instruction — Verbatim

> Original user spec, captured verbatim.

---

Please instruct Lovable to create a logo for me. The instruction should be saved into the project file system as well, so it knows how to create a logo. I will give the product name, a little bit of product idea based on the voice, and a sample color and things like that. It would generate the project name first at the root level. So there should be a folder named `Projects`, and inside that it will have `01`, `02`, `03`, etc., project name

## Key Spec Points

1. Prompt saved to `.lovable/prompts/02-logo-create.md` and mirrored at root `plan.md`
2. Folder structure: `Projects/{Seq}-{PascalCaseProjectName}/`
3. Sequence: zero-padded 2-digit, auto-increment
4. Never overwrite existing project folders
5. Dark + white variants default to ON
6. All prompts in file system, not `mem://`
7. Generate everything in one shot unless user asks for phased delivery

## User Feedback During Session

### ScriptsFixer Redesign
> "For the scripts fixture, could you please move this, uh, this, let's say, arm type, uh, element or what could we say? We, we could just remove it and probably use different stuff. But idea here is should not collide one item with the another, okay? Make sure of that"

**Action taken:** Removed overlapping wrench element from ScriptsFixer logo. Replaced with a non-overlapping checkmark + spark badge in the bottom-right corner, keeping `</>` brackets in upper-left. This ensures zero collision between elements.
