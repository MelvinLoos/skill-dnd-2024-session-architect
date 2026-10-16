# Social, Gala & Council Modules

Everything needed to run talky, high-stakes D&D 5e (2024) scenes: the 2024 Social
Action Matrix, the Social Hit Points template, **Module A (Alexandrian Gala)**,
and **Module B (3-Vote Council)**.

> **2024 vocabulary reminder.** The relevant actions are **Influence**,
> **Study**, **Search**, **Utilize**, and **Help**. Reading a creature's motive is
> a **Search** action using Wisdom (**Insight**), not a standalone action.

## 1. The 2024 Social Action Matrix

### 1a. The Influence Action

**Influence** urges a creature to do something. The player describes *how* they
communicate (deceive, intimidate, amuse, persuade). That establishes the
creature's **Willingness**, which decides whether any roll happens at all:

| Willingness | When it applies | Roll required? |
| --- | --- | --- |
| **Willing** | The request aligns with what the creature already wants. | **No roll.** It complies in the manner it prefers. |
| **Hesitant** | The request is plausible but costly, risky, or against habit. | **Yes — Influence check** against the Attitude DC. |
| **Unwilling** | The request is repugnant, suicidal, or against alignment. | **Impossible** until Leverage shifts the state to Hesitant. |

When a roll is required, set the DC from the creature's **Starting Attitude**,
then apply a single clean modifier:

| Starting Attitude | Base DC | Then adjust for… |
| --- | --- | --- |
| **Friendly** | **10** | −5 if the request is trivial; +5 if it risks the creature's Bond. |
| **Indifferent** | **15** | −5 for a credible Leverage Point; +5 if the creature is watched. |
| **Hostile** | **20** | −5 for proof that changes the creature's mind about the PCs. |

**Check selection.** The player picks the skill that matches their approach, all
Charisma-based in 2024:

- **Deception** — sustaining a lie, forging intent, playing a role.
- **Intimidation** — coercing via threat. A threat you cannot back up raises the DC by 5.
- **Persuasion** — honest appeal, flattery, principled argument.
- **Performance** — working a room, holding a crowd, playing a part.

**Passive Influence.** Do not roll for trivial asks; compare against a passive
read of the creature (`10 + Persuasion/Insight relevant modifier`) and narrate
the reaction. Roll only when the outcome is contested and costly.

### 1b. The Study & Search Actions in Intrigue

**Study** (Intelligence) dredges memory, documents, and evidence. **Search**
(Wisdom) finds what is hidden, including what a face is hiding.

| Player goal | Action | Ability & skill | Typical DC |
| --- | --- | --- | --- |
| Read an NPC's true motive or fear | **Search** | Wisdom (**Insight**) | 12–18 vs. their Deception |
| Confirm a document is forged | **Study** | Intelligence (**Investigation**) | 15–20 |
| Recall a faction's heraldry or oath | **Study** | Intelligence (**History**) | 10–15 |
| Identify a poison, drug, or elixir | **Study** | Intelligence (**Nature**) | 12–17 |
| Decode a cipher, sigil, or ritual | **Study** | Intelligence (**Arcana**) | 15–20 |
| Reconcile a ledger against reality | **Study** | Intelligence (**Investigation**) | 16–22 |
| Spot a concealed weapon or trap | **Search** | Wisdom (**Perception**) | 14–20 |
| Determine if a wound is self-inflicted | **Search** | Wisdom (**Medicine**) | 13–18 |

**The three-beat read.** When a PC studies an NPC, reveal in order: (1) the
**Objection** they are defending, (2) the **Leverage** that would move them, and
(3) the **thing they are afraid you already know**. Never gate all three behind
one roll — one check reveals one beat, so the table must keep probing.

## 2. The "Social Hit Points" Template (3 Objections & Leverage)

Every Key NPC gets this block. The **3 Objections** are the NPC's social shields:
until each is broken, the Influence check cannot plausibly succeed. **Leverage**
is the crowbar. Copy the fenced template below and fill in concrete specifics —
never write "the NPC is suspicious," write *why* and *at what DC*.

```markdown
### [[NPC Name]] — Social Hit Points

**Attitude:** Friendly / Indifferent / Hostile  → **Base Influence DC:** 10 / 15 / 20
**Willingness:** Willing / Hesitant / Unwilling
**Core Goal:** [one sentence — what they want tonight]

#### The 3 Objections (Social Shields)

| # | Objection (what they say) | What actually breaks it | Check & DC |
| --- | --- | --- | --- |
| 1 | "[in-character refusal]" | [proof / argument / action] | DC __ Wisdom (Insight) to read it, then Charisma (Persuasion/Deception) |
| 2 | "[in-character refusal]" | [proof / argument / action] | DC __ Intelligence (Investigation/History) |
| 3 | "[in-character refusal]" | [proof / argument / action] | DC __ Charisma (Intimidation/Performance) |

#### Leverage Points (Vulnerabilities)

| # | Leverage (Ideal / Bond / Flaw / Secret) | Mechanical benefit |
| --- | --- | --- |
| 1 | [the secret or bond] | Advantage on the Influence check **or** −5 to the DC |
| 2 | [the flaw or debt] | Shifts Willingness: **Unwilling → Hesitant** (or **Hesitant → Willing**) |

#### Fail-Forward Consequence

On a failed Influence check, the scene does **not** dead-end. Apply one:
[**+] cost** (they help only for a named price), [**⏱] tick a Progress Clock**
(name which), or [**↻] a favour owed** to be collected later.
```

### Objection design rules

- An Objection must be **answerable by play, not by a single die roll**. It names
  a thing the party can *do* — produce the ledger, bring a witness, disarm the
  guard — and only then asks for a check.
- Break an Objection **permanently** when the party does the thing. Do not make
  them re-roll it. Social progress should feel like progress.
- Three Objections, no more. More than three stalls the table; fewer than three
  makes the NPC a vending machine.

### Leverage design rules

- Leverage is **discovered**, not assumed: a **Search** (Wisdom/Insight) to read
  it, or a **Study** (Intelligence/History or Investigation) to dig it up.
- Award exactly one clean mechanical benefit per Leverage: **Advantage** *or*
  **−5 DC** *or* a one-step **Willingness shift** — never all three.
- Retreat on a failed roll is banned. Fail forward: shift cost, tick a clock, or
  bank a favour. The story always moves.

### Worked micro-example

> [!warning] DM Secret & Leverage
> `[[Salt Warden]]`'s Objection 2 ("I do not trust land-dwellers with a
> tide-chart") breaks the moment a PC returns the stolen chart; no roll. Its
> Leverage 2 (Flaw: *terrified of deep water*) shifts it from **Unwilling →
> Hesitant**, then a `DC 15 Charisma (Persuasion)` check opens the sea-gate. A
> failure costs the party their fastest route and ticks *City Watch Lockdown* by 1.


## 3. Module A — Alexandrian Gala / High-Society Party Mode

Enable when the session involves a ball, feast, festival, diplomatic summit, or
tavern night. A gala is **not** a single scene; it is four overlapping zones, six
moving VIPs, a rumour economy, and a clock. The party cannot cover it all, so the
cost of every choice is real.

### 3a. The 4 Party Zones (sensory vibe + passive mechanical perk)

Each zone gives a **passive perk** so where the party stands matters
mechanically. Copy and fill:

```markdown
| Zone | Sensory Vibe (light, sound, smell) | Passive Mechanical Perk |
| --- | --- | --- |
| [[Grand Ballroom]] | [candlelight, string quartet, beeswax + wine] | Advantage on Charisma (Performance) while dancing; every 10 min here ticks the *Gala Spine* clock. |
| [[Smoking Balcony]] | [cold sea air, pipe smoke, muted music] | Advantage on Wisdom (Insight) — relative quiet makes lies easier to read. |
| [[Card Room]] | [green baize, brandy, low laughter] | Advantage on Intelligence (Investigation) to notice marked cards or forged notes; gambling can win 25–250 GP. |
| [[Servants' Gallery]] | [steam, brass, clatter, gossip] | Advantage on Wisdom (Perception) to overhear; servants know every secret worth 1 Objection. |
```

### 3b. The 6 VIP Guests

| [[NPC]] | Current Zone | Who They Seek | Who They Avoid | Secret Agenda |
| --- | --- | --- | --- | --- |
| [[Lady Marcelle Vane]] | Grand Ballroom | The party's patron | [[Tidewright Vesper]] | Wants the Ledger destroyed before dawn. |
| [[Tidewright Vesper]] | Card Room | Anyone holding ciphers | [[Lady Marcelle Vane]] | Buying silence from the harbour crews. |
| [[Captain Rell]] | Smoking Balcony | A patron with coin | [[Lady Marcelle Vane]] | Recruiting for a mutiny. |
| [[Sister Anneke]] | Servants' Gallery | The wounded | Anyone in authority | Smuggling a witness out of the city. |
| [[Doctor Orsino Bale]] | Card Room | Debtors | [[Captain Rell]] | Poisoning the evening's wine—selectively. |
| [[Lord Halvard]] | Grand Ballroom | A marriage alliance | [[Sister Anneke]] | His "dead" brother is in the sea-cave. |

### 3c. The 5 Floating Gossip Topics

Any NPC can raise these when conversation stalls. Each routes to a numbered
Secret/Clue from the session's Secrets & Clues table:

1. "Did you hear the harbour ledger's pages are numbered in two colours?" → Clue #2
2. "They say a Warden walks the caves at low tide and counts ships." → Clue #5
3. "The Cardinal's ring went missing the same night the tide-charts were copied." → Clue #7
4. "There is a room upstairs nobody is allowed to sweep." → Clue #3
5. "Someone paid the string quartet double to play the mournful suite." → Clue #9

### 3d. The 5-Beat Event Spine

Time-boxed disruptions fire **regardless of what the party does**, forcing state
changes and cutting conversations short:

```markdown
- **[00:00] Opening Toast.** Host greets the crowd; every VIP shifts one Zone.
- **[00:30] The Missing Ring.** A theft is announced; all Search checks gain +2 DC, and [[Captain Rell]] moves to the Balcony exits.
- **[01:00] Quartet Turns Mournful.** The library is left unguarded for 10 minutes — a free window for a Study run.
- **[01:30] Wine Is Served.** [[Doctor Orsino Bale]]'s poison resolves; one VIP takes the Poisoned condition. Escalate.
- **[02:00] The Tide Bell.** Announcement: the sea-gate closes in 15 minutes. All Progress Clocks advance 1.
```

**Running the Spine.** Announce each beat with a change in *sound and light*,
never a flat "30 minutes pass." The gala should feel like weather rolling in.


## 4. Module B — The 3-Vote Council / Parley Tracker

Enable when the party must sway a tribunal, guild council, or noble assembly.
A council is a **turn-based combat scene where the "damage" is votes**. Run it
with the same rigor as initiative.

### 4a. Structure & Round Limit

- The council runs for **4–6 Social Rounds**. Announce the limit up front and
  count it down aloud — the gavel falling is the doom clock.
- **Each PC takes exactly one action per round:** **Study**, **Search**,
  **Utilize**, or **Influence**. They may not double up on the same voter's
  Objection in one round.
- **The Hardliner takes a counter-action every round.** At the end of each round,
  they either raise one voter's DC by 5, erase one broken Objection, or introduce
  a new Objection against a random swing voter.
- **Winning** = 3 of 5 votes. **Losing** is not the end: the motion fails *and*
  the Hardliner's favoured rider passes instead (name its consequence).

### 4b. The 5-Voter Breakdown Template

```markdown
### Council: [Name of Body] — Motion: [exact wording]

**Rounds:** [0/5]  **Votes secured:** 0  **Gavel falls at round 5.**

| Voter | Role | Starting Stance | The Pillar That Sways Them | Voted? |
| --- | --- | --- | --- | --- |
| [[Ally]] | Ally | For the party | Already on side; offers Advantage on one Study check per round (Help). | [ ] |
| [[Hardliner]] | Hardliner | Opposed (no DC will move them) | Cannot be swayed — only *silenced* (Utilize an exposed crime) for 1 round. | [ ] |
| [[Voter A]] | Swing | Indifferent | **Security Guarantee:** prove the party will protect their interests in combat. | [ ] |
| [[Voter B]] | Swing | Indifferent | **Leverage & Evidence:** bring blackmail or stolen proof (Stealth/Search chain). | [ ] |
| [[Voter C]] | Swing | Hostile | **Logic & Oratory:** a DC 18 Charisma (Persuasion) argument built on a Study result. | [ ] |
```

### 4c. The Three Pillars (assign one per swing voter)

| Pillar | What the voter wants to see | Actions & checks that satisfy it |
| --- | --- | --- |
| **Combat / Security** | A credible promise of protection or force. | Demonstrate capability: a martial display, an escort guarantee, or **Utilize** a captive threat as proof. Influence (Intimidation) at +5 DC if unbacked. |
| **Stealth / Blackmail** | Something the voter can use in private. | A **Search** (Wisdom/Perception) to find the document, then **Study** (Intelligence/Investigation) to authenticate it. Delivering it is a free Willingness shift. |
| **Logic / Diplomacy** | An argument that survives scrutiny. | A **Study** (Intelligence/History or Arcana) beat to build the premise, then **Influence** (Persuasion) to land it. Cross-check the party's earlier clues. |

### 4d. Running the Council (DM script)

1. **Open** with the Hardliner stating the motion against the party; read the
   exact wording so the stakes are unambiguous.
2. **Round loop:** each PC acts → resolve → the Hardliner counters → tick the
   round counter.
3. **Every 2 rounds**, a floating Gossip Topic or a Tension Pool result should
   enter the chamber (a shouted interruption, a delivered letter) so the scene
   never becomes a static debate.
4. **Close** by reading the tally aloud. Success earns the boon *and* a named
   enemy; failure passes the Hardliner's rider and sets up the next session.

> [!danger] Council Complication
> If the party is still one vote short at the start of round 5, the Hardliner
> calls for an **immediate vote by acclamation**. The party gets exactly one
> final Influence attempt at **+5 DC** — win it and the chamber erupts into
> argument worth a one-round extension; fail it and the motion dies.

