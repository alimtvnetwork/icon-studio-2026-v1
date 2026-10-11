---
name: file-synchronization-and-structure-optimization
description: >-
  File synchronization and structure optimization skill to flatten, compact, and synchronize merged repositories while preserving unique assets, ideas, and folder structures.
---

# File Synchronization and Structure Optimization Skill

## Non-Negotiable Operational Rules
1. Flatten temporary sequence-prefixed files (`01_*`, `02_*`, etc.) into clean canonical file paths.
2. Synchronize identical and similar files to make the repository flat and compact.
3. Keep unique and distinct ideas, folder structures, and assets (logos, icons, themes, tokens, project readmes) preserved under `Projects/` or their respective project directories.
4. Total ban on `rg`, `ripgrep`, `grep`, `git grep`, `Select-String`. Exclusively use GitMap (`gitmap aum search`, `gitmap find`, `gitmap cat`, `gitmap ps`, `gitmap py`).
5. Strictly use relative Git paths across all specs, plans, documentation, and commits.
6. Commit and push via GitMap hyphen-separated command (`gitmap cpf "<module> - <summary>"`).
