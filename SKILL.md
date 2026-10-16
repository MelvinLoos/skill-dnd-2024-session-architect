---
name: dnd-2024-session-architect
description: "Build complete, Obsidian-ready D&D 5e (2024) session prep notes with full mechanical crunch, Fantasy Statblocks YAML, 2024 Influence/Study social mechanics, and modular frameworks (Lazy DM, 5-Room Dungeon, Tension Pool, Galas, Councils, and optional Campaign modules). Use whenever the user asks to prep a D&D session, one-shot, dungeon, social encounter, political intrigue arc, or adventure note."
license: MIT
metadata:
  author: session-architect
  version: "1.0.0"
---

# D&D 2024 Session Architect

This skill turns a short brief into one copy-pasteable Obsidian note containing a
complete, runnable D&D 5e (2024 rules) session. It combines high-agency prep
frameworks (Lazy DM, 5-Room Dungeon, 3-T Combat, Tension Pool) with the 2024
ruleset's social engine (Influence, Study, Search, Social Hit Points) and emits
both Obsidian callouts and full custom `statblock` YAML.

**The output is always a single outer fence of four backticks (with the
`markdown` language tag) that wraps the entire note.** Never emit the note
without that wrapper.

## Progressive Disclosure Routing Rules

Read auxiliary files on demand — do not load everything upfront. Routing:

| Trigger | Files to load | Why |
| --- | --- | --- |
| Preparing to write the final note (any session) | `references/2024-statblocks-and-crunch.md` **and** `examples/gold-standard-oneshot.md` | Locks in strict 2024 monster math and valid Obsidian `Fantasy Statblocks` YAML syntax; the example is the structural target. |
| The session contains NPCs, negotiations, galas, balls, tavern nights, feasts, tribunals, or council votes | `references/social-gala-council-modules.md` | Provides the Influence/Study matrices, Social HP template, and the Gala / Council modules. |
| The user says the session is part of an ongoing campaign (not a contained one-shot) | `references/campaign-continuity-module.md` | Adds the 3-Faction Triangle, Grim Portents, Bastion integration, and Spiral Seeds. **Skip this file entirely for one-shots.** |

Rule of thumb: **always** read the crunch reference and the gold-standard example
before drafting; read the social module whenever people talk; read the campaign
module only in Campaign Mode. Cite file paths you loaded so the user can audit
your sources.

## Phase 1: Mandatory Pre-Prep Intake

**Never skip this.** Even when the user supplies a detailed brain-dump, pause and
ask **at least 2 and up to 4** targeted, in-depth questions. Ask only what is
missing or what will sharpen the adventure. Cover, at minimum:

1. **Party Specs & Pacing Scope** — What level and party size? Is this a
   **Contained One-Shot** (default) or **Campaign Mode** (unlocks Grim Portents,
   the 3-Faction Triangle turn, and PC Backstory Spiral)?
2. **Core Unstable Situation & Social/Combat Balance** — What is the central
   unstable situation, and does the session need a **Special Social Set-Piece**
   (Alexandrian Gala/Party Mode, or 3-Vote Council Mode) alongside standard
   exploration/combat?
3. **Key Antagonist / VIP Secrets** — Who is the primary boss or political
   obstacle, and what is the one line they will not cross or the secret they are
   hiding?
4. **Tone & Constraints** — Are there specific monsters, hazards, or character
   hooks that must appear? Any table-safety or content limits?

Then **stop and wait for the user's reply** before generating the note. Do not
draft the note in the same turn as the intake questions.

## Phase 2: Obsidian Formatting & Output Rules

These rules are mandatory; broken fences make the note useless to the user.

1. **Quadruple-Backtick Wrapper.** Wrap the ENTIRE Obsidian note inside a single
   outer code block fenced with **four** backticks tagged `markdown`. Inner
   statblock blocks use **three** backticks, so they never split the response.
2. **Obsidian YAML Frontmatter.** Begin the note with clean metadata:
   `tags: [session-prep, dnd-2024, oneshot]` (use `campaign` in Campaign Mode),
   plus `party_level:`, `party_size:`, `estimated_runtime:`, and
   `pacing_engine: tension-pool`.
3. **Wiki-Links.** Wrap every named NPC, Location, Faction, Monster type, and
   Notable Magic Item in `[[Wiki-Links]]` on first mention in each section.
4. **Obsidian Callouts.** Use them consistently:
   - `> [!quote] Read-Aloud` — 2–3 sentence sensory box text opening a scene/location.
   - `> [!warning] DM Secret & Leverage` — hidden traps, twists, NPC vulnerabilities, exact DCs.
   - `> [!tip] Loot & Rewards` — GP, parcels, and 2024 magic items / Bastion rewards.
   - `> [!danger] Tension Complication` — Tension Pool results and Progress Clock triggers.
5. **High Mechanical Crunch (2024 Rules).** Never hand-wave. Always give explicit
   DCs (`DC 14 Wisdom (Insight)`), passive thresholds (`Passive Perception 14+`),
   exact damage dice, conditions, and the 2024 action names — **Study**,
   **Search**, **Influence**, **Utilize**, and **Help**.

## Phase 3: Core Session Document Blueprint

Emit these six sections, in this order, inside the outer fence:

1. **Session Overview, PC Tie-In Hooks & Strong Start.** 2–3 bullets naming the
   unstable situation (who wants what; what happens if the PCs do nothing) and
   3–4 PC-specific hooks, then an in-media-res Strong Start with a
   `Read-Aloud` callout and an immediate mechanical prompt (Search / Study /
   Influence / Initiative).
2. **Pacing Engine: Tension Pool & Scene Clocks.** Every 10 minutes of in-game
   exploration/searching/ritual time adds **1d6** to the pool; reckless noise
   rolls it immediately; at 6d6 roll and clear it. Any **1** triggers a bespoke
   6-entry Session Complication Table. Add 2 active Progress Clocks (`[0/4]` or
   `[0/6]`) stating exactly what ticks each up or down.
3. **10 Location-Agnostic Secrets & Clues Table.** Apply the Three Clue Rule so
   every critical conclusion has at least 3 clues. Columns: `#`, `Secret / Clue`,
   `Passive Threshold (Core Clue)`, `Active 2024 Check (Study / Search /
   Influence)`, `Possible Discovery Nodes`.
4. **Social & Political Encounter Prep.** 3–4 Key NPCs, each with the Universal
   Roleplay Template (appearance/mannerism/voice), 2024 Attitude & Willingness,
   **3 Objections ("Social HP")** with the exact argument/proof/check that breaks
   each, **2 Leverage Points**, and a **Fail-Forward Consequence** (never a dead
   end). See `references/social-gala-council-modules.md`.
5. **The 5-Node Adventure Flow.** Five interconnected nodes following the
   5-Room Dungeon structure (Entrance → Roleplay/Puzzle → Trick/Setback →
   Climax/Boss → Revelation/Twist) with at least one non-linear loop or shortcut.
   Each node carries a `Read-Aloud`, 3 sensory/mechanical details, 1 interactive
   **Treat** usable with the **Utilize** action, and either a **3-T Combat**
   block (**Threat** + a **1d4**-round **Timer** + **Treat**) with *The Monsters
   Know* tactics and retreat/surrender thresholds, or explicit Study/Search/
   Utilize/Influence DCs with multiple solution paths.
6. **Custom 2024 Fantasy Statblocks.** Provide complete inline statblock YAML
   (three-backtick fences tagged `statblock`) for every unique monster, minion
   type, and stat-bearing NPC. Never ship a bare `monster:` link. Validate against
   `references/2024-statblocks-and-crunch.md` before emitting.

## Reference Files

- `references/2024-statblocks-and-crunch.md` — CR math, DC/hazard tables, Weapon
  Mastery riders, and 3 gold-standard statblock YAML templates.
- `references/social-gala-council-modules.md` — Social Action Matrix, Social HP
  template, Gala Module A, and the 3-Vote Council tracker.
- `references/campaign-continuity-module.md` — 3-Faction Triangle, Grim Portents,
  Bastion integration, and Spiral Seeds (Campaign Mode only).
- `examples/gold-standard-oneshot.md` — a finished Level 4 note ("The Velvet
  Ledger") to emulate for structure, tone, and YAML.

## Gotchas

- **Never break the outer block.** 4 backticks outside, 3 backticks inside.
- **Never hand-wave.** Ban "perhaps the players find a clue" and "adjust the DC
  as needed." Write concrete facts, exact DCs, exact GP, and specific smells,
  lighting, and textures.
- **Always ask first.** Two targeted questions minimum, even for a "quick
  goblin dungeon."
- **2024 terminology only.** Use Study/Search/Influence/Utilize/Help and 2024
  statblock formatting — not 2014 "investigation" idioms.

