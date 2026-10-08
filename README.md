# Co-op Survivors – How to play

A 2-player online co-op survival game in the style of *Vampire Survivors*, packed into one file: `index.html`.
You only move. Your weapons fire on their own. Survive the endless, escalating horde together, earn **gold**, and
spend it on permanent **PowerUps** and new **characters**.

Play online: **https://geldarb.github.io/coop-survivor/** (or open `index.html` directly).

## Starting a game
1. Open the game in a recent desktop browser (Chrome, Edge, Firefox or Safari). Online play needs an internet
   connection. The networking library (PeerJS) loads from a CDN, and the free public PeerJS server introduces the
   two browsers to each other.
2. Type your name, then pick a hero with **Characters** and buy upgrades with **PowerUps** (optional).
3. **Host game**: you get a 4-character **room code** (e.g. `8UTY`). Send it to your friend.
4. Your friend opens the same game, types the code next to **Join**, and clicks **Join**.
5. In the lobby, each of you sees the other's hero. You can still **Change** hero or buy PowerUps there.
   When ready, the host clicks **Start game**.
6. **Solo** starts a single-player run right away.

Tip: `...?join=CODE` at the end of the game URL pre-fills the code for your friend.

## Controls
| Action | Keys |
|---|---|
| Move | **W A S D** or **Arrow keys** (or click/touch and drag anywhere) |
| Pick a level-up upgrade | Click a card, or press **1 / 2 / 3 / 4** |
| Pause (Solo only) | **Esc** or **P** |

Weapons aim and fire automatically. Throwing Knives fly in the direction you last moved.

## Rules
- In co-op the host has a **blue** ring and name, the guest **orange**. Both players can pick the same hero; the
  ring colour and name tell you apart.
- Kill enemies to drop **XP gems** (blue → green → red). XP is **shared**: when the team levels up, **each player
  picks their own upgrade**. The game pauses until both have picked.
- **Gold coins** (and coin bags from Elites) drop now and then. Each player keeps the coins they pick up.
  Red orbs with a white cross heal 30 HP.
- Enemies grow stronger over time. Watch for bat **swarms**, and an **Elite** boss about every 75 seconds.
- **Going down:** at 0 HP you become a **ghost**. Your partner revives you by standing next to your ghost for
  ~3 seconds. If you own the *Revival* PowerUp, you get back up on the spot once per run. The run ends when both
  players are down.

## Gold and saving progress
At the end of every run, each player earns gold:
**25 per minute survived + 1 per 10 of your kills + 3 per team level + the coins you picked up**, multiplied by your
Greed bonus. The game-over screen shows the breakdown.

Gold, PowerUps, unlocked characters and your best run are saved **in your own browser** (localStorage). In co-op,
each player keeps their own save. Your bonuses are sent to the host when the game starts, so they apply to your
hero. Clearing site data / private-browsing windows reset the save.

## Characters
| Hero | Starting weapon | Perk | Unlock |
|---|---|---|---|
| Arcanist | Magic Bolt | -10% weapon cooldowns | Free |
| Rogue | Throwing Knives | +15% move speed | Free |
| Paladin | Holy Aura | +40 max HP, +1 armour (tanky) | Free |
| Berserker | Battle Axe | +3% damage per team level (scales) | 500 gold |
| Magnetist | Orbit Blades | +60% pickup radius, +10% XP | 600 gold |
| Stormcaller | Thunder | +15% area, +10% duration | 900 gold |
| Gambler | Random weapon | +50% luck, +25% gold | 1200 gold |
| Pyromancer | Fire Wand | +15% damage, +20% projectile speed | Survive 5:00 in any run, **or** 1500 gold |

## PowerUps (permanent, bought on the main menu)
Each rank costs more: the base price × the rank number (e.g. Might costs 200, 400, 600, 800, 1000).
**Refund all** (click twice) gives back everything you spent, so you can re-spec any time.

| PowerUp | Per rank | Ranks | Base price |
|---|---|---|---|
| Might | +5% damage | 5 | 200 |
| Armour | -1 damage taken per hit | 3 | 600 |
| Max Health | +10% max HP | 3 | 200 |
| Recovery | +0.1 HP/s | 5 | 200 |
| Cooldown | -2.5% weapon cooldowns | 2 | 900 |
| Area | +5% weapon area | 2 | 300 |
| Speed | +10% projectile speed | 2 | 300 |
| Duration | +10% projectile duration/range | 2 | 300 |
| Move Speed | +5% move speed | 2 | 300 |
| Magnet | +25% pickup radius | 2 | 300 |
| Luck | +10% luck (chance of a 4th level-up choice, more coins and heals) | 3 | 600 |
| Growth | +3% XP from gems you collect | 5 | 900 |
| Greed | +10% gold earned | 5 | 200 |
| Revival | Revive yourself once per run (50% HP) | 1 | 2500 |
| Amount | +1 projectile / blade / strike for every weapon | 1 | 3000 |

## Weapons (up to 5 per player, each up to level 6)
| Weapon | What it does |
|---|---|
| Magic Bolt | Fires at the nearest enemies. More bolts and pierce as it levels. |
| Throwing Knives | Fans of piercing knives in your movement direction. |
| Orbit Blades | Blades circle around you and slice anything they touch. |
| Holy Aura | A ring that constantly damages and pushes back nearby enemies. |
| Thunder | Lightning strikes random enemies near you, with splash damage. |
| Battle Axe | Heavy axes hurled in an arc that pierce many enemies. |
| Fire Wand | Fireballs at random enemies that explode on impact. |

In-run passives from level-ups: Swift Boots, Vitality, Power Rune, Haste, Magnet, Regeneration, Armor.

## Troubleshooting online play
- **"Room not found"**: check the code, and make sure the host still has the lobby open.
- **"Could not connect to the host (timed out)"**: this is a peer-to-peer (WebRTC) game. A few networks block it,
  such as some corporate or school firewalls and some mobile carriers (strict/symmetric NAT). PeerJS falls back to
  its free public relay, but that relay isn't guaranteed. Try another network, or swap who hosts.
- If either player closes the tab or loses connection for ~7 seconds, both return to the menu with a message.
- Keep the host's tab visible if you can. Browsers throttle background tabs.
