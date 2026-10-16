# Campaign Continuity Module

Load this file **only in Campaign Mode** (multi-session play). It gives the
world a life of its own between sessions so the campaign advances even when the
party rests, argues, or chases a side quest.

> **Do not load for one-shots.** If the session is contained, ignore this file
> entirely — the 3-Faction Triangle and Grim Portents need runway to pay off.

## 1. The 3-Faction Triangle Engine

Three factions, each opposed to the other two, so **every alliance carries a
cost**. If the party helps A, they automatically anger B and C — there is no
clean win, only a choice of enemies.

```
        [Faction A]
         /        \
   opposes          opposes
       /              \
[Faction C] ——— opposes ——→ [Faction B]
```

### Faction dossier template

Give each faction three **Goals** and three **Assets**. Rate every Asset from
**+1 (fledgling)** to **+4 (dominant)** — this is the faction's dice modifier on
its turn.

```markdown
### [[Faction Name]]
**Archetype:** [e.g. harbour syndicate / crown church / mercantile guild]
**Public Face:** [what the city believes they are]
**True Goal:** [what they actually want this arc]

**Goals (in priority order):**
1. [immediate goal — this session's shadow]
2. [medium goal — next 3 sessions]
3. [long goal — the arc's endgame]

**Assets (rate each +1 to +4):**
| Asset | Rating | What it does on a Turn |
| --- | --- | --- |
| [[Asset A: e.g. dock crews]] | +3 | Control of a physical chokepoint |
| [[Asset B: e.g. the Cardinal's ear]] | +2 | Political cover / legal immunity |
| [[Asset C: e.g. blackmail ledger]] | +1 | Leverage over one rival NPC |
```

### Between-Session Faction Turn Procedure

Run this **once per downtime block** between sessions. It takes two minutes and
generates next session's world shifts.

1. **Declare the match.** Choose a faction that acts, and the rival it targets
   (follow the triangle: A→B, B→C, or C→A). The third faction sits out and
   **gains +1 to one Asset** for its patience.
2. **Roll the contest.** Each side rolls **`1d10 + the relevant Asset rating`**.
   The attacking faction chooses which of its Assets it is leveraging.
3. **Resolve:**
   - **Attacker wins by 1–4:** the target loses **1 point** from the Asset it
     defended (minimum +1). Small, grinding pressure.
   - **Attacker wins by 5+:** the attacker **seizes** the contested Asset — the
     target's rating drops to +1 and the attacker's rises by 1. A real reversal.
   - **Tie:** a **stalemate**. Both sides entrench; the next Turn against this
     pairing is at **−2** to the attacker.
   - **Defender wins:** the attacker's chosen Asset drops by 1 and the defender
     gains Advantage on its own next Turn against the winner.
4. **Translate the result into the world.** Write exactly **3 tavern rumours**
   for the next session. Each rumour must be traceable to the roll so the world
   feels causal, not random:

```markdown
> [!tip] Tavern Rumours (from last session's Faction Turn)
> 1. "Did you hear the dock crews walked off three berths this week? Somebody
>    bought their silence." → *Result: Faction A seized the dock-crew Asset.*
> 2. "The Cardinal's man was seen burning a ledger behind the cathedral." →
>    *Result: Faction B defended its Assets at a cost.*
> 3. "A new tax on salt — the guild calls it a 'tide levy.'" → *Result: Faction C
>    banked its patience bonus and is moving.*
```

### Keeping It Fair

- The party is **never** a faction here; they are the weather between them. Their
  actions change which **Assets** exist, not the dice.
- Factions should act on their own **Goals**, not the DM's plot: a faction wins
  by advancing its goal #1, which always makes tonight's session harder in a new
  way.
- Log every Turn. By session five, the ratings tell a story about who is winning
  the city.

## 2. Grim Portents & Campaign Fronts

A **Front** is a threat on a schedule. It does not wait for the party. Each Front
has **4 sequential Grim Portents** — escalating facts about the world — and an
**Impending Doom** at the end. When the last Portent lands, the Doom happens.

```markdown
> [!danger] Campaign Front: [Name]
> **Threat:** [who or what, in one line]
> **Impending Doom:** [the irreversible thing that happens at Portent 4]
>
> **1. [Portent name — a whisper]** — [a sign nobody heeds yet; costs nothing]
> **2. [Portent name — a wound]** — [a named NPC, place, or route is harmed]
> **3. [Portent name — a siren]** — [the threat acts openly; a clock appears]
> **4. [Portent name — the storm]** — [the Doom arrives; the map changes]

**Tick rule:** advance one Portent each time the party takes **two or more Long
Rests** without addressing the Front, **or** explicitly ignores a hook tied to it.
```

### How to advance a Front without punishing the party

- A Portent is a **fact**, not a cutscene. "The salt-marsh drowned its chapel" is
  a Portent; "the villain gives a monologue" is not.
- Announce each tick through **3 channels**: a rumour on the road, a physical sign
  the party passes, and a mechanical change (a route closed, a price doubled, an
  NPC's Attitude dropped one step).
- Let the party **interrupt** a Portent by acting. Clearing a Front early simply
  retires it and converts its remaining Portents into rewards for the next arc.
- Run **no more than two Fronts** at once. Three competing clocks overwhelm the
  table; two create genuine tension.

### Sample Front (reusable skeleton)

```markdown
> [!danger] Campaign Front: The Drowned Debt
> **Threat:** The harbour's patron tithe-cults are calling up something beneath the bay.
> **Impending Doom:** The sea-gate floods permanently and the lower city is lost to salt water.
>
> **1. Watermarks Creep** — cellar floors below the Bluffs are damp; dockhands joke about it.
> **2. The Chapel Sinks** — the salt-marsh chapel and its [[Sister Anneke]] are gone; a witness flees inland.
> **3. The Tide Bell Rings at Dawn** — an unnatural high tide floods the fishmarket; *Sea-Gate Surge [0/4]* clock appears.
> **4. The Warden Wakes** — [[The Salt Warden]] rises; the sea-gate cannot be closed and the lower docks are submerged.
```


## 3. 2024 Bastion & Downtime Integration (Levels 5+)

In the 2024 rules a Bastion is a player-owned stronghold that runs **Bastion
Turns** during downtime. Tying session rewards into Bastions gives the party a
reason to care about the world between sessions. *(Consult the 2024 Dungeon
Master's Guide for the full facility and order rules; use the lookup below to
slot session outcomes into it.)*

### 3a. Bastion Turn quick lookup

- A **Bastion Turn** happens each **7 days** of in-game downtime. The owner issues
  one order to each **special facility** they control.
- Orders: **Craft, Empower, Harvest, Maintain, Recruit, Research, Trade** (some
  facilities only accept specific orders).
- Facilities cost **Bastion Points (BP)** to build or upgrade. Basic facilities
  are free; special facilities unlock special capabilities.
- **Bastion Defenders** guard the site. If the Bastion is attacked, defenders
  fight; the number of defenders and the outcome come from the DMG's Bastion
  Events.

### 3b. Wiring session rewards into the Bastion

```markdown
| Session Reward | Bastion Effect | Narrative Hook |
| --- | --- | --- |
| Rescued a named NPC | **Recruit** that NPC as a **Hireling** for one facility | They remember the debt and may become a Front target |
| Cleared a monster lair | Unlock a **special facility** (e.g. [[Trophy Room]], [[Menagerie]]) | Requires **BP** and a builder |
| Won a council vote | A faction issues a standing **Trade** order; +GP per Turn | The losing faction becomes a Front |
| Recovered blueprints | Upgrade a facility one tier | Starts a 7-day build during the next downtime |
| Freed captured guards | +2 **Bastion Defenders** | A rival probes the defenses next Turn |
| Secured a trade route | One **Trade** order yields double GP | Routes can be cut by a Front Portent |
```

### 3c. Downtime activities between sessions

Offer each player **one** of the following per downtime block, in addition to
Bastion orders, so downtime produces session hooks rather than bookkeeping:

- **Research** a Front's Portent to reveal the next tick early.
- **Recruit** a follower, contact, or faction ally (costs GP and time).
- **Craft** a 2024 magic item from a recovered formula (needs the facility and BP).
- **Train** to learn a language, tool, or weapon mastery.
- **Carouse** to gather the next session's 3 tavern rumours directly.

### 3d. Faction Orders during a Bastion Turn

Let a faction the party has allied with place **one order** in the party's Bastion
each Turn. This is flavour *and* mechanics: the faction gains a facility's output
and, in exchange, becomes a named asset the party can call on — and a liability
when a rival Front targets it.

## 4. Spiral Campaign Seeds

Plant **3 hooks** in tonight's session that point outward to the next ring of the
map, so the campaign grows a spiral rather than a straight line. Each seed must
be **ignorable now** and **unmistakable later**.

```markdown
| # | Seed (planted in tonight's session) | Where it points (next ring) | Trigger to sprout |
| --- | --- | --- | --- |
| 1 | A [foreign coin / sigil / accent] in a loot parcel | A neighbouring [region / plane / city-state] | When the party next visits a port or guild |
| 2 | A [map fragment / letter] naming an unknown place | A deeper dungeon or wild frontier | On the next Bastion Research order |
| 3 | A [survivor / prisoner] who flees outward | A faction HQ or patron's rival | When a Front ticks to Portent 3 |
```

### Spiral design rules

- **One ring at a time.** Seeds should reference the *immediate* next region, not
  the endgame. Mystery is a ladder, not a chasm.
- **Make seeds physical.** An object the party can hold, a name they can say, a
  person they can chase. Abstract foreshadowing is forgotten by next session.
- **Reward attention without requiring it.** If they chase a seed early, seed #1
  becomes a session; if they ignore it, it becomes a Front Portent instead.
- **Retire a Spiral after two sessions** if untouched. Unresolved seeds rot into
  noise; convert them into a Front or drop them.

