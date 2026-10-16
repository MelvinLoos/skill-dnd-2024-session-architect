> **Reference output, not instructions.** Everything between the opening
> four-backtick fence and the closing one is the exact *shape* of a finished
> note — copy this structure, not this content.

````markdown
---
tags: [session-prep, dnd-2024, oneshot]
party_level: 4
party_size: 4
estimated_runtime: 4 hours
pacing_engine: tension-pool
---

# The Velvet Ledger

A masquerade heist above [[Gullrock Sea-Cave]]. The smuggler syndicate
[[The Velvet Ledger]] is auctioning a stolen harbour register tonight, upstairs,
while the real ledger changes hands on the tide below.

## 1. Session Overview & Strong Start

**Situation Summary**

- [[Tidewright Vesper]] is selling the [[Harbour Register]] to [[Lord Halvard]]
  at midnight, upstairs, during the masquerade — and the sea-gate closes an hour later.
- [[Sister Anneke]] has smuggled a witness into the cellars who can testify the
  Register is a forgery; she will die if the tide rises with her still below.
- If the party does nothing: Halvard buys the Register, Anneke drowns, and the
  syndicate's grip on the docks hardens into law.

**PC Tie-In Hooks**

- The party's patron owes a debt recorded in the Register — buying it is the only way to erase it.
- [[Captain Rell]] offers 250 GP for proof the Register is forged.
- One PC recognises [[Sister Anneke]]'s handwriting on an anonymous letter seeking help.
- A PC's family name appears in a stolen ledger page they glimpsed last session.

**The Strong Start**

> [!quote] Read-Aloud
> The barge noses into the sea-cave under a ceiling of string lights, and the
> music from the ballroom above thuds through the hull like a heartbeat. A
> footman in a gull mask takes your invitation — then his eyes catch the sea
> behind you and widen. The tide is already over the lower landing.

**Immediate prompt:** as the barge bumps the dock, the footman drops the tray and
runs. Call for **Initiative**, or let the party **Search** (`DC 13 Wisdom
(Perception)`) to spot the flooded stair before the crush. The masquerade starts
now, whether they are ready or not.

## 2. Pacing Engine: Tension Pool & Scene Clocks

Every **10 minutes** of in-game searching, picking locks, arguing, or casting a
ritual adds **1d6** to the pool. Deliberate reckless noise (a dropped crate, a
shouted argument, a spell with a bang) **rolls the pool immediately**. At **6d6**,
roll and clear it. Every **1** rolled triggers the table below.

> [!danger] Tension Complication — roll 1d6
>
> | 1d6 | Complication | Immediate mechanical effect |
> | --- | --- | --- |
> | 1 | A gull-masked patrol enters the room. | **DC 14 Dexterity (Stealth)** to slip aside; failure means combat with 2 [[Lantern-Cutter\|Lantern-Cutters]]. |
> | 2 | The tide surges up the stairwell. | Floor becomes **difficult terrain**; tick **The Sea-Gate Floods** by 1. |
> | 3 | A lantern gutters and dies. | Area drops to **Darkness**; Passive Perception below 14 fails until relit (an action). |
> | 4 | A guest recognises a PC. | That NPC's Attitude **drops one step** (Friendly→Indifferent→Hostile); one broken Objection re-forms. |
> | 5 | Vesper's wards flare. | The cipher key scrambles: all **Study** DCs against the Register rise by 5 until re-synced (DC 15 Arcana). |
> | 6 | Brine-drowned servitors surface. | 3 [[Lantern-Cutter\|Lantern-Cutters]] climb from the cellar water; they act on Initiative 13. |

**Active Progress Clocks**

- **The Sea-Gate Floods `[0/6]`** — ticks +1 per Tension Pool trigger involving
  water, +1 per 30 minutes of in-game time, and +1 whenever a PC enters the
  cellar. At **6/6** the stairwell floods and the cellar route is lost.
- **Halvard's Purchase `[0/4]`** — ticks +1 per Gala Spine beat and +1 per Tension
  Pool trigger. At **4/4** the Register is sold and the syndicate wins.

## 3. Secrets & Clues (Three Clue Rule)

Each critical conclusion is reachable by at least three routes.

| # | Secret / Clue | Passive Threshold (Core Clue) | Active 2024 Check (Study / Search / Influence) | Possible Discovery Nodes |
| --- | --- | --- | --- | --- |
| 1 | The Register is a forged copy; the true ledger is aboard the auction barge. | Passive Insight 15+ on Halvard's nervous tic | **Study** (Intelligence/Investigation) **DC 16** on the ink; **Search** (Wisdom/Insight) **DC 15** on Halvard | Ballroom, Card Room, Barge |
| 2 | Two-colour page numbering betrays a switched signature page. | Passive Perception 14+ | **Study** (Intelligence/History) **DC 17** | Card Room, Library |
| 3 | [[Sister Anneke]] is alive in the cellar with a witness. | Passive Perception 16+ (distant knocking) | **Search** (Wisdom/Perception) **DC 18**; **Search** (Wisdom/Medicine) **DC 15** for the wound | Cellar Stair, Servants' Gallery |
| 4 | [[Doctor Orsino Bale]] has drugged the wine, but only the Host's decanter. | Passive Insight 14+ | **Study** (Intelligence/Nature) **DC 16**; **Search** (Wisdom/Perception) **DC 15** | Card Room, Banquet |
| 5 | The sea-gate key hangs openly on the Host's chatelaine. | Passive Perception 15+ | **Search** (Wisdom/Perception) **DC 14**; **Influence** (Charisma/Deception) **DC 17** to borrow it | Ballroom, Harbourmaster's Door |


## 4. Social & Political Encounter Prep

| [[NPC Name]] & Role | Appearance, Mannerism & Voice | Starting Attitude & Base Influence DC | Willingness State | Core Goal |
| --- | --- | --- | --- | --- |
| [[Lord Halvard]] — the mark | Tall, sun-burned, gloves always on. Sniffs before he speaks, over-precise cadence. | **Indifferent → DC 15** | Hesitant | Buy the Register to bury a debt in his own name. |
| [[Tidewright Vesper]] — syndicate broker | Sharp-shouldered, salt-stiff coat, ink-stained cuffs. Answers questions with questions. | **Hostile → DC 20** | Unwilling | Sell the Register and leave before the tide. |

### [[Lord Halvard]] — Social Hit Points

**Attitude:** Indifferent → **Base DC 15** · **Willingness:** Hesitant
**Core Goal:** Own the Register so his daughter's debt silently disappears.

| # | Objection (what he says) | What actually breaks it | Check & DC |
| --- | --- | --- | --- |
| 1 | "The ledger is genuine — I have a notary's word." | Show the two-colour page numbering (Clue #2). | **Study** (Intelligence/Investigation) **DC 16** to authenticate. |
| 2 | "I will not be seen speaking with river-thieves." | A private room (the Card Room) or a covered exit. | **Influence** (Charisma/Deception) **DC 15** to cover them. |
| 3 | "Even so the price is fixed; I cannot move." | Proof Vesper is selling a forgery (Clue #1). | **Influence** (Charisma/Persuasion) **DC 15**. |

| # | Leverage (Ideal / Bond / Flaw / Secret) | Mechanical benefit |
| --- | --- | --- |
| 1 | **Bond** — his daughter's name is in the Register's debt column. | **Advantage** on the Influence check. |
| 2 | **Flaw** — terrified of scandal above all else. | Shifts Willingness: **Hesitant → Willing**. |

**Fail-Forward:** on a failed Influence check he buys the Register anyway, then
demands a favour to stay silent. Tick **Halvard's Purchase** by 1.


### [[Tidewright Vesper]] — Social Hit Points

**Attitude:** Hostile → **Base DC 20** · **Willingness:** Unwilling
**Core Goal:** Sell the Register, settle her debts, and be gone before the bell.

| # | Objection (what she says) | What actually breaks it | Check & DC |
| --- | --- | --- | --- |
| 1 | "You have nothing I want." | Produce the cipher key recovered from the barge (Clue #1). | **Study** (Intelligence/Arcana) **DC 17** to read it aloud. |
| 2 | "I do not bargain with people who owe me." | Expose Halvard's forgery, proving her sale is already spoiled. | **Influence** (Charisma/Intimidation) **DC 16**, backed by proof. |
| 3 | "The tide is my clock, not yours." | Threaten the sea-gate key on the Host's chatelaine (Clue #5). | **Search** (Wisdom/Perception) **DC 14**, then **Influence** (Charisma/Persuasion) **DC 15**. |

| # | Leverage (Ideal / Bond / Flaw / Secret) | Mechanical benefit |
| --- | --- | --- |
| 1 | **Secret** — the Register implicates her own patron, not just the party. | **−5** to the Influence DC. |
| 2 | **Flaw** — she cannot swim and fears open water above all else. | Shifts Willingness: **Unwilling → Hesitant**. |

**Fail-Forward:** on a failed check she whistles once; three [[Lantern-Cutter\|Lantern-Cutters]]
surface from the cellar and the barge begins to cast off. Tick **The Sea-Gate
Floods** by 2 — the party keeps their lead but loses the easy route.


## 5. The 5-Node Adventure Flow

Route: **1** Barge Dock → **2** [[The Card Room]] → **3** Servants' Gallery →
**4** [[The Cellar Landing]] → **5** [[The Sea-Gate]].
**Non-linear loop:** the Servants' Gallery (3) connects directly up to the Card
Room (2) and down to the Cellar Landing (4), so a party can skip the ballroom
entirely — at the cost of leaving Clues #1 and #4 undiscovered.

### Node 2 — [[The Card Room]] (Roleplay / Puzzle)

> [!quote] Read-Aloud
> Green baize, brandy, and the soft click of a faro deck. Every head in the room
> turns a fraction as you enter, then turns back — except one man in gloves, who
> keeps losing on purpose and watching the door.

- **Lighting & terrain:** **Dim light** (candles). Congested tables are
  **difficult terrain**; a **Search** (`DC 12 Wisdom (Perception)`) reveals the
  two-seat alcove behind the screen.
- **Cover & hazard:** an overturned brandy lamp; any creature that enters its
  square makes a **DC 13 Dexterity save**, taking **11 (2d10) fire** on a failure,
  or half on a success.
- **Sensory:** pipe smoke and spilled brandy; the quartet muffled through the floor.
- **Interactive Treat — the Marked Faro Deck (Utilize):** the deck is rigged.
  **Utilize** it with a **DC 15 Dexterity (Sleight of Hand)** check to palm the
  marked ace onto Halvard's side — the next **Influence** check against him gains
  **Advantage**. Reading the deck instead is a **Study** (Intelligence/History)
  **DC 17**, which reveals **Clue #2**.
- **Three solution paths:** (a) **Study** (Intelligence/Investigation) **DC 16**
  on the notary's seal → **Clue #1**; (b) **Influence** (Charisma/Performance)
  **DC 15** to run the table and draw Halvard aside; (c) **Search** (Wisdom/Insight)
  **DC 15** to read Halvard's tic — or Passive Insight 15+ for free.
- **Transitions & clues:** ↔ Ballroom (1) and Servants' Gallery (3). Carries
  **Clues #1, #2, #4**.

### Node 4 — [[The Cellar Landing]] (Climax / Combat)

> [!quote] Read-Aloud
> The stair ends in black water that is deeper than it was ten minutes ago. On
> the flooded landing, a woman in a nun's grey is hammering on a sea-gate chain —
> and behind you, the stairs fill with lantern-light and wet footsteps.

- **Lighting & terrain:** **Darkness** below the waterline; flooded steps are
  **difficult terrain** for all but the [[Lantern-Cutter\|Lantern-Cutters]].
- **Cover & hazard:** a rusted cargo winch groans overhead. Triggering it forces
  a **DC 14 Dexterity save** or **22 (4d10) bludgeoning damage** and the **Prone**
  condition in a 10-ft. cone.
- **Sensory:** brine and old rope; the sea-gate chain grinding; light on water.
- **Interactive Treat — the Rusted Winch (Utilize):** cut the cable with
  **Utilize** (**DC 15 Dexterity**) to drop the load on the landing, dealing the
  hazard above to **every** creature in the cone — and exposing the sea-gate chain
  for **Clue #5**.
- **3-T Combat:**
  - **Threat:** [[Sable Cray]] (boss) plus **2** [[Lantern-Cutter\|Lantern-Cutters]].
  - **Timer (1d4 rounds):** on round 3 the surge makes the steps difficult terrain;
    on round 4 the **sea-gate** begins to close (tick **The Sea-Gate Floods** +1
    each round thereafter).
  - **Treat:** the winch.
- **The Monsters Know:** the cutters flank and use **Nimble Escape** to hold the
  stairs; Cray opens with **Harpoon** to drag the healer into the water, targets
  the **lowest-AC** creature, and triggers **Bloodied Last Stand** at **68 HP**.
  At **Bloodied** the cutters flee upstairs; Cray fights to the death only while
  the sea-gate remains open.
- **Transitions & clues:** ↔ Cellar Stair (3) and [[The Sea-Gate]] (5). Carries
  **Clues #3 and #5**.

> [!tip] Loot & Rewards
> In the strongbox on the landing: **250 GP** in harbour scrip, a **Potion of
> Healing (2d4 + 2)**, the forged [[Harbour Register]], and the **sea-gate key**
> (opens the cellar route permanently).


## 6. Custom 2024 Fantasy Statblocks

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
actions:
  - name: Scimitar
    desc: "Melee Attack Roll: +5, reach 5 ft. Hit: 6 (1d6 + 3) Slashing damage, and the cutter has Advantage on its next attack roll against the target before the end of its next turn (Vex)."
  - name: Hand Crossbow
    desc: "Ranged Attack Roll: +5, range 30/120 ft. Hit: 6 (1d6 + 3) Piercing damage."
  - name: Two-Blade Flurry (Recharge 5-6)
    desc: "The cutter makes two Scimitar attacks against one creature or two creatures within 5 ft. of it."
bonus_actions:
  - name: Nimble Escape
    desc: "The cutter takes the Disengage or Hide action."
reactions:
  - name: Slip the Noose
    desc: "Trigger: A creature the cutter can see moves within 5 ft. of it. Response: The cutter moves up to 10 ft. without provoking Opportunity Attacks."
```

```statblock
name: Sable Cray
size: Medium
type: Humanoid
alignment: Lawful Evil
ac: 16 (Chain Mail)
hp: 136
hit_dice: 16d8 + 64
speed: 30 ft., swim 30 ft.
stats: [18, 14, 18, 10, 13, 12]
saves:
  - str: 7
  - con: 7
skillsaves:
  - athletics: 7
  - intimidation: 5
  - perception: 4
damage_resistances: poison
damage_immunities: ""
condition_immunities: ""
senses: Passive Perception 14, Initiative +5 (15)
languages: Common, Aquan, Thieves' Cant
cr: 5
traits:
  - name: Saltblooded
    desc: "Cray adds her Proficiency Bonus to Initiative rolls and has Advantage on saving throws against the Frightened and Poisoned conditions."
  - name: Amphibious
    desc: "Cray can breathe air and water."
actions:
  - name: Multiattack
    desc: "Cray makes two Cutlass attacks and one Harpoon attack."
  - name: Cutlass
    desc: "Melee Attack Roll: +7, reach 5 ft. Hit: 13 (2d8 + 4) Slashing damage, and the target has Disadvantage on its next attack roll before the end of Cray's next turn (Sap)."
  - name: Harpoon
    desc: "Ranged Attack Roll: +7, range 30/90 ft. Hit: 9 (1d10 + 4) Piercing damage, and the target must succeed on a DC 15 Strength saving throw or be pulled up to 20 ft. toward Cray."
  - name: Brine Slam (Recharge 5-6)
    desc: "Each creature within 15 ft. of Cray makes a DC 15 Constitution saving throw, taking 21 (6d6) Cold damage and having the Prone condition on a failure, or half as much damage only on a success."
bonus_actions:
  - name: Boarding Rush
    desc: "Cray moves up to her Speed toward a creature she can see. If she ends this move within 5 ft. of that creature, she can shove it (DC 15 Strength saving throw or Prone)."
reactions:
  - name: Riposte
    desc: "Trigger: A creature within 5 ft. of Cray hits her with a melee attack. Response: Cray makes one Cutlass attack against that creature."
  - name: Bloodied Last Stand
    desc: "Trigger: Cray becomes Bloodied (68 HP or fewer). Response: She gains 20 Temporary Hit Points and recharges Brine Slam."
```
````

