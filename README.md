# D&D 2024 Session Architect

A Claude Agent Skill that turns a short brief into one copy-pasteable Obsidian
note containing a complete, runnable **Dungeons & Dragons 5e (2024 rules)**
session — full mechanical crunch, Fantasy Statblocks YAML, the 2024
Influence/Study social engine, and modular prep frameworks.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE.txt)
[![Version](https://img.shields.io/badge/version-1.0.0-blue.svg)](SKILL.md)
[![Ruleset](https://img.shields.io/badge/ruleset-D%26D%205e%202024-red.svg)](references/2024-statblocks-and-crunch.md)

---

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Repository Structure](#repository-structure)
- [Requirements](#requirements)
- [Installation](#installation)
- [Usage](#usage)
- [How It Works](#how-it-works)
- [Reference Files](#reference-files)
- [Contributing](#contributing)
- [License & Attribution](#license--attribution)

---

## Overview

**D&D 2024 Session Architect** combines high-agency prep frameworks (Lazy DM,
5-Room Dungeon, 3-T Combat, Tension Pool) with the 2024 ruleset's social engine
(**Influence**, **Study**, **Search**, **Social Hit Points**) to produce a single
Obsidian-ready session note. It emits both Obsidian callouts and full custom
`statblock` YAML, never hand-waving DCs, damage, or monster math.

The skill is designed around **progressive disclosure**: only the reference files
relevant to the current session are loaded, keeping context small and output
focused.

## Features

- **One copy-pasteable note** — the entire session prep wrapped in a single
  four-backtick `markdown` fence, ready to drop into Obsidian.
- **2024 rules accuracy** — Study/Search/Influence/Utilize/Help actions, 2024
  monster statistics by CR, hazard severities, and Weapon Mastery riders.
- **Valid Fantasy Statblocks YAML** — complete inline statblocks (three-backtick,
  `statblock`-tagged) for every unique monster, minion, and stat-bearing NPC.
- **Social & political modules** — the 2024 Social Action Matrix, Social HP
  template, Alexandrian Gala, and 3-Vote Council trackers.
- **Campaign continuity (optional)** — 3-Faction Triangle, Grim Portents, Bastion
  integration, and Spiral Seeds for multi-session play.
- **Pacing engine** — Tension Pool (`1d6` accumulation, complications on a `1`)
  plus explicit Progress Clocks.
- **Non-linear adventure flow** — a 5-node 5-Room Dungeon structure with at least
  one loop or shortcut.

## Repository Structure

```
skill-dnd-2024-session-architect/
├── SKILL.md                              # Entry point: trigger, routing, workflow, output rules
├── references/
│   ├── 2024-statblocks-and-crunch.md     # CR math, DC/hazard tables, statblock YAML templates
│   ├── social-gala-council-modules.md    # Social Action Matrix, Social HP, Gala & Council modules
│   └── campaign-continuity-module.md     # 3-Faction Triangle, Grim Portents (Campaign Mode only)
├── examples/
│   └── gold-standard-oneshot.md          # Finished Level 4 note ("The Velvet Ledger") to emulate
├── LICENSE.txt                           # MIT license + Wizards of the Coast attribution
└── README.md                             # This file
```

## Requirements

- A Claude client that supports **Agent Skills** (project or user skills).
- [Obsidian](https://obsidian.md/) for using the generated notes.
- The [Fantasy Statblocks](https://github.com/valentine195/obsidian-5e-statblocks)
  community plugin (recommended) for rendering the embedded `statblock` YAML.
- No build step, package manager, or external dependencies — the skill is pure
  Markdown.

## Installation

### As a project skill

Copy the whole directory into your project's skills folder:

```bash
git clone https://github.com/<owner>/skill-dnd-2024-session-architect.git \
  .claude/skills/dnd-2024-session-architect
```

The skill is then discovered automatically by its `SKILL.md` metadata.

### As a personal (user-level) skill

Clone it into your user-level skills directory, for example:

```bash
git clone https://github.com/<owner>/skill-dnd-2024-session-architect.git \
  ~/.claude/skills/dnd-2024-session-architect
```

> Replace `<owner>` with the actual repository owner.

## Usage

Once installed, simply ask Claude to prep a session. The skill triggers on
requests such as:

- "Prep a D&D session for tonight — level 5 party, a haunted lighthouse."
- "Build me a one-shot with a masquerade heist and a boss fight."
- "Design a political intrigue arc with a council vote."
- "Create a 5-room dungeon for a level 3 party."

### Example prompt

```text
Prep a contained one-shot for a level 4 party of four players.
Theme: a masquerade auction on the docks; the focus is a social set-piece
plus one boss encounter. Tone: tense, high-society intrigue.
```

The skill will first ask **2–4 targeted intake questions** (party specs, core
unstable situation, antagonist secrets, tone/safety constraints) and wait for
your reply before drafting the note.

## How It Works

The skill follows a three-phase workflow defined in [`SKILL.md`](SKILL.md):

1. **Phase 1 — Mandatory Pre-Prep Intake.** Pause and ask 2–4 targeted questions
   before generating anything. Never drafted in the same turn as the questions.
2. **Phase 2 — Obsidian Formatting & Output Rules.** Enforce the quadruple-backtick
   wrapper, YAML frontmatter, wiki-links, standard callouts, and high mechanical
   crunch.
3. **Phase 3 — Core Session Document Blueprint.** Emit the six required sections
   in order: Overview & Strong Start, Pacing Engine, Secrets & Clues, Social &
   Political Prep, the 5-Node Adventure Flow, and Custom 2024 Statblocks.

A **routing table** in `SKILL.md` decides which reference files to load on demand
(crunch + example always; social module when people talk; campaign module only in
Campaign Mode).

## Reference Files

| File | Purpose |
| --- | --- |
| [`references/2024-statblocks-and-crunch.md`](references/2024-statblocks-and-crunch.md) | CR math, DC/hazard tables, Weapon Mastery riders, and gold-standard statblock YAML templates. |
| [`references/social-gala-council-modules.md`](references/social-gala-council-modules.md) | Social Action Matrix, Social HP template, Gala Module A, and the 3-Vote Council tracker. |
| [`references/campaign-continuity-module.md`](references/campaign-continuity-module.md) | 3-Faction Triangle, Grim Portents, Bastion integration, and Spiral Seeds (Campaign Mode only). |
| [`examples/gold-standard-oneshot.md`](examples/gold-standard-oneshot.md) | A finished Level 4 note ("The Velvet Ledger") to emulate for structure, tone, and YAML. |

## Contributing

Contributions are welcome. To keep the skill reliable:

1. Fork the repository and create a feature branch.
2. Keep the outer **four-backtick** wrapper intact and internal statblocks at
   **three** backticks — a broken fence makes a note unusable.
3. Use **2024 terminology only** (Study/Search/Influence/Utilize/Help) and back
   every claim with explicit DCs, damage dice, and conditions.
4. Validate any new statblock YAML against the pre-flight checklist at the end of
   [`references/2024-statblocks-and-crunch.md`](references/2024-statblocks-and-crunch.md).
5. Follow [Conventional Commits](https://www.conventionalcommits.org/) for commit
   messages.

## License & Attribution

Released under the [MIT License](LICENSE.txt).

This skill's reference material is game content formatted for use with *Dungeons &
Dragons 5th Edition (2024 rules)*. Dungeons & Dragons and D&D are trademarks of
Wizards of the Coast. This skill is an independent work and is **not affiliated
with, endorsed by, or sponsored by** Wizards of the Coast.
