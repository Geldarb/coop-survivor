# Co-op Survivors – How to play

A 2-player online co-op survival game in the style of *Vampire Survivors*, packed into one file: `index.html`.
You only move. Your weapons fire on their own. Survive the endless, escalating horde together.

## Starting a game
1. Open `index.html` in a recent desktop browser (Chrome, Edge, Firefox or Safari). You need an internet
   connection for online play. The networking library (PeerJS) loads from a CDN, and the free public PeerJS
   server introduces the two browsers to each other.
2. Type your name (optional).
3. **Host game**: you get a 4-character **room code** (e.g. `8UTY`). Send it to your friend.
4. Your friend opens the **same `index.html`** on their computer (send them the file), types the code
   into the box next to **Join**, and clicks **Join**.
5. When the host sees "*Name* joined!", the host clicks **Start game**.
6. **Solo** starts a single-player run right away. It's good for practising or testing.

Tip: if you host the file somewhere, `index.html?join=CODE` pre-fills the code for your friend.

## Controls
| Action | Keys |
|---|---|
| Move | **W A S D** or **Arrow keys** (or click/touch and drag anywhere) |
| Pick a level-up upgrade | Click a card, or press **1 / 2 / 3** |
| Pause (Solo only) | **Esc** or **P** |

Weapons aim and fire automatically. Throwing Knives fly in the direction you last moved.

## Rules
- **Blue = host (Magic Bolt start)**, **Orange = guest (Throwing Knives start)**.
- Kill enemies to drop **XP gems** (blue → green → red for bigger values). Walk near a gem to pull it in.
  XP is **shared**: when the team levels up, **both players pick their own upgrade (1 of 3)**. The game pauses
  until you have both picked.
- Red orbs with a white cross **heal 30 HP**.
- Enemies get stronger and more numerous over time. Watch out for **swarms** of bats closing in from every side,
  and an **Elite** boss about every 75 seconds. Elites drop a pile of XP and a heal.
- **Going down:** at 0 HP you turn into a **ghost**. Your partner revives you by standing next to your ghost for
  ~3 seconds (you come back with 50% HP). An arrow at the screen edge always points to your partner.
  The run ends when **both** players are down. You then see a stats screen, and either player can click **Play again**.

## Weapons (up to 4 per player, each up to level 6)
| Weapon | What it does |
|---|---|
| Magic Bolt | Fires at the nearest enemies. More bolts and pierce as it levels. |
| Throwing Knives | Fans of piercing knives in your movement direction. |
| Orbit Blades | Blades circle around you and slice anything they touch. |
| Holy Aura | A ring that constantly damages and pushes back nearby enemies. |
| Thunder | Lightning strikes random enemies near you, with splash damage. |

## Passives (up to level 5)
Swift Boots (move speed), Vitality (max HP), Power Rune (damage), Haste (cooldowns), Magnet (pickup radius),
Regeneration (HP/sec), Armor (less damage per hit).

## Enemies
Ghoul (basic chaser) · Bat (fast, comes in swarms) · Brute (slow and tanky, appears after 1:30) · Elite (boss with a crown).

## Troubleshooting online play
- **"Room not found"**: check the code, and make sure the host still has the lobby open.
- **"Could not connect to the host (timed out)"**: this is a peer-to-peer (WebRTC) game. A few networks block it,
  such as some corporate or school firewalls and some mobile carriers (symmetric NAT). PeerJS falls back to its free
  public TURN relay, but that relay isn't guaranteed. Try another network (e.g. a home Wi-Fi or phone hotspot), or try
  with the other person hosting.
- If either player closes the tab or loses connection for ~7 seconds, both players see a message and return to the menu.
- Keep the host's tab visible if you can. Background tabs are throttled by browsers. The game keeps simulating in the
  background, but at a lower rate.
