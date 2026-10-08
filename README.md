# Emberwick Academy Survivors: How to play

*The Hollow Moon has risen. Defend the academy grounds, together.*

A 2-player online co-op survival game in the style of *Vampire Survivors*, set at **Emberwick Academy**, an original
school of magic. The whole game is one file: `index.html`. You only move: your spells cast themselves. Survive the
endless night on the castle grounds, collect **Crowns**, study permanent enchantments in the **Library of Enchantments**,
enrol new students, and evolve your spells by opening treasure chests.

Play online: **https://geldarb.github.io/coop-survivor/** (or open `index.html` directly).

## Starting a game
1. Open the game in a recent desktop browser (Chrome, Edge, Firefox or Safari). Online play needs an internet
   connection. The networking library (PeerJS) loads from a CDN, and the free public PeerJS server introduces the
   two browsers to each other.
2. Type your name. Optionally pick a hero with **Students**, buy enchantments in the **Library of Enchantments**, and
   browse the **Grimoire**.
3. **Host game**: you get a 4-character **room code** (e.g. `8UTY`). Send it to your friend.
4. Your friend opens the same game, types the code next to **Join**, and clicks **Join**.
5. In the lobby, each of you sees the other's hero. You can still **Change** hero or visit the **Library** there.
   When ready, the host clicks **Start game**.
6. **Solo** starts a single-player run right away.

Tip: `...?join=CODE` at the end of the game URL pre-fills the code for your friend.

## Controls
| Action | Keys |
|---|---|
| Move | **W A S D** or **Arrow keys** (or click/touch and drag anywhere) |
| Pick a level-up card | Click a card, or press **1 / 2 / 3 / 4** |
| Reroll the level-up cards | **R** or the Reroll button (needs Reroll Scrolls) |
| Claim a treasure chest | **Enter / Space / E** or the Claim button |
| Pause (Solo only) | **Esc** or **P** |

Spells aim and cast automatically. Hexed Daggers fly in the direction you last moved.

## Rules
- In co-op the host has a **blue** ring and name, the guest **orange**. Both players can pick the same hero; the
  ring colour and name tell you apart.
- Defeated creatures drop **XP gems** (blue, then green, then red). XP is **shared**: when the team levels up, **each
  player picks their own card**. The game pauses until both have picked.
- **Crowns** (single coins and purses from elites) drop now and then. Each player keeps the Crowns they pick up.
  Red healing draughts restore HP.
- The night grows darker over time: bat swarms and spider broods, and a **Dark Warlock** elite about every 75 seconds.
  Every 4th elite is an **Ember Drake**, a great boss.
- **Going down:** at 0 HP you become a **ghost**. Your partner revives you by standing next to your ghost for
  ~3 seconds. With the *Second Life Sigil* enchantment you rise again on the spot once per run. The run ends when both
  players are down ("The night prevails").

## Treasure chests and evolutions
- Every elite drops **one treasure chest per player**, marked with a beam of light, your colour ring, and an edge
  arrow when it's off-screen. Only its owner can open it for the first 25 seconds. The **Ember Drake** drops
  **great chests**.
- Opening a chest pauses the run and shows what's inside:
  - **Evolution:** if one of your spells is at **level 6 (max)** and you hold its **paired item** (any level), the spell
    **evolves** into a stronger form with a new effect. A great chest can evolve up to 3 spells at once.
  - Otherwise the chest gives 1 random upgrade (sometimes 3 or 5; luck helps) plus some Crowns.
- Recipes appear on the level-up cards ("Evolves into ... at Lv 6 with ...") and in the **Grimoire**. A toast tells
  you when a spell is ready to evolve.

## Spells (up to 6 per player, each up to level 6)
| Spell | What it does | Paired item | Evolution | Evolved effect |
|---|---|---|---|---|
| Spark Bolt | Bolts at the nearest enemy | Tome of Swiftcasting | **Arc Lance** | Faster golden bolts with more pierce; every hit chains lightning to 3 nearby enemies |
| Hexed Daggers | Piercing daggers the way you face | Swiftwind Quill | **Crimson Fangs** | Daggers fly out and return, cutting twice, and make enemies bleed |
| Orbiting Spellbooks | Books circle you | Sandglass of Ages | **Whirling Library** | An extra, larger tome; wider orbit, +50% damage, hurls enemies away |
| Warding Circle | Damaging, repelling rune circle | Heartstone Amulet | **Soulward Sanctum** | Wider; slows enemies inside by 40% and drains life to heal you |
| Lightning Charm | Strikes random nearby enemies | Seer's Crystal Orb | **Tempest Crown** | +2 strikes; each strike leaves burning ground |
| Enchanted Broom | Spinning brooms in a high arc | Seven-League Boots | **Cyclone Besom** | Huge brooms with unlimited pierce that whip up cyclones, pulling enemies in |
| Fire Wand | Exploding fireballs | Ember Ring | **Phoenix Staff** | Bigger blasts that burst into 5 embers which set enemies alight |
| Frost Shard | Ice shards that chill (-50% speed) | Elixir of Renewal | **Winter's Heart** | Freezes enemies solid for 1.2 s; shards shatter into 3 splinters |
| Will-o'-Wisps | Homing wisps | Lodestone Charm | **Lantern Host** | Wisps never fade on hit, and every kill sparks a new wisp |
| Thornseed Pouch | Bramble patches that slow and cut | Ironbark Cloak | **Elderwood Grove** | Bigger groves that root enemies and creep after the nearest foe |

## Items (up to 6 per player, level 5 max unless noted)
| Item | Per level |
|---|---|
| Tome of Swiftcasting | -8% spell cooldowns |
| Swiftwind Quill | +10% projectile speed |
| Sandglass of Ages | +10% spell duration and range |
| Heartstone Amulet | +20 max HP |
| Seer's Crystal Orb | +8% spell area |
| Seven-League Boots | +10% move speed |
| Ember Ring | +10% damage |
| Elixir of Renewal | +0.4 HP per second |
| Lodestone Charm | +30% pickup radius |
| Ironbark Cloak | -1 damage taken per hit |
| Echo Prism (max 2) | +1 projectile / book / strike for every spell |

When every slot is full and maxed, level-ups offer **Pouch of Crowns** (+25 Crowns) or a **Healing Draught** (+40 HP).

## Students and faculty
Robe colour shows the house. Achievement-locked heroes can also be bought outright.

| Hero | House | Starting spell | Perk | Unlock |
|---|---|---|---|---|
| Wren Ashby | Emberfox | Fire Wand | +15% spell damage | Free |
| Marin Tidewell | Tidecrest | Frost Shard | +20% projectile speed, +10% duration | Free |
| Bram Thornley | Thornvale | Thornseed Pouch | +30 max HP, +0.3 HP/s | Free |
| Isolde Vey | Duskmoth | Spark Bolt | -10% spell cooldowns | Free |
| Pip Larkin | Emberfox | Hexed Daggers | +15% move speed | 400 Crowns |
| Nyx Hollowell | Duskmoth | Will-o'-Wisps | +60% pickup radius, +10% XP | 600 Crowns |
| Cass Ironwood | Thornvale | Enchanted Broom | +3% damage per team level | 800 Crowns |
| Tobias Reedwater | Tidecrest | Lightning Charm | +15% area, +10% duration | 1000 Crowns |
| Old Fennick (caretaker) | Faculty | Random spell | +50% luck, +25% Crowns | Evolve any spell, **or** 1200 Crowns |
| Prof. Elowen Thistle | Faculty | Warding Circle | +40 max HP, +1 armour | Survive 5:00, **or** 1500 Crowns |
| Archmage Corvin Starling | Faculty | Orbiting Spellbooks | +1 projectile for every spell, +10% damage | Defeat an Ember Drake, **or** 3000 Crowns |

The houses are **Emberfox** (orange, the fox), **Tidecrest** (teal, the wave), **Thornvale** (green, the oak) and
**Duskmoth** (violet, the moth), plus the **Faculty**.

## Crowns and saving progress
At the end of every run, each player earns Crowns:
**25 per minute survived + 1 per 10 of your kills + 3 per team level + the Crowns you picked up**, multiplied by your
Coin-Charm bonus. The game-over screen shows the breakdown.

Crowns, enchantments, unlocked heroes, Grimoire discoveries and your best run are saved **in your own browser**
(localStorage). In co-op, each player keeps their own save; your hero and enchantments are sent to the host when the
game starts. Clearing site data or using a private-browsing window resets the save.

**Saves from the previous version carry over.** Your gold becomes Crowns, PowerUps become the matching enchantments,
and each unlocked hero becomes the academy hero with the same starting spell and perk:

| Old hero | New hero |
|---|---|
| Arcanist | Isolde |
| Rogue | Pip |
| Paladin | Bram |
| Berserker | Cass |
| Magnetist | Nyx |
| Stormcaller | Tobias |
| Gambler | Old Fennick |
| Pyromancer | Prof. Elowen |

## Library of Enchantments (permanent, bought on the main menu)
Each rank costs the base price × the rank number (e.g. Runes of Might costs 200, 400, 600, 800, 1000).
**Refund all** (click twice) gives back everything you spent, so you can re-spec any time.

| Enchantment | Per rank | Ranks | Base price |
|---|---|---|---|
| Runes of Might | +5% damage | 5 | 200 |
| Warding Weave | -1 damage taken per hit | 3 | 600 |
| Vital Draught | +10% max HP | 3 | 200 |
| Mending Charm | +0.1 HP/s | 5 | 200 |
| Quickened Casting | -2.5% spell cooldowns | 2 | 900 |
| Expansive Sigils | +5% spell area | 2 | 300 |
| Swift Glyphs | +10% projectile speed | 2 | 300 |
| Lingering Hexes | +10% duration/range | 2 | 300 |
| Fleetfoot Charm | +5% move speed | 2 | 300 |
| Lodestone Lore | +25% pickup radius | 2 | 300 |
| Fortune's Favour | +10% luck (4th card, better chests, more drops) | 3 | 600 |
| Scholar's Insight | +3% XP | 5 | 900 |
| Coin-Charm | +10% Crowns earned | 5 | 200 |
| Reroll Scrolls | +1 level-up reroll per run | 3 | 400 |
| Head Start | Starting spell begins at level 2 | 1 | 1500 |
| Second Life Sigil | Rise again once per run (50% HP) | 1 | 2500 |
| Echoing Incantation | +1 projectile / book / strike for every spell | 1 | 3000 |

## Creatures of the Hollow Moon
| Creature | Role |
|---|---|
| Hollow Imp | Basic chaser |
| Gloom Bat | Fast; comes in circling swarms |
| Giant Spider | Quick hunter; bursts out in broods |
| Cursed Armour | Slow, very tough tank |
| Wraith | Drifts straight through the horde, weaving |
| Goblin Hexer | Ranged caster: keeps its distance and flings slow hex bolts (dodge them!) |
| Dark Warlock | Elite: rings of hex orbs plus aimed volleys. Drops a chest for each player |
| Ember Drake | Great boss (every 4th elite): fans of fireballs. Drops great chests |

## Grimoire
The **Grimoire** on the main menu lists every spell, item, evolution and creature, plus the houses. Things you
haven't found yet are greyed out. Evolution names stay hidden until you discover them, but their recipes are always
shown.

## Troubleshooting online play
- **"Room not found"**: check the code, and make sure the host still has the lobby open.
- **"Could not connect to the host (timed out)"**: this is a peer-to-peer (WebRTC) game. A few networks block it,
  such as some corporate or school firewalls and some mobile carriers (strict/symmetric NAT). PeerJS falls back to
  its free public relay, but that relay isn't guaranteed. Try another network, or swap who hosts.
- If either player closes the tab or loses connection for ~7 seconds, both return to the menu with a message.
- Keep the host's tab visible if you can. Browsers throttle background tabs.

*Emberwick Academy and all its characters, houses, spells and creatures are original to this game.*
