# 2024 Statblocks & Crunch

Reference for building mechanically-tight D&D 5e (2024) sessions: monster math,
DC and hazard severity, Weapon Mastery riders, and gold-standard Obsidian
`Fantasy Statblocks` YAML.

> **Precedence rule.** If a creature exists in the 2024 *Monster Manual*, use the
> printed statblock. The tables below exist to (a) calibrate homebrew and named
> NPCs and (b) sanity-check that a printed creature is appropriate for the party.

## 1. 2024 Monster Statistics by Challenge Rating

Use this to build or upscale homebrew creatures. **HP ranges are the intended
"fight length" band, not a single number** — pick a value low in the band for a
skirmisher, high for a bruiser. **Initiative Bonus** reflects 2024's design push
toward faster monsters (Dex modifier plus, for bosses, Proficiency Bonus).

| CR | Prof. Bonus | Armor Class | Hit Points (range) | Attack Bonus | Save DC | Damage/Round (DPR) | Initiative Bonus |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1/4 | +2 | 13 | 36–49 | +3 | 10 | 4–5 | +1 to +2 |
| 1/2 | +2 | 13 | 50–70 | +3 | 10 | 6–8 | +1 to +2 |
| 1 | +2 | 13 | 71–85 | +3 | 11–12 | 9–14 | +2 to +3 |
| 2 | +2 | 13 | 86–100 | +3 | 12–13 | 15–20 | +2 to +3 |
| 3 | +2 | 13–14 | 101–115 | +4 | 13–14 | 21–26 | +2 to +4 |
| 4 | +2 | 14 | 116–130 | +5 | 14 | 27–32 | +2 to +4 |
| 5 | +3 | 15 | 131–145 | +6 | 15–16 | 33–38 | +3 to +5 |
| 6 | +3 | 15 | 146–160 | +6 | 16 | 39–44 | +3 to +5 |
| 7 | +3 | 15 | 161–175 | +6 | 17 | 45–50 | +3 to +5 |
| 8 | +3 | 16 | 176–190 | +7 | 17–18 | 51–56 | +3 to +6 |
| 9 | +4 | 16 | 191–205 | +7 | 17–18 | 57–62 | +4 to +6 |
| 10 | +4 | 17 | 206–220 | +7 | 18–19 | 63–68 | +4 to +6 |
| 11 | +4 | 17 | 221–235 | +8 | 19–20 | 69–74 | +4 to +7 |
| 12 | +4 | 17 | 236–250 | +8 | 19–20 | 75–80 | +4 to +7 |
| 13 | +5 | 18 | 251–265 | +8 | 19–20 | 81–86 | +5 to +8 |
| 14 | +5 | 18 | 266–280 | +8 | 19–20 | 87–92 | +5 to +8 |
| 15 | +5 | 18 | 281–295 | +9 | 19–20 | 93–98 | +5 to +8 |

**Using the table.**

- **DPR is the whole creature's round**, including Multiattack. If a creature has
  three attacks, divide DPR by 3 and round for each hit.
- **Solo Boss adjustment.** A single creature against a full party needs roughly
  **1.5–2× the HP band** and a **Legendary Resistance / Recovery** trait to
  survive focused fire (see Template 3). Add **minions** to absorb action economy.
- **Save DC** applies to the creature's own forced effects (breath, spells,
  conditions). Do not stack a new save on every individual claw hit — bake the
  rider in (see §3).

## 2. Difficulty Class & Hazard Severity

### Standard DCs (2024)

| Difficulty | DC | When to use |
| --- | --- | --- |
| Very Easy | 5 | Anyone could do it; roll only to add tension. |
| Easy | 10 | Trained or lucky characters succeed routinely. |
| Medium | 15 | The default "meaningful risk" check. |
| Hard | 20 | Specialists with Advantage or high rolls. |
| Very Hard | 25 | Requires the right tool, spell, or Leverage. |
| Nearly Impossible | 30 | Legendary feats; the answer is usually a plan, not a die. |

### Improvised Damage & Hazard Table (by Tier)

Match severity to the fiction. **Nuisance** chips resources, **Deadly** threatens
a character's turn, **Lethal** can drop a PC from full if it lands.

| Tier (Levels) | Nuisance | Deadly | Lethal |
| --- | --- | --- | --- |
| 1–4 (Tier 1) | 1d10 (5) | 2d10 (11) | 4d10 (22) |
| 5–10 (Tier 2) | 2d10 (11) | 4d10 (22) | 10d10 (55) |
| 11–16 (Tier 3) | 4d10 (22) | 10d10 (55) | 18d10 (99) |
| 17–20 (Tier 4) | 10d10 (55) | 18d10 (99) | 24d10 (132) |

**Format hazards with all four parts:** trigger, save (ability + DC), damage
(with half-on-save noted), and aftermath (`Prone`, blocked route, or a Tension
Pool tick).

> **Example:** Rusted cargo winch snaps. Any creature in the 10-ft. cone makes a
> **DC 14 Dexterity save**, taking **22 (4d10) bludgeoning damage** on a failure,
> or half as much on a success, and is knocked **Prone**.

## 3. 2024 Weapon Mastery & Tactical Traits Quick-Reference

2024 Weapon Masteries let a mundane attack do something *extra* without adding a
second roll. **Bake the mastery directly into the attack's `desc:` string** so
the DM never has to look it up mid-combat.

| Mastery | Effect to bake into the attack description |
| --- | --- |
| **Cleave** | On a hit, one creature within 5 ft. of the target takes ability-modifier damage (no new roll). |
| **Graze** | On a **miss**, the target still takes ability-modifier damage. |
| **Nick** | Make the extra Light-weapon attack as part of the Attack action (frees the Bonus Action). |
| **Push** | On a hit, push the target up to 10 ft. straight away (Large-or-smaller only). |
| **Sap** | On a hit, the target has **Disadvantage** on its next attack roll before your next turn. |
| **Slow** | On a hit, reduce the target's Speed by 10 ft. until your next turn. |
| **Topple** | On a hit, **DC = 8 + Prof. + ability mod**; on a failed **Constitution** save the target is **Prone**. |
| **Vex** | On a hit, you gain **Advantage** on your next attack against that same target before your next turn. |

### Baking rider conditions into an attack (no second save)

2024 attack actions apply their rider condition on a hit, end-timed to the
creature's next turn, rather than granting a fresh save every swing:

- **Poisoned** — "…and the target has the **Poisoned** condition until the start
  of the creature's next turn."
- **Prone** — grant it via **Topple** only (that is where the 2024 save lives) or
  via an explicit shove.
- **Restrained** — reserve for a named grapple/hold action with an escape DC, not
  a routine hit; it is very strong.
- **Dazed / Incapacitated** — esoteric; gate behind a recharge (Recharge 5–6) or
  a legendary/boss action, and cap it at "until the start of the target's next
  turn."

### Tactical traits worth reusing

- **Pack Tactics.** Advantage on an attack against a target if an ally is within
  5 ft. of it and not Incapacitated.
- **Nimble Escape.** Bonus Action: Disengage or Hide.
- **Bloodied (2024 semantics).** Many 2024 statblocks key reactions off the
  **Bloodied** condition (half HP or fewer). Use it as the Trigger for a boss's
  desperation move, or as the threshold at which minions flee.
- **Battlefield timer (the "second T").** Give the fight a **1d4-round** event
  (rising tide, ritual tick, collapsing floor) so stalling costs the party.


## 4. Gold-Standard Obsidian `Fantasy Statblocks` YAML Templates

### YAML lint rules (apply to EVERY block)

1. **Quote any string containing a colon.** `desc: "Melee Attack Roll: +5…"` —
   an unquoted `:` inside a value breaks the YAML parse.
2. **Never use tabs.** Indent with 2 spaces for mapping keys, 2 more for list
   items, and 4 for the `name`/`desc` children of a list item.
3. **`stats` is a flat array in fixed order:** `[STR, DEX, CON, INT, WIS, CHA]`.
   Values are the **ability scores** (e.g. 16), not the modifiers.
4. **`saves`/`skillsaves` are arrays of single-key maps** using the standard
   three-letter/name key and the **total modifier** including ability and
   proficiency: `- dex: 5`.
5. **Empty optional fields use `""`**, never `null` or a blank value.
6. **`cr` accepts fractions as strings:** `cr: 1/2`, `cr: 1/4`.
7. **`senses` carries both passive and Initiative** in the 2024 style:
   `Passive Perception 13, Initiative +3 (13)` — the parenthetical is the
   equivalent static Initiative score the DM can compare against.
8. **Fence the block with three backticks carrying the `statblock` language tag,
   and close with three bare backticks.** Inside the final session note these
   3-backtick fences sit within the outer 4-backtick wrapper.
9. **Every `actions`/`bonus_actions`/`reactions`/`legendary_actions` entry needs
   exactly one `name` and one `desc`.**
10. **Damage notation is `average (dice + mod) type`:** `11 (2d6 + 4) Piercing`.
    Always give the printed average first.

### Template 1 — 2024 Skirmisher / Minion (CR 1/2)

A fast, disposable lane-holder. Steady DPR stays in the CR band; the Recharge
adds a burst spike. Note how **Vex** is baked into the attack and **Nick**-style
pressure is delivered via a bonus action instead of a second save.

```statblock
name: Lantern-Cutter
size: Medium
type: Humanoid
alignment: Neutral Evil
ac: 13 (Leather Armor)
hp: 52
hit_dice: 8d8 + 16
speed: 30 ft.
stats: [10, 16, 14, 10, 12, 10]
saves:
  - dex: 5
skillsaves:
  - stealth: 5
  - perception: 3
damage_resistances: ""
damage_immunities: ""
condition_immunities: ""
senses: Passive Perception 13, Initiative +3 (13)
languages: Common, Thieves' Cant
cr: 1/2
traits:
  - name: Pack Tactics
    desc: "The cutter has Advantage on an attack roll against a creature if at least one of the cutter's allies is within 5 ft. of the creature and that ally isn't Incapacitated."
  - name: Lantern Signal
    desc: "While holding its hooded lantern, the cutter can use a Bonus Action to flash a signal. Up to three allied Lantern-Cutters that can see it can immediately move 5 ft. without provoking Opportunity Attacks."
actions:
  - name: Scimitar
    desc: "Melee Attack Roll: +5, reach 5 ft. Hit: 6 (1d6 + 3) Slashing damage, and the cutter has Advantage on its next attack roll against the target before the end of its next turn (Vex)."
  - name: Hand Crossbow
    desc: "Ranged Attack Roll: +5, range 30/120 ft. Hit: 6 (1d6 + 3) Piercing damage."
  - name: Two-Blade Flurry (Recharge 5-6)
    desc: "The cutter makes two Scimitar attacks against one creature or two creatures within 5 ft. of it. If both hit the same creature, that creature has the Poisoned condition until the start of the cutter's next turn."
bonus_actions:
  - name: Nimble Escape
    desc: "The cutter takes the Disengage or Hide action."
reactions:
  - name: Slip the Noose
    desc: "Trigger: A creature the cutter can see moves within 5 ft. of it. Response: The cutter moves up to 10 ft. without provoking Opportunity Attacks."
```

**Retreat threshold:** at **Bloodied** (26 HP or fewer) or when two allies drop,
the surviving cutters flee toward the nearest exit and will not fight to the
death — they would rather sell the location of the party's base to their patron.


### Template 2 — 2024 Spellcaster / VIP (CR 5)

A named antagonist with a face, a voice, and getaway magic. Note the 2024 pattern:
a **Multiattack of spell attacks** for reliable DPR, a day-based `spells:` list
instead of slot tracking, and a Bonus Action escape. Save DC (15) equals
`8 + Proficiency (+3) + Intelligence modifier (+4)`.

```statblock
name: Tidewright Vesper
size: Medium
type: Humanoid
alignment: Lawful Evil
ac: 15 (Mage Armor)
hp: 132
hit_dice: 24d8 + 24
speed: 30 ft.
stats: [8, 14, 14, 18, 13, 12]
saves:
  - int: 7
  - wis: 4
skillsaves:
  - arcana: 7
  - deception: 4
  - investigation: 7
damage_resistances: cold
damage_immunities: ""
condition_immunities: ""
senses: Passive Perception 11, Initiative +2 (12)
languages: Common, Aquan, Thieves' Cant
cr: 5
traits:
  - name: Ledger Ward
    desc: "While Vesper's spellbook, The Velvet Ledger, is on her person, she has Advantage on Constitution saving throws made to maintain Concentration."
  - name: Salt-Bound
    desc: "Vesper ignores difficult terrain and the Frightened condition while she is within 60 ft. of open water."
actions:
  - name: Multiattack
    desc: "Vesper makes three Arcane Burst attacks."
  - name: Arcane Burst
    desc: "Melee or Ranged Spell Attack Roll: +7, reach 5 ft. or range 120 ft. Hit: 11 (2d6 + 4) Force damage."
  - name: Undertow Lash (Recharge 5-6)
    desc: "Vesper lashes a 15-ft. cone. Each creature there makes a DC 15 Strength saving throw. On a failure, it takes 22 (4d8 + 4) Cold damage and is pulled 10 ft. toward Vesper. On a success, it takes half damage and is not moved."
bonus_actions:
  - name: Tidepool Step
    desc: "Vesper teleports into an unoccupied space she can see within 30 ft. that is within 5 ft. of standing water or a water-bearing vessel."
reactions:
  - name: Ward of the Ledger
    desc: "Trigger: Vesper is hit by an attack she can see. Response: She gains a +3 bonus to her AC against that attack, potentially causing it to miss."
spells:
  - "At will: arcane lock, mage hand, minor illusion, prestidigitation"
  - "3/day each: invisibility, misty step, shield"
  - "1/day each: counterspell, dimension door, greater invisibility"
```

**Parley window.** Vesper is a **Willing** entity once the party proves they hold
`The Velvet Ledger`'s cipher key: she would rather negotiate a split than lose her
grip on the harbour ledger (see her Social HP block in the social module).


### Template 3 — 2024 Solo Boss (CR 6, uplifted for a party of four)

A boss must survive four focused turns. Note the **elevated Initiative**, the
**condition-recovery trait**, **Legendary Resistance**, a **Bloodied-keyed
Reaction**, and 3 **legendary actions** that spend the party's attention. HP is
~1.5× the printed CR 6 band because it fights alone.

```statblock
name: The Salt Warden
size: Large
type: Giant
alignment: Neutral Evil
ac: 16 (Natural Armor)
hp: 231
hit_dice: 22d10 + 110
speed: 30 ft., swim 40 ft.
stats: [20, 12, 18, 8, 14, 10]
saves:
  - str: 8
  - con: 7
skillsaves:
  - athletics: 8
  - perception: 5
damage_resistances: cold, poison
damage_immunities: ""
condition_immunities: prone
senses: Passive Perception 15, Initiative +5 (15)
languages: Common, Giant, Aquan
cr: 6
traits:
  - name: Legendary Resistance (3/Day)
    desc: "If the Warden fails a saving throw, it can choose to succeed instead."
  - name: Salt-Born Recovery
    desc: "At the start of each of its turns, the Warden ends one condition on itself from the following: Blinded, Charmed, Deafened, Frightened, or Restrained."
  - name: Brine Aura
    desc: "The ground within 10 ft. of the Warden is slippery brine; it is difficult terrain for creatures other than the Warden."
actions:
  - name: Multiattack
    desc: "The Warden makes two Salt-Gauntlet attacks and uses Undertow Grasp if it is available."
  - name: Salt-Gauntlet
    desc: "Melee Attack Roll: +8, reach 10 ft. Hit: 14 (2d8 + 5) Bludgeoning damage plus 4 (1d8) Cold damage, and the target has the Poisoned condition until the start of the Warden's next turn."
  - name: Undertow Grasp (Recharge 5-6)
    desc: "The Warden lashes a 20-ft. cone of brine. Each creature there makes a DC 16 Strength saving throw. On a failure, it takes 22 (4d8 + 4) Cold damage, is pulled 10 ft. toward the Warden, and has the Restrained condition until the end of its next turn. On a success, it takes half damage and is not moved."
  - name: Tidal Roar (Recharge 6)
    desc: "Each creature within 20 ft. of the Warden makes a DC 16 Constitution saving throw. On a failure, it takes 18 (4d8) Thunder damage and is pushed 10 ft. away and knocked Prone. On a success, it takes half damage and is not moved."
bonus_actions:
  - name: Drownstep
    desc: "The Warden moves up to half its Speed without provoking Opportunity Attacks. It can move through the space of a Medium-or-smaller creature, which must succeed on a DC 16 Dexterity saving throw or fall Prone."
reactions:
  - name: Undertow Retort
    desc: "Trigger: A creature within 10 ft. of the Warden hits it with a melee attack. Response: The creature must succeed on a DC 16 Strength saving throw or be Grappled (escape DC 16) by the Warden."
  - name: Bloodied Surge
    desc: "Trigger: The Warden becomes Bloodied (115 HP or fewer). Response: It immediately recharges Undertow Grasp and uses it."
legendary_actions:
  - name: Tide Slam
    desc: "The Warden makes one Salt-Gauntlet attack."
  - name: Dread Current
    desc: "One creature the Warden can see within 60 ft. makes a DC 16 Wisdom saving throw or has the Frightened condition until the end of its next turn."
  - name: Roiling Brine (Costs 2 Actions)
    desc: "The Warden churns the brine. Each creature within 10 ft. makes a DC 16 Constitution saving throw, taking 10 (3d6) Cold damage on a failure, or half as much on a success."
```

**The Monsters Know.** The Warden opens with **Tidal Roar** to break formation,
then **Undertow Grasp** to drag a squishy caster into **Brine Aura** and grind it
down. It targets the lowest-AC creature it can reach, ignores the tank unless
that tank is the only target, and spends **Legendary Resistance** on the first
save-or-lose effect aimed at it. At **Bloodied** it becomes *Unwilling* to flee
(it cannot leave the water) and fights to destruction.

### Pre-flight checklist before emitting any statblock

- [ ] Every `desc` that contains `:` is wrapped in double quotes.
- [ ] `stats` is six ability **scores** in `[STR, DEX, CON, INT, WIS, CHA]` order.
- [ ] `senses` includes both Passive Perception and `Initiative +X (score)`.
- [ ] Save DCs equal `8 + Proficiency Bonus + ability modifier`.
- [ ] Attack bonuses equal `Proficiency Bonus + ability modifier`.
- [ ] DPR of the full round sits inside the CR band (×1.5–2 for solo bosses).
- [ ] No tabs anywhere in the YAML.

