# How to Play — Five Legends of Riftbound

A standalone, play-focused guide to five **Riftbound** legends — **Diana**, **Vi**,
**Azir**, **Lillia**, and **Leona**. Each entry is a complete "how to pilot this deck"
walkthrough: the game plan, the win condition, the power curve, the key cards, and
**two decision trees** — one for *your* turn (offense) and one for the *opponent's*
turn (defense) — that separate the correct line from the greedy-instinct trap.

## Contents

1. [Rules primer](#rules-primer-what-the-trees-assume) — the shared vocabulary every tree assumes
2. [How to read the decision trees](#how-to-read-the-decision-trees)
3. **Diana — Scorn of the Moon** *(Mind / Chaos — reactive spell-control / tempo)* → [jump](#diana--scorn-of-the-moon)
4. **Vi — Piltover Enforcer** *(Fury / Order — proactive beatdown / tempo-midrange)* → [jump](#vi--piltover-enforcer)
5. **Azir — Emperor of the Sands** *(Calm / Order — Equipment-gated Sand Soldier swarm)* → [jump](#azir--emperor-of-the-sands)
6. **Lillia — Bashful Bloom** *(Calm / Mind — [Temporary] Sprite tempo)* → [jump](#lillia--bashful-bloom)
7. **Leona — Radiant Dawn** *(Calm / Order — stun-control midrange / buff accrual)* → [jump](#leona--radiant-dawn)
8. [Web Resources & Sources](#web-resources--sources)

---

## How to read the decision trees

```mermaid
flowchart LR
    Q{"A read / decision<br/>(what to check)"}:::q
    G["The correct line"]:::good
    R["The greedy-instinct trap"]:::trap
    Q --> G
    Q -.->|"greedy instinct"| R
    classDef q fill:#e8f0fe,stroke:#1a73e8,stroke-width:2px,color:#12325f;
    classDef good fill:#e6f4ea,stroke:#188038,stroke-width:2px,color:#0d3b1e;
    classDef trap fill:#fdecea,stroke:#d93025,stroke-width:2px,color:#5f1a15;
```

Blue = a read to make · Green = the correct line · Red (dashed) = the greedy trap.
Every legend below has **two** trees — one for your turn (offense), one for the
opponent's turn (defense) — because you make decisions on both.

> Riftbound units are written **Might + optional Power**, not "X/X". A "2-Might body"
> has 2 Might and no printed Power pip.

---

## Diana — Scorn of the Moon
*(Mind / Chaos — reactive spell-control / tempo)*

**Game plan.** Diana's legend — *"[Reaction] Exhaust: Add 1 Energy, spend only during
showdowns; this add can't be reacted to"* — is a resource nobody else has: interaction
invisible to the opponent's rune count and usable exactly when units are fighting over a
battlefield. So she plays a **tempo-control** game: contest early with cheap 2-Might
bodies (Ravenbloom Student, Tideturner), then win **the one showdown that matters** by
chaining cheap [Reaction] tricks part-funded by the showdown Energy — converting a
favourable fight into a Conquer, then Holding it to 8. Spell density does double duty:
every spell pumps **Ravenbloom Student +1 Might this turn**, so the "answers" are also
the clock.

**Win condition.** Bank a point on a contested showdown (shrink their attacker, bounce
their blocker, or pull-and-shrink defenders with Moonfall so your unit survives and
theirs doesn't), then **Hold** that battlefield toward 8. Vex - Apathetic locks a held
battlefield by stunning whatever the opponent plays there.

**Power curve.** Weakest turns 1–2 and vs. fast aggression (small bodies, and the Energy
only exists *inside* showdowns). Strongest mid-game (~T3–5) once Hwei is moving for
cards, Fizz is recurring spells, and Students are online. Favoured in the grind.

| Card | What it does |
|---|---|
| **Diana - Scorn of the Moon** (Legend) | Exhaust → **+1 Energy usable only in showdowns**, and the add **can't be reacted to**. Lets you cast one more trick than your visible runes imply — the bluff the deck is built around. |
| **Moonfall** (spell, 3 Energy + 1 Power) | Choose a battlefield where you have units; pull up to one enemy unit there; then **all** enemy units there get **−2 Might this turn**. Self-targets (no target prompt). |
| **Hwei - Brooding Painter** (Might 5) | *When I move:* draw 1, discard 1, then a bonus by discard type (spell→draw; gear→ready 2 runes; unit→+3 Might). The carry — move it every turn for value. |
| **Fizz - Trickster** (Might 3) | On play, replay a **≤3-Energy** spell from trash for free (still pay Power), then recycle it. Reuses Moonfall/Gust — the late-game gas. |
| **Vex - Apathetic** (Might 4, Deflect) | Stuns a unit the opponent plays onto its battlefield. The stun **auto-selects** the unit, so it isn't a "target" — targeting protection can't stop it. Locks a Hold. |
| **Ravenbloom Student** (Might 2) | *When you play a spell:* +1 Might this turn. Turns the reaction pile into an offensive clock. |
| **Gust / Stupefy / Star-Crossed / Smoke Screen** | The cheap [Reaction] toolbox. Gust bounces a unit with ≤3 Might; Star-Crossed bounces **one of yours + one enemy** (a real cost); Stupefy is −1 Might + draw; Smoke Screen is −4 Might. **Stupefy & Smoke Screen floor at 1 Might — they shrink, they don't kill.** |

> **Watch the fine print a greedy line ignores:** Diana adds **Energy only** —
> Moonfall / Star-Crossed / Smoke Screen still cost **Power**, so a "free" trick stack
> still drains runes; and the shrink spells can't take a unit below 1 Might.

### On your turn — *Is this THE showdown, and how deep do I commit?*

```mermaid
flowchart TD
    A["Contested showdown is live.<br/>You hold cheap [Reaction]s + an unexhausted Diana (showdown-only +1 Energy)."]:::ctx
    A --> Q1{"Does winning THIS showdown bank or protect<br/>a point THIS turn? (a Conquer, or defend a Hold toward 8)"}:::q

    Q1 -->|"No — midboard scuffle, nothing scores"| T1["Fire Gust/Stupefy/Moonfall to win a meaningless fight"]:::trap
    T1 --> T1o["Tricks + Energy gone; no answer on the real scoring turn"]:::trap

    Q1 -->|"Yes"| Q2{"Can you still defend their next-turn push<br/>after committing?"}:::q

    Q2 -->|"No — winning empties your hand"| C1["Under-commit or concede; hold the stack, take the tempo loss"]:::good
    C1 --> C1o["Stay un-tapped — Diana wins attrition, so don’t trade efficiency for a marginal point"]:::good

    Q2 -->|"Yes"| Q3{"Are you ahead on visible runes, so they may<br/>play around a trick you might not even need?"}:::q

    Q3 -->|"Yes"| R1["REPRESENT: leave Diana unexhausted, let the threat do the work"]:::good
    R1 --> R1o["Win the fight for free; keep the cards and the bluff"]:::good

    Q3 -->|"No — they’ll push through"| W1["COMMIT: exhaust Diana for +1 showdown Energy,<br/>chain the MINIMUM tricks so your unit lives and theirs doesn’t"]:::good
    W1 --> W1o["Bank the point efficiently, then Hold it — the deck’s whole win pattern"]:::good

    classDef ctx fill:#f6f8fa,stroke:#57606a,color:#24292f;
    classDef q fill:#e8f0fe,stroke:#1a73e8,stroke-width:2px,color:#12325f;
    classDef good fill:#e6f4ea,stroke:#188038,stroke-width:2px,color:#0d3b1e;
    classDef trap fill:#fdecea,stroke:#d93025,stroke-width:2px,color:#5f1a15;
```

**Greedy vs. expert.** *Greedy:* exhausts Diana every fight (tipping the interaction) and
dumps tricks into scuffles that score nothing, then has no answer when a point is
actually on the line. *Expert:* represents the un-reactable Energy without spending it,
and empties the stack only on a Conquer/Hold-protecting showdown it can still defend
after.

### On the opponent's turn (defending) — *Shave the attack to a survivor, cheapest first*

Diana defends inside the showdown: her legend's **+1 Energy is un-reactable and exists
only in combat**, so she can answer with more than her visible runes show. She denies a
Conquer by keeping a defender alive — bounce or shrink attackers so one of her bodies
survives.

```mermaid
flowchart TD
    A["Opponent’s turn: they attack a battlefield you contest (Showdown → you gain Focus),<br/>or cast a spell (Closed chain → [Reaction]s only)."]:::ctx
    A --> Q1{"If unanswered, does their attack leave you with NO unit at a battlefield you need<br/>(they Conquer a point you can’t give up)?"}:::q

    Q1 -->|"No — a defender survives, or the battlefield is worthless"| H1["Hold everything. Don’t exhaust Diana, don’t fire a reaction; pass Focus.<br/>Bank the reactions + showdown Energy for the battlefield that matters"]:::good
    H1 --> H1o["Zero resources spent, point denied, full interaction kept"]:::good

    Q1 -->|"Yes"| E1["Exhaust Diana NOW for +1 showdown Energy (un-reactable — can’t be stopped)"]:::good
    E1 --> Q2{"Do they still have open resources / a trick represented?"}:::q
    Q2 -->|"Yes — bait it"| B2["Pass; let them commit their trick to the chain, then answer it<br/>(your [Reaction] resolves first, or Hard Bargain taxes it 2E), THEN shrink/bounce to keep a survivor"]:::good
    B2 --> B2o["You avoid being two-for-one’d and still deny the point"]:::good
    Q2 -->|"No — wide attack (many small units)"| B3["Moonfall ([Action]) — pull one in, -2 Might to ALL enemies there"]:::good
    B3 --> B3o["One card collapses the whole stack so a defender survives"]:::good
    Q2 -->|"No — one big attacker"| B4["Cheapest sufficient answer to leave a survivor: Stupefy (-1) → Smoke Screen (-4)<br/>→ Gust (bounce a ≤3 attacker). Star-Crossed if you can also rescue your own dying body"]:::good
    B4 --> B4o["Point denied for minimum resource; the rest carries to the next showdown"]:::good

    A -.->|"naive line"| T["✗ Fire Smoke Screen on the biggest body immediately (no Diana Energy),<br/>or spend a trick to defend a battlefield you don’t need"]:::trap
    T --> To["Tips your hand, walks into their trick, and empties answers for the real scoring turn"]:::trap

    classDef ctx fill:#f6f8fa,stroke:#57606a,color:#24292f;
    classDef q fill:#e8f0fe,stroke:#1a73e8,stroke-width:2px,color:#12325f;
    classDef good fill:#e6f4ea,stroke:#188038,stroke-width:2px,color:#0d3b1e;
    classDef trap fill:#fdecea,stroke:#d93025,stroke-width:2px,color:#5f1a15;
```

*(Note: Hard Bargain's [Repeat] raises the tax on the **same** spell to 4 Energy — it
doesn't counter a second spell. Vex - Apathetic, set up on your turn, is a standing
defensive lock: it Stuns any unit the opponent plays onto its battlefield.)*

**Sources.** [Diana champion deck guide — RQ Vancouver winner (riftboundguide.com, 2026-06-08)](https://riftboundguide.com/2026/06/08/riftbound-diana-champion-deck-guide/) ·
[Diana legend page — card text, tier, tournament results (Hextech Analytics)](https://hextechanalytics.com/legends/diana) ·
[Diana tempo / counter matchup (RiftStorm.gg)](https://riftstorm.gg/blog/diana-counter-riftbound-tempo) ·
[Vex - Apathetic ruling — auto-selected stun isn't a "target" (riftboundfaq.com)](https://www.riftboundfaq.com/cards/vex-apathetic) ·
[Scoring, in depth (riftbound.gg)](https://riftbound.gg/the-in-depth-guide-to-scoring-in-riftbound/) *(browser-reachable; bot-walls automated fetches)*.

---

## Vi — Piltover Enforcer
*(Fury / Order — proactive beatdown / tempo-midrange)*

**Game plan.** Race the board: win showdowns for battlefields faster than the opponent
can defend, and chain a *second* conquest off the same turn. Every attack aims at one
number — beat the defenders' **total** Might by at least **3 excess damage**, so Vi's
legend (*"When you conquer, if you assigned 3+ excess damage, you may exhaust me to ready
a unit"*) fires and you ready an attacker — ideally a **Ganking** unit that moves to and
contests a *second* battlefield the same turn. One turn's energy threatens two points.

**Win condition.** 8 points via **Conquer** (win an attacking showdown at a battlefield
you don't control — scores when the showdown *resolves*) plus **Hold**. The overkill →
ready → second-battlefield chain is what lets one turn touch two battlefields — which is
also how the **8th point** becomes reachable (a lone conquer can't take the last point
unless you conquered *every* battlefield that turn).

**Power curve.** Strongest mid-game (~T3–6) once Accelerate enablers (Rek'Sai, Rengar)
are down and you have enough board Might — plus a buff or removal — to reliably clear the
+3 line and ready-chain. Weakest very early (no Might on board → the legend does nothing)
and in grindy late games vs. disciplined multi-blocker defenses or reactive removal that
kills your buffed attacker mid-commit. *(Meta note: Vi is a fringe competitive pick — as
of 2026-07-10 Hextech Analytics tracks her around **D-tier / ~1% meta share** with no
tracked top-8s in the trailing ~14 days. The lines below are about piloting the deck
well, not a claim that it's meta-strong.)*

| Card | What it does |
|---|---|
| **Vi - Piltover Enforcer** (Legend) | Conquer with **3+ excess damage** → exhaust her to **ready a unit**. Keep her home and un-exhausted; her exhaust is the cost, so one ready per turn. The whole deck serves this trigger. |
| **Cleave** / **Against the Odds** | **Overkill fuel** — the *right* way to reach +3. Cleave = **[Assault 3]** (+3 Might attacking); Against the Odds = **+2 Might per enemy unit** at the battlefield. Adding attacker Might raises excess. |
| **Sky Splitter** / **Hidden Blade** / **Falling Star** | **Blocker removal** — the *other* way to reach +3: kill a defender so there's less total Might to beat. Sky Splitter's cost drops by your highest Might (often near-free, deal 5); Hidden Blade kills at instant speed (they draw 2). |
| **Rengar - Unseen** (Might 4) | The premier ready-chain target: **Ganking** (move battlefield-to-battlefield) opens a second front, **Deflect** shields it, **Assault 2** helps hit overkill. |
| **Rek'Sai - Breacher** (Might 3, Assault) | Grants **[Accelerate]** to units played from non-hand — they *may* pay 1 Energy + 1 Fury to enter ready and attack immediately (an optional cost, not free). |
| **Vi - Peacekeeper** (Might 5, Ambush) | Flash onto a contested battlefield as a Reaction; on attack, **Stun** an enemy here. The Stun is **defensive** — it stops that unit dealing damage back so you *win* the fight; it does **not** lower the overkill bar (see below). |
| **Ferrous Forerunner** (Might 6) | Resilient top-end: **[Deathknell]** → two 3-Might Mech tokens to base, keeping the board wide through trades. |

> **The correction that matters:** **Stun does not help you reach +3 excess.** Stun only
> zeroes the *outgoing* damage a unit deals back to you — a stunned blocker is **still on
> the battlefield and still needs its full Might in lethal to be killed**, so stunning it
> doesn't reduce the damage you must assign to clear the fight. You raise excess only by
> **adding attacker Might** (Cleave, Against the Odds) or **killing a defender outright**
> (Sky Splitter, Hidden Blade, Falling Star), which takes its Might off the board entirely.
> (Deathgrip is *not* removal — it sacrifices your *own* unit to buff another + draw.)
> *(Rules confirmed: [Rift Watcher — Stun](https://riftwatcher.com/rules/stun/),
> [RiftJudge](https://app.riftjudge.com/questions).)*

### On your turn — *Engineer +3 excess, then cash the ready into a second point*

```mermaid
flowchart TD
    A["You want to attack a defended battlefield.<br/>Excess = your assigned damage beyond the defenders’ TOTAL Might."]:::ctx
    A --> Q1{"Will your committed Might beat the defenders’<br/>TOTAL Might by 3 or more?"}:::q

    Q1 -->|"Already +3 or more"| Q2{"Do you have a unit that can reach<br/>a SECOND battlefield if readied?"}:::q
    Q2 -->|"Yes"| W1["Attack, conquer, exhaust Vi to READY that unit<br/>(prefer a Ganking unit), move it to contest a second battlefield"]:::good
    W1 --> W1o["Two points of pressure from one turn — the deck’s best swing"]:::good
    Q2 -->|"No reachable second target"| P1["Take the plain +N conquer for 1 point;<br/>don’t waste Vi’s exhaust on a ready that goes nowhere"]:::good
    P1 --> P1o["Steady one-point progress, resources conserved"]:::good

    Q1 -->|"Only +0 to +2, but I hold a buff / removal"| B2["ADD attacker Might (Cleave +3 / Against the Odds +2 per enemy)<br/>OR KILL the gating defender (Sky Splitter / Hidden Blade / Falling Star), THEN swing"]:::good
    B2 --> B2o["Converts a flat 1-point conquer into a legend trigger + free readied attacker"]:::good

    Q1 -->|"Can’t cross +3, or it’s a removal/Deflect trap"| C1["Decline the greedy overkill: develop board, hold Ambush/Hidden,<br/>attack a softer battlefield or bait the answer first"]:::good
    C1 --> C1o["Preserve attackers/tempo; attack on your terms next turn"]:::good

    A -.->|"naive line"| T["✗ Swing for a ’clean’ +0 to +2 conquer,<br/>OR Stun a blocker expecting to inflate excess"]:::trap
    T --> To["1 point and NO ready (Stun doesn’t lower the overkill bar) — Vi’s whole engine idles"]:::trap

    classDef ctx fill:#f6f8fa,stroke:#57606a,color:#24292f;
    classDef q fill:#e8f0fe,stroke:#1a73e8,stroke-width:2px,color:#12325f;
    classDef good fill:#e6f4ea,stroke:#188038,stroke-width:2px,color:#0d3b1e;
    classDef trap fill:#fdecea,stroke:#d93025,stroke-width:2px,color:#5f1a15;
```

**Naive vs. expert.** *Naive:* swings for a tidy conquer at +0–+2 (one point, no ready),
or Stuns a wall expecting the excess to jump. *Expert:* does the arithmetic first, spends
a buff or a kill to cross +3, and readies a *reaching* unit — one turn, two battlefields.

### On the opponent's turn (defending) — *Win the Might math (there's no counter, and no defensive Stun)*

Vi is a **proactive race deck** — its "defense" is winning the defensive showdown's math,
not a control shell. It has **no counterspell**, and — critically — **Vi - Peacekeeper's
Stun is "when I *attack*"**, so Ambushing her on defense makes her a plain **Might-5
blocker**, not a stun. Over-defending is how this deck loses its tempo edge.

```mermaid
flowchart TD
    A["Opponent attacks a battlefield you hold. Your only defensive tools are combat math:<br/>Against the Odds ([R] +2/enemy), Deathgrip ([R] sac→buff), a pre-hidden Hidden Blade ([Action] kill), an Ambush body."]:::ctx
    A --> Q1{"Is this a point you actually need to keep, and can you keep a defender alive?"}:::q

    Q1 -->|"Not needed / you’re ahead on the race"| L1["Let it resolve. Hold everything; stay on your proactive clock<br/>(you win by conquering faster, and the legend rewards overkill conquers)"]:::good
    L1 --> L1o["Concede 1 point but keep all tempo + interaction — usually correct for Vi"]:::good

    Q1 -->|"One big attacker & you pre-hid Hidden Blade"| K1["Flip Hidden Blade for 0 ([Action] in the showdown) to KILL the key attacker —<br/>its Might leaves the fight entirely, so your defender survives"]:::good
    K1 --> K1o["Point denied, threat gone; Peacekeeper stays free for your next attack"]:::good

    Q1 -->|"WIDE attack (several units)"| W1["Against the Odds — +2 Might per ENEMY unit there (scales with their commit)<br/>to push a defender over the lethal it will eat; or Deathgrip a chump into a bigger body"]:::good
    W1 --> W1o["Defender outlasts the damage → No Conquer; the scaling pump matches a wide swing"]:::good

    Q1 -->|"You just need more blocking Might"| B1["Ambush Vi - Peacekeeper as a bare Might-5 body (she does NOT Stun on defense) —<br/>her 5 Might joins the defense so a body survives"]:::good
    B1 --> B1o["Reach a survivor; she stays as a re-blocker next turn"]:::good

    A -.->|"naive line"| T["✗ Ambush Vi expecting her Stun to blank the attacker"]:::trap
    T --> To["Her Stun only fires when she ATTACKS — a defensively-Ambushed Vi is just a Might-5 body. The point resolves"]:::trap

    classDef ctx fill:#f6f8fa,stroke:#57606a,color:#24292f;
    classDef q fill:#e8f0fe,stroke:#1a73e8,stroke-width:2px,color:#12325f;
    classDef good fill:#e6f4ea,stroke:#188038,stroke-width:2px,color:#0d3b1e;
    classDef trap fill:#fdecea,stroke:#d93025,stroke-width:2px,color:#5f1a15;
```

**Sources.** [Vi champion deck guide (riftboundguide.com, 2026-04-08)](https://riftboundguide.com/2026/04/08/riftbound-vi-champion-deck-guide/) ·
[How damage / excess works (riftboundguide.com)](https://riftboundguide.com/2026/03/29/how-damage-works-in-riftbound/) ·
[Combat rules (Rift Watcher)](https://riftwatcher.com/rules/combat/) ·
[Stun — deals no damage but still needs full lethal (Rift Watcher)](https://riftwatcher.com/rules/stun/) ·
[Ambush — pure play-timing, no stun on defense (Rift Watcher)](https://riftwatcher.com/rules/ambush/) ·
[Vi legend page — meta stats (Hextech Analytics)](https://hextechanalytics.com/legends/vi) ·
[Keyword glossary (runesandrift)](https://runesandrift.com/riftbound-keywords/).

---

## Azir — Emperor of the Sands
*(Calm / Order — Equipment-gated Sand Soldier swarm)*

**Game plan.** Azir's legend makes a 2-Might **Sand Soldier** token for 1 Energy — **only
if you've played an Equipment this turn** — and Sand Soldiers have **[Weaponmaster]** (they
can wear that Equipment, equipping for **1 Power less**, which is *free* for the 1-cost gear
the deck runs). So each turn: **play one cheap Equipment → make a Soldier → suit it up**,
building a go-wide board. The payoff is **Arise!** (a Soldier per Equipment you control,
ready up to two), which floods two battlefields at once for a double-conquer /
conquer-and-hold closing turn.

**Win condition.** 8 points via Conquer + Hold, using the token width to win showdowns at
**two** battlefields at once. Arise! + Azir - Sovereign's token-pull is the classic ~6→8
finisher (and satisfies the last-point rule by touching both boards the same turn).

**Power curve.** Strongest mid-game (T3–6): the equipment→legend loop makes a
Weaponmaster-buffed Soldier every turn, out-tempoing slower decks. Peak is the Arise! +
Sovereign flood. Weakest turn 1 (nothing to gate yet) and into **board wipes** — dumping
the whole board into a sweeper with no reload is how Azir loses winnable games.

| Card | What it does |
|---|---|
| **Azir - Emperor of the Sands** (Legend) | 1 Energy, exhaust → 2-Might Sand Soldier to base, **only if you played an Equipment this turn**. Grants your Sand Soldiers **[Weaponmaster]**. The gate is the whole deck's tempo. |
| **Arise!** (6 Energy + 1 Power, Signature) | Play a 2-Might Sand Soldier **per Equipment you control**, then **ready up to two**. With 4–6 gear out, an instant army — the finisher. |
| **Azir - Sovereign** (Might 4) | The closer: on attack, move **any number** of your token units to his battlefield to win that conquer, freeing width to contest a second. |
| **1-cost Equipment** (Doran's Shield · Eye of the Herald · Soul Sword) | The gate keys. Cheap [Equip] stat-fixers; playing **one per turn** keeps the engine live and gives Sand Soldiers something to wear for free via Weaponmaster. |
| **Guards!** / **Back Off** (Hidden) | Instant-speed plays: Guards! flips for 0 to make a Soldier (may pay Order to ready it); Back Off Stuns a unit (+draw from hand). Surprise defense / extra body. |
| **Discipline** (2 Energy, Reaction) | +2 Might **and draw 1** — the go-to showdown pump that also refuels an Equipment-hungry hand. |

> **The rule that anchors the whole deck:** [Weaponmaster]'s reminder text reads *"when
> they're played, you may [Equip] one of your Equipment to them for 🌈 less"* — i.e.
> **1 Power (one rune) cheaper**, which zeroes out the 1-cost gear the deck runs. And the
> legend's token only appears **if an Equipment was already played this turn** — so the
> order of operations (gear first, always) is not a preference, it's the engine.

### On your turn — *Play one Equipment first, every turn, to arm the gate*

```mermaid
flowchart TD
    A["It’s your main phase. Before you touch the board or cast a spell:"]:::ctx
    A --> Q1{"Do you have a cheap Equipment to play this turn?"}:::q

    Q1 -->|"No"| N1["Do NOT tap Azir for a dead token.<br/>Dig (Discipline / Scuttle Crab), hold reactions, re-arm next turn"]:::good
    N1 --> N1o["Engine-off turn by choice; runes kept up for defense"]:::good

    Q1 -->|"Yes"| Q2{"Is this the Arise! finisher turn?<br/>(4+ Equipment in play, wide board, can contest TWO battlefields)"}:::q

    Q2 -->|"No — normal grind turn"| G1["Play ONE Equipment FIRST → exhaust Azir (1E) for a 2-Might Soldier →<br/>free-attach the gear via Weaponmaster. Bank any extra gear"]:::good
    G1 --> G1o["Engine stays live every turn; a stat-boosted Soldier joins the board while you ration fuel"]:::good

    Q2 -->|"Yes"| F1["Break the ration: cast Arise! (a Soldier per Equipment, ready up to two),<br/>attack with Azir - Sovereign to pull the swarm and win BOTH battlefields"]:::good
    F1 --> F1o["Flood two boards at once and jump toward 8 — the intended kill turn"]:::good

    Q2 -->|"Yes, but facing a board-wipe deck"| F2["Open the gate with one gear + one Soldier, but KEEP a second threat + gear in hand;<br/>save Arise! as the post-wipe reload"]:::good
    F2 --> F2o["Keep chipping points while holding rebuild fuel — one sweeper doesn’t end the game"]:::good

    A -.->|"naive line"| T["✗ Tap Azir or cast a spell FIRST (skip a whole Soldier),<br/>or dump TWO gears in one turn"]:::trap
    T --> To["Gate never opens (a turn’s tempo gone) — or two gears make zero extra tokens and thin future turns"]:::trap

    classDef ctx fill:#f6f8fa,stroke:#57606a,color:#24292f;
    classDef q fill:#e8f0fe,stroke:#1a73e8,stroke-width:2px,color:#12325f;
    classDef good fill:#e6f4ea,stroke:#188038,stroke-width:2px,color:#0d3b1e;
    classDef trap fill:#fdecea,stroke:#d93025,stroke-width:2px,color:#5f1a15;
```

**Naive vs. expert.** *Naive:* taps Azir or casts a spell before playing gear (the gate
never opens, a Soldier lost — the deck's #1 tempo leak), or dumps two gears for zero extra
tokens. *Expert:* gear→legend→equip in that order every turn, rationing to one gear except
the Arise! turn, and holds rebuild fuel against sweepers.

### On the opponent's turn (defending) — *Keep one Sand Soldier alive; deny for free when the math holds*

Azir's swarm makes defense cheap: a Conquer needs the opponent to kill **every** defender
there, so **one surviving Sand Soldier cancels the point**. Spend a reaction only when the
incoming damage would wipe all your bodies — cheapest line first, and save answers for the
game-ending Conquer.

```mermaid
flowchart TD
    A["Opponent attacks a battlefield you hold with Sand Soldiers.<br/>Kit: Back Off ([Hidden]/[Action] Stun +draw), Defy ([R] counter ≤4E/≤1P), Guards! ([Hidden] Soldier), Hidden Blade (kill), pumps."]:::ctx
    A --> Q1{"Will the incoming damage kill EVERY defender I have here?"}:::q

    Q1 -->|"No — a Sand Soldier survives on raw Might"| N1["Do nothing. The survivor denies the Conquer for free; hold all reactions"]:::good
    N1 --> N1o["Point denied at zero cost; full answer suite kept for the real threat"]:::good

    Q1 -->|"Yes — one oversized attacker, Back Off ready"| S1["Stun it with Back Off (no chain needed, +draw from hand).<br/>Its damage leaves the fight → your soldiers survive"]:::good
    S1 --> S1o["Cheapest denial + a card; better than Hidden Blade (no ’draw 2’ gift to them)"]:::good

    Q1 -->|"Yes — enabled by a spell ≤4E/≤1P on the chain"| D1["Defy that spell as a [Reaction] — it resolves first, so the buff/removal never happens"]:::good
    D1 --> D1o["Point denied by removing the enabler; note the cap — a 5+E / 2+P bomb is uncounterable"]:::good

    Q1 -->|"Yes — spread across attackers, or Defy out of range"| A1["Add a body instead of removing one: reveal Hidden Guards! (a Sand Soldier),<br/>or pump a lone defender (Discipline/En Garde/Deathgrip) so ONE outlasts the damage"]:::good
    A1 --> A1o["One survivor cancels the Conquer; Guards! leaves a body they must also kill"]:::good

    A -.->|"naive line"| T["✗ Spend a reaction on the first attack even though a soldier already survives"]:::trap
    T --> To["Answers wasted before the game-ending Conquer"]:::trap

    classDef ctx fill:#f6f8fa,stroke:#57606a,color:#24292f;
    classDef q fill:#e8f0fe,stroke:#1a73e8,stroke-width:2px,color:#12325f;
    classDef good fill:#e6f4ea,stroke:#188038,stroke-width:2px,color:#0d3b1e;
    classDef trap fill:#fdecea,stroke:#d93025,stroke-width:2px,color:#5f1a15;
```

**Sources.** [Token Azir deck tech (Cards Realm)](https://riftbound.cardsrealm.com/en-us/articles/riftbound-deck-tech-token-azir) ·
[Weaponmaster — equip for 1 Power less (Rift Watcher)](https://riftwatcher.com/rules/keywords/weaponmaster/) ·
[Keyword glossary — Weaponmaster / Accelerate (learnriftbound.gg)](https://learnriftbound.gg/glossary) ·
[Spiritforged keyword rundown (runesandrift)](https://runesandrift.com/riftbound-spiritforged-keywords/) ·
[Spiritforged core rules / patch notes (official, playriftbound.com)](https://playriftbound.com/en-us/news/rules-and-releases/riftbound-core-rules-spiritforged-patch-notes/) ·
[Azir guide (riftbound.gg)](https://riftbound.gg/azir-emperor-of-the-sands-guide/) *(browser-reachable; bot-walls automated fetches)*.

*(The Weaponmaster reduction was confirmed as **1 Power less** by four independent sources; the featured Cards Realm list placed 2nd in group B at Ascension League stage 2 — the only tournament result found, no win-rate figures.)*

---

## Lillia — Bashful Bloom
*(Calm / Mind — [Temporary] Sprite tempo)*

**Game plan.** Flood **[Temporary]** Sprite tokens and use them as **use-it-now Conquer
tools**. A Temporary unit is killed at the start of your next Beginning Phase **before Hold
scoring** — so a Sprite can **Conquer** for an immediate point the turn it's made, but can
**never Hold**. Lillia's legend (4 Energy, exhaust → a **ready** 3-Might Temporary Sprite,
**−1 Energy per friendly Temporary unit**) plus Sprite Burst (two ready Sprites) generate
the pressure; you race to ~6–7 on Sprite conquers, then seal it with a **durable** unit.

**Win condition.** 8 points, mostly via **Conquer**. Crucially, your **Hold points and the
legal 8th point must come from non-Temporary units** (Fae Fawn, Watcher, Faefolk, Poro,
Student) — a Sprite left "to hold" evaporates before scoring. Thousand-Tailed Watcher
(ETB: all enemies −3 Might) softens both battlefields for a closing double-conquer.

**Power curve.** Strongest early-to-mid (T1–5): can pressure or conquer a battlefield as
early as turn one and snowball on relentless Sprite conquers. Weakest if the race stalls
(Sprites can never Hold and evaporate each upkeep) and into **Vex - Apathetic**, which
Stuns a Sprite *played onto its battlefield* — the deck's primary hard counter.

| Card | What it does |
|---|---|
| **Lillia - Bashful Bloom** (Legend) | 4 Energy, exhaust → a **ready** 3-Might **[Temporary]** Sprite; **−1 Energy per friendly [Temporary] unit**. Activate it **last** each turn so the discount is maxed. |
| **Sprite Burst** (5 Energy) | Two **ready** 3-Might Temporary Sprites at once — the enabler for conquering **both** battlefields in one turn. |
| **Lillia - Fae Fawn** (Might 3) | [Accelerate]. When she **moves** from a location, drop a 3-Might Temporary Sprite there — but that Sprite enters **exhausted** (it can't attack the turn it's made). |
| **Heart of Dark Ice** (gear) | Exhaust: **+3 Might** to a unit this turn — turns a 3-Might Sprite into a 6-Might attacker that actually breaks a blocker to Conquer. |
| **Thousand-Tailed Watcher** (Might 7) | Primary closer: [Accelerate], ETB **all enemies −3 Might** — deploy near 6 points to shrink both battlefields for a double-conquer. |
| **Unchecked Power** (7 Energy + 2 Power) | Reset: exhaust **all** friendly units, then **12 damage to ALL units at battlefields**. A *symmetric* wipe — fire it when the opponent's durable board out-values yours (you re-flood Sprites next turn; they don't). |

> **The correction that matters:** only the **legend's** and **Sprite Burst's** Sprites
> enter **ready** (their text says so). **Fae Fawn's** move-trigger Sprite enters
> **exhausted** — it holds/contests but can't attack the turn it appears.

### On your turn — *Conquer this turn, or nothing: how to spend each ready Sprite*

```mermaid
flowchart TD
    A["You have one or more READY [Temporary] Sprites this turn<br/>(legend + Sprite Burst make ready ones; Fae Fawn’s move-Sprite is exhausted).<br/>Each dies at your next upkeep, BEFORE Hold scoring."]:::ctx
    A --> Q1{"Are you at 7 points / trying to take the FINAL point?"}:::q

    Q1 -->|"Yes"| L1["Do NOT rely on a Sprite for the point.<br/>Put a NON-Temporary unit (Watcher/Faefolk/Poro/Student/Fae Fawn) on the battlefield to Hold;<br/>use Sprites only to Conquer the REMAINING battlefields this same turn"]:::good
    L1 --> L1o["A legal finish — the 8th point comes from a real unit’s Hold or a same-turn all-battlefield conquer"]:::good

    Q1 -->|"No"| Q2{"Can this Sprite WIN an attacking showdown<br/>at an uncontrolled battlefield this turn?<br/>(with Heart of Dark Ice +3 / Discipline / Watcher -3 if needed)"}:::q

    Q2 -->|"Yes — and I have two (Sprite Burst)"| D1["Split them to Conquer BOTH battlefields<br/>(Watcher’s -3 Might first to clear defenders)"]:::good
    D1 --> D1o["Double-Conquer — jump two points, the core ~2/turn engine"]:::good

    Q2 -->|"Yes — one Sprite"| C1["Attack and Conquer for an immediate point;<br/>pump with Heart of Dark Ice / Discipline to guarantee the win"]:::good
    C1 --> C1o["Bank a point that turn — the only way a Sprite ever scores"]:::good

    Q2 -->|"No, but losing an incoming showdown would let them Conquer ME"| H1["Hold ONE Sprite back as a chump to deny their Conquer;<br/>Conquer with the rest"]:::good
    H1 --> H1o["Trade the token’s inevitable death for denying an enemy point"]:::good

    Q2 -->|"No, and not needed as a blocker"| F1["Still Conquer an undefended battlefield if any, else feed it into a trade —<br/>never park it for ’future’ value"]:::good
    F1 --> F1o["Extract the tempo that exists now; the Sprite has zero future"]:::good

    A -.->|"naive line"| T["✗ Park a Sprite on a battlefield ’to Hold it’,<br/>or expect a Sprite to take the 8th point"]:::trap
    T --> To["It dies at upkeep before Hold scoring → scores nothing; the turn is wasted"]:::trap

    classDef ctx fill:#f6f8fa,stroke:#57606a,color:#24292f;
    classDef q fill:#e8f0fe,stroke:#1a73e8,stroke-width:2px,color:#12325f;
    classDef good fill:#e6f4ea,stroke:#188038,stroke-width:2px,color:#0d3b1e;
    classDef trap fill:#fdecea,stroke:#d93025,stroke-width:2px,color:#5f1a15;
```

**Naive vs. expert.** *Naive:* parks Sprites "to hold a battlefield" (they vanish at
upkeep, scoring nothing) or expects a Sprite to take the last point. *Expert:* Conquers
with every ready Sprite the turn it exists (splitting Sprite Burst across both
battlefields), reserves a durable unit for the Hold and the 8th point, and fires Unchecked
Power only when the board favors the opponent.

### On the opponent's turn (defending) — *Chump with a dying-anyway Sprite*

Lillia's [Temporary] Sprites are **already dying** at your next upkeep, so blocking/trading
one to deny a Conquer costs **nothing** — the ideal defensive resource. Keep a survivor at
the battlefield (a No Result denies the point), spend a real card only when the free chump
won't cover it.

```mermaid
flowchart TD
    A["Opponent attacks a battlefield your Sprites contest.<br/>Reactions available in the showdown: Discipline (+2 +draw), Stupefy (-1 +draw); Defy ([R] counter) on their chain."]:::ctx
    A --> Q1{"Do you already have TWO+ Sprites there, so one survives the trade?"}:::q

    Q1 -->|"Yes"| N1["Do nothing. Let a Sprite trade; one survivor = No Result — you keep the battlefield for ZERO cards<br/>(the traded Sprite was dying next upkeep anyway)"]:::good
    N1 --> N1o["The ideal default — free point-denial that fuels the whole tempo plan"]:::good

    Q1 -->|"One Sprite blocks but will die and leave the attacker standing"| C1["Spend the MINIMUM in the showdown to leave a survivor:<br/>Discipline (+2 so it lives) or Stupefy (-1 the attacker) — both cantrip"]:::good
    C1 --> C1o["Forces a No Result and usually draws a card — cheap point-denial"]:::good

    Q1 -->|"They cast a spell ≤4E/≤1P to break your block (Closed chain)"| D1["Defy it as a [Reaction] — it resolves first, so their removal/pump never happens"]:::good
    D1 --> D1o["Block holds, Conquer denied, no body spent"]:::good

    Q1 -->|"You’re ahead on the race, or holding costs cards you need elsewhere"| L1["Let the Sprites die and the opponent Conquer; redeploy Sprites next turn<br/>(Fae Fawn on move, the legend for 0-1 Energy) and out-tempo them"]:::good
    L1 --> L1o["Trade a point of board for card/tempo — Lillia regenerates bodies faster than they convert battlefields"]:::good

    classDef ctx fill:#f6f8fa,stroke:#57606a,color:#24292f;
    classDef q fill:#e8f0fe,stroke:#1a73e8,stroke-width:2px,color:#12325f;
    classDef good fill:#e6f4ea,stroke:#188038,stroke-width:2px,color:#0d3b1e;
    classDef trap fill:#fdecea,stroke:#d93025,stroke-width:2px,color:#5f1a15;
```

*(Unchecked Power — exhaust all friendly units + 12 to all battlefield units — is a
**your-main-phase** reset, not a reaction: fire it when they out-commit with big *real*
units, since your Sprites were dying anyway.)*

**Sources.** [Lillia aggro deck tech (Cards Realm, 2026-07-05)](https://riftbound.cardsrealm.com/en-us/articles/riftbound-deck-tech-lillia-aggro) ·
[Keyword glossary — [Temporary] reminder text (runesandrift)](https://runesandrift.com/riftbound-keywords/) ·
[Glossary — Temporary (Riftbound Wiki / Fextralife)](https://riftbound.wiki.fextralife.com/Glossary) ·
[Keywords — Temporary (riftboundguide.com)](https://riftboundguide.com/keywords/) ·
[Turn order & the scoring phase (runesandrift)](https://runesandrift.com/riftbound-turn-order/) ·
[Hold vs conquer ruling (RiftJudge #1297)](https://app.riftjudge.com/rulings/1297/how-does-scoring-work-in-riftbound-particularly-regarding-holding-and-conquering).

*(All three glossaries give the [Temporary] reminder — "killed at the start of its controller's Beginning Phase, **before scoring**" — and Cards Realm confirms Fae Fawn is "the only effect in the game that summons an **exhausted** Sprite token" and that Vex - Apathetic hard-counters the deck.)*

---

## Leona — Radiant Dawn
*(Calm / Order — stun-control midrange / buff accrual)*

**Game plan.** Leona is Origins' Calm/Order stun legend: *"When you stun one or more enemy
units, buff a friendly unit. (If it doesn't have a buff, it gets a +1 Might buff.)"* Read
what is **not** in that text: no exhaust, no once-per-turn — the trigger is free, so
**every separate stun event pays a buff**, on your turn or theirs (the "one or more" clause
only collapses a simultaneous multi-stun into a single buff). The shell is a defensive
Calm/Order midrange — Defy, Discipline, Sona - Harmonious, Shield/Tank bodies — whose
interaction is the **stun suite instead of removal**: each attack into a battlefield you
hold is answered by a 2–3 Energy stun that blanks the attacker's damage *and* permanently
grows your board. The community verdict (Cards Realm's "Holding Leona") matches the card
text: hold battlefields, frustrate every attack, and let the buffs compound until your
units simply win the math.

**Win condition.** 8 points, Hold-leaning: conquer early or open ground, then keep it —
every defended showdown banks a point at your next turn start *plus* a permanent +1.
**Zenith Blade** (stun + move a friendly unit to that battlefield) and **Leona -
Determined**'s attack-stun add conquers when their board is committed elsewhere. The
final-point rule never hurts a hold deck — the 8th point is naturally a Hold. And the
finisher is timed to the scoreboard: **Leona - Zealot enters ready once an opponent is
within 3 of the Victory Score** (score 5+), a deploy-and-fight Might 6 whose aura makes
late showdowns unwinnable for a stunned board.

**Power curve.** Weakest T1–2: with no board the legend is blank, and a stun is a card
spent to blank one attack. Mulligan for the cheap Calm starters — **Lonely Poro** (2E,
Might 2, Deathknell: draw 1 if it died alone), **Stellacorn Herder** (4E, Might 3, *when I
move, draw 1*), **Sona - Harmonious** (4E + 1 pip — end-of-turn readies up to 4 runes,
funding the pip-heavy stuns). Strongest anchored mid-game (~T3–6): one stun per enemy
attack ≈ a saved point plus a permanent +1, every cycle. Late, Zealot ready-deploys once
they hit 5 points and **Eclipse Herald** (7E + 1 pip, Might 7) re-readies with +1 Might on
every stun for multi-showdown turns. Weak to go-wide boards (a stun blanks one body),
removal-dense decks (Kai'Sa, Ezreal), and its own card flow (Back Off from hand and Grove
of the God-Willow patch it). **Meta reality:** a fringe archetype — Rift Watcher lists her
**Tier C, ~24.5% win rate, 0.7% play rate** (point-in-time, accessed 2026-07-10), and she
sits outside Hextech Analytics' ranked S–C tiers with no tracked top-8s in the events
surveyed. Treat any single percentage as a snapshot (see Sources).

| Card | What it does |
|---|---|
| **Leona - Radiant Dawn** (Legend) | Stun one-or-more enemy units → **buff a friendly unit**. No exhaust in the cost → fires on **every stun event**, both turns; a simultaneous multi-stun collapses to one buff. Buffs are **one per unit** — spread them; a second buff on the same unit doesn't apply. |
| **Leona - Determined** (4E + 1 pip, Might 4) | **[Shield]** (+1 while defending) and *when I attack, stun an enemy unit here* — the deck's one proactive stun: blanks the scariest damage-back mid-showdown and banks a buff. The stunned defender still takes **full lethal** — her stun is armor, not a kill. |
| **Leona - Zealot** (6E + 1 pip, Might 6) | The converter: **stunned enemy units here have −8 Might, min 1** — at her battlefield a stunned body up to Might 9 is a Might 1 that dies to anything. *Enters ready if an opponent's score is within 3 of the Victory Score* — the catch-up finisher fights the turn it lands. |
| **Rune Prison** (2E + 1 pip) / **Thwonk!** (2E, Repeat 2E) / **Back Off** (3E, [Hidden]) | The stun stack — all **[Action]s**, live in showdowns. Thwonk! targets **attackers only** (pure defense; Repeat stuns a second one). Back Off **from hand** draws 1; pre-hidden it flips for 0E, no draw. |
| **Zenith Blade** (3E + 2 pips, [Action]) | The signature: stun an enemy at a battlefield **and move a friendly unit there** — deliver Zealot onto the stunned unit, or turn a stun into a contest. A near-staple alongside Defy and Discipline. |
| **Solari Chief** (5E + 1 pip, Might 4) | ETB: choose an enemy — **if it's stunned, kill it**; otherwise stun it. With a stun cast first this is the colour pair's only on-demand kill; **Solari Shrine** (3E gear) exhausts to draw 1 whenever you kill a stunned unit. |
| **Fiora - Victorious** (4E, Might 4) | The premier buff target: one legend buff makes her **Mighty (5+)** → **Deflect, Ganking and Shield** all switch on. The buff currency, cashed as keywords. |

> **The correction that matters:** stun is **damage prevention, not removal.** A stunned
> attacker still stands at resolution and still conquers if all your defenders die, and a
> stunned defender still takes full lethal to clear. What Leona uniquely owns is the
> **converters**: Zealot's aura makes stunned enemies at her battlefield Might 1, and Solari
> Chief kills a stunned unit outright. Both are **same-turn** plays — stun wears off at end
> of turn (*"doesn't deal combat damage **this turn**"*), so a stun banked on their turn is
> gone by yours. Stun, then convert, in one turn — or accept that the stun bought one turn
> of silence plus one buff, nothing more.

### On your turn — *Convert the stun the turn you cast it — never stun just to farm a buff*

```mermaid
flowchart TD
    A["Every stun event banks a permanent +1 buff on a friendly unit — the legend never exhausts.<br/>But buffs don’t stack (one per unit) and stun wears off at end of turn:<br/>convert it now, or it only bought silence."]:::ctx
    A --> Q1{"Where does this turn’s point come from —<br/>open ground, a Determined attack, or a stun-convert showdown?"}:::q

    Q1 -->|"A battlefield is open / lightly held"| G1["Claim it with a spare body and SAVE the stuns —<br/>they are your defense AND your buff engine on their turn"]:::good
    G1 --> G1o["1 point now, a hold stream from next turn, interaction intact"]:::good

    Q1 -->|"Defended, and raw Might clears their TOTAL"| G2["Attack with Leona - Determined in the party: her attack-stun blanks the scariest<br/>defender’s damage-back and banks a buff mid-showdown (Shield is defense-only — don’t count it)"]:::good
    G2 --> G2o["Conquer, a cheaper fight, a permanent +1 — her stun is armor, not removal"]:::good

    Q1 -->|"A key enemy body must DIE"| G3["Stun-convert in ONE turn: Rune Prison / Zenith Blade it, then Solari Chief kills it while stunned —<br/>or Zenith Blade moves Leona - Zealot in, where the stunned unit is Might 1 and dies in combat"]:::good
    G3 --> G3o["Real removal plus a body and a buff — the only way Calm/Order kills on demand"]:::good

    Q1 -->|"Opponent at 5+ points"| G4["Leona - Zealot enters READY — deploy her straight into the key showdown,<br/>and play for the Hold (the 8th point can’t be a lone conquer while a battlefield sits empty)"]:::good
    G4 --> G4o["The catch-up clause: your finisher costs no tempo exactly when you’re behind"]:::good

    A -.->|"naive line"| T["✗ Cast Rune Prison / Back Off at an idle unit on your own turn ’to farm a buff’,<br/>or pile every buff onto the same carry"]:::trap
    T --> To["An idle unit loses nothing to stun — a card for +1 Might — and a second buff on the same<br/>unit doesn’t apply. You enter their turn with no interaction left"]:::trap

    classDef ctx fill:#f6f8fa,stroke:#57606a,color:#24292f;
    classDef q fill:#e8f0fe,stroke:#1a73e8,stroke-width:2px,color:#12325f;
    classDef good fill:#e6f4ea,stroke:#188038,stroke-width:2px,color:#0d3b1e;
    classDef trap fill:#fdecea,stroke:#d93025,stroke-width:2px,color:#5f1a15;
```

**Naive vs. expert.** *Naive:* treats stun as removal — stuns a wall and swings expecting
the conquer, reflex-stuns every showdown, farms buffs on its own turn, and stacks them on
one carry (they don't stack). *Expert:* spends stuns on the **opponent's** turn where a
blanked attacker is a saved point, converts stun into a kill **same-turn** via Zealot or
Solari Chief when the body must die, and spreads the buffs so the whole board creeps out of
everyone's combat math.

### On the opponent's turn (defending) — *Their attack is your engine turn: one stun, one survivor, one buff*

Unlike an exhaust-gated draw engine, Leona's legend has **no once-per-turn throttle** —
every enemy showdown you interact with compounds the board, which makes this tree the
deck's engine room. All three stuns are **[Action]s**, legal once you gain Focus in their
showdown; only **Defy** works in the Closed state against their spells; and a bare unit
played in Neutral Open can't be responded to at all.

```mermaid
flowchart TD
    A["They attack a battlefield you hold. No Conquer = ONE of your units alive at resolution.<br/>A stun zeroes one attacker’s damage — and banks a permanent +1 buff even if the point falls.<br/>Tools: Thwonk! (2E, attackers only, Repeat 2E), Rune Prison (2E + 1 pip),<br/>Back Off (3E from hand draws 1; pre-hidden flip 0E), Defy, Discipline."]:::ctx
    A --> Q1{"Does zeroing ONE attacker’s damage<br/>leave you a survivor?"}:::q

    Q1 -->|"Yes — one carry does the damage"| S1["Thwonk! it (2E, the cheapest). Its damage vanishes,<br/>your defender lives, the legend banks a buff"]:::good
    S1 --> S1o["Point kept + board permanently bigger — the deck’s core exchange"]:::good

    Q1 -->|"Zealot defends here"| Z1["Stun their biggest anyway: at her battlefield it deals nothing AND drops to Might 1,<br/>so your combat damage kills it — deny the point and remove the body"]:::good
    Z1 --> Z1o["The one defensive stun in the game that IS removal"]:::good

    Q1 -->|"Wide attack — one stun isn’t enough"| W1["Count the remaining lethal: Discipline (+2 Might, draw 1) on the survivor, or Thwonk!’s Repeat<br/>(2E more) for a second attacker — only if it actually produces a survivor; otherwise let it go"]:::good
    W1 --> W1o["Their conquer scores once; your saved cards and permanent buffs keep paying"]:::good

    Q1 -->|"Their trick threatens the math"| C1["Hold Focus, let them commit the pump or removal first,<br/>then Defy it (counters up to 4E / 1 pip)"]:::good
    C1 --> C1o["The attack was budgeted around the trick — the whole showdown math flips"]:::good

    A -.->|"naive line"| T["✗ Reflex-stun the biggest attacker in every showdown"]:::trap
    T --> To["Stun cuts damage, not bodies: if the rest still clear your defenders, the stunned<br/>unit is standing at resolution — Conquer scored. A card for +1 Might, and the point lost anyway"]:::trap

    classDef ctx fill:#f6f8fa,stroke:#57606a,color:#24292f;
    classDef q fill:#e8f0fe,stroke:#1a73e8,stroke-width:2px,color:#12325f;
    classDef good fill:#e6f4ea,stroke:#188038,stroke-width:2px,color:#0d3b1e;
    classDef trap fill:#fdecea,stroke:#d93025,stroke-width:2px,color:#5f1a15;
```

**Sources.** [Holding Leona deck tech (Cards Realm)](https://riftbound.cardsrealm.com/en-us/articles/riftbound-deck-tech-holding-leona) ·
[Stun — not removal, still needs full lethal (Rift Watcher)](https://riftwatcher.com/rules/stun/) ·
[Keyword glossary — Stun (runesandrift)](https://runesandrift.com/riftbound-keywords/) ·
[Stun ruling (RiftJudge)](https://app.riftjudge.com/questions) ·
[Leona legend page — Tier C / 24.5% WR / 0.7% play (Rift Watcher)](https://riftwatcher.com/legend/leona/) ·
[Tier list — sample & tiers (Hextech Analytics)](https://hextechanalytics.com/tierlist). Note: riftbound.gg's Leona guide
and some riftdecks / mobalytics RQ lists bot-wall automated fetches (403), and Hextech's per-legend Leona figures sit in a
collapsed row that couldn't be machine-read; canon on this deck is thin, so the trees above lean on engine-verified card
text more than tournament consensus.

---

## Web Resources & Sources

Community and official references used to build and cross-check these guides. Each was
checked during the 2026-07-10 pass; a handful of community sites bot-wall automated
requests (noted below) and were used via search-index summaries only.

### Rules & keywords (game-wide)
- **[RiftJudge #1297 — how scoring works (Conquer vs Hold)](https://app.riftjudge.com/rulings/1297/how-does-scoring-work-in-riftbound-particularly-regarding-holding-and-conquering)** — the authoritative ruling behind the "final point can't be a lone conquer" and Hold-timing lines.
- **[Combat rules (Rift Watcher)](https://riftwatcher.com/rules/combat/)** — damage assignment (lethal-to-one-before-the-next) and how "excess damage" is measured.
- **[How damage works in Riftbound (riftboundguide.com)](https://riftboundguide.com/2026/03/29/how-damage-works-in-riftbound/)** — excess/overkill arithmetic used by the Vi trees.
- **[Stun — deals no damage but still needs full lethal (Rift Watcher)](https://riftwatcher.com/rules/stun/)** and **[RiftJudge Q&A](https://app.riftjudge.com/questions)** — three-way confirmation that Stun is damage-prevention, **not** removal (the Vi and Leona corrections).
- **[Keyword glossary (runesandrift.com)](https://runesandrift.com/riftbound-keywords/)**, **[learnriftbound.gg glossary](https://learnriftbound.gg/glossary)**, **[Spiritforged keyword rundown (runesandrift)](https://runesandrift.com/riftbound-spiritforged-keywords/)**, **[Riftbound Wiki glossary (Fextralife)](https://riftbound.wiki.fextralife.com/Glossary)**, **[Rift Watcher — Weaponmaster](https://riftwatcher.com/rules/keywords/weaponmaster/)** / **[Ambush](https://riftwatcher.com/rules/ambush/)** — [Ambush], [Accelerate], [Weaponmaster] (= equip for 1 Power less), [Temporary] (killed before scoring), [Deathknell], [Shield], [Deflect].
- **[Turn order & the scoring phase (runesandrift)](https://runesandrift.com/riftbound-turn-order/)** — places Hold scoring inside the Beginning Phase, after [Temporary] units die.
- **[Spiritforged core rules / patch notes (official, playriftbound.com)](https://playriftbound.com/en-us/news/rules-and-releases/riftbound-core-rules-spiritforged-patch-notes/)** — official Weaponmaster / triggered-ability rulings.
- **[Vex - Apathetic ruling (riftboundfaq.com)](https://www.riftboundfaq.com/cards/vex-apathetic)** — confirms the auto-selected stun is not a "target" (targeting protection can't stop it).

### Per-legend
- **Diana:** [RQ-Vancouver champion deck guide (riftboundguide.com)](https://riftboundguide.com/2026/06/08/riftbound-diana-champion-deck-guide/) · [Diana legend page — text, tier, results (Hextech Analytics)](https://hextechanalytics.com/legends/diana) · [Diana tempo / counter matchup (RiftStorm.gg)](https://riftstorm.gg/blog/diana-counter-riftbound-tempo)
- **Vi:** [Vi champion deck guide (riftboundguide.com)](https://riftboundguide.com/2026/04/08/riftbound-vi-champion-deck-guide/) · [Vi legend page — meta stats (Hextech Analytics)](https://hextechanalytics.com/legends/vi)
- **Azir:** [Token Azir deck tech (Cards Realm)](https://riftbound.cardsrealm.com/en-us/articles/riftbound-deck-tech-token-azir) · [Azir guide (riftbound.gg)](https://riftbound.gg/azir-emperor-of-the-sands-guide/) *(browser-only)* · [Calm/Order Azir deck guide (Rift Mana)](https://riftmana.com/calm-order-azir-emperor-of-the-sands-deck-guide/) *(browser-only)*
- **Lillia:** [Lillia aggro deck tech (Cards Realm)](https://riftbound.cardsrealm.com/en-us/articles/riftbound-deck-tech-lillia-aggro) · [Lillia guide (riftbound.gg)](https://riftbound.gg/lillia-bashful-bloom-guide/) *(browser-only)*
- **Leona:** [Holding Leona deck tech (Cards Realm)](https://riftbound.cardsrealm.com/en-us/articles/riftbound-deck-tech-holding-leona) · [Leona legend page — Tier C / 24.5% WR / 0.7% play (Rift Watcher)](https://riftwatcher.com/legend/leona/) · [Tier list (Hextech Analytics)](https://hextechanalytics.com/tierlist)

> **Bot-walls.** Several community sites (riftbound.gg, mobalytics.gg, riftmana.com, riftdecks.com) return HTTP 403 to
> automated fetches but load normally in a browser — links marked *(browser-only)* are still useful to a human reader;
> they simply couldn't be machine-verified in the 2026-07-10 pass.

### Engine-verified card data
- All card **rules text, Energy/Power costs, and Might** in this document were re-verified against the project's distilled `data/card_behavior.json` — the exact lowercased tokens the game engine pattern-matches — and each keyword against its printed reminder text. Where a community source and the card text disagreed, **the card text wins.**

> **A note on numbers.** Public "tier," "win rate," and "meta share" figures for these
> archetypes come from third-party trackers that update frequently and disagree with each
> other; treat any specific percentage as a snapshot, not a constant. The strategic lines
> in the decision trees are derived from card text and rules and do not depend on those
> numbers.
