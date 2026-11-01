# ⛏️ Mine with friends

A turn-based online mining game for two players, each on their own device.

## Getting into a game
0. The first time you open the game, **create your miner**: name, skin tone, hair style and colour, hat style and colour, shirt, pants and shoes. You can change it later with **Edit miner** in the lobby.
1. Enter your name and click **Create lobby**. You'll get a 5-character code.
2. Send the code (or the **Copy invite link** link) to your friend. They enter it and click **Join lobby**.
3. Lobbies hold exactly 2 players. Anyone else who tries the code is told the lobby is full.

Players connect directly browser-to-browser (via [PeerJS](https://peerjs.com)), so no server or account is needed.

## How to play
**Co-op, real time.** There are no turns — both players play at the same time as a team. Gold, ore and bars go into one **team stash** you both spend from.

- **Walk** freely with WASD / arrow keys (diagonals too), or the on-screen pad on phones. **Hold** Space / the action button to keep swinging. Two rooms: the **mine** and the **Upgrades room** (walk through the UPGRADES / MINE doors).
- **Mine** (mine): face a rock and press **Space** / tap **Mine**. Rocks are levels 1–10; green badges are ones you can mine. Success gives gold, XP and ore. A miss cracks the rock (easier next time) — and **may disturb an enemy**. Enemies also creep in on their own every so often while someone's in the mine.
- **Fight**: face an enemy and press **Space** / tap **Attack** to strike with your dagger. Enemies get tougher in deeper rock:
  - 🟢 **Pebble Slime** (levels 1–3) · 🦇 **Cave Bat** (4–6, fast) · 💎 **Crystal Golem** (7–10, tough)
  - They chase the nearest miner and hit when next to you. Defeating one drops gold for the team and XP for you.
- **Health**: shown as ❤️ in the top bar. At 0 you're **knocked out** and wake up a few seconds later in the Upgrades room. Health slowly refills while you rest in the Upgrades room.
- **Upgrades room** (all paid from the team stash):
  - 🔥 **Forge** — 2 ore + 1 Coal → 1 bar (Stone needs no coal).
  - ⚒️ **Anvil** — forge your next **pickaxe** or **dagger** from bars of its material (Wooden → Stone → Copper → … → Mythril). Daggers need one bar fewer.
  - 🛒 **Upgrade Cart** — 🧪 Health Potion, 🥪 Miner's Lunch (full health + XP), 🍀 Lucky Charm, 🧨 Dynamite, 🪨 Sack of Coal.
- Each player has their own level, health, pickaxe and dagger. The **📊 Stats** panel shows both players, the team stash, milestones and the log.

## Custom sprites
You can add your own character, ore and station art as PNG sprite sheets — see [`sprites/README.md`](sprites/README.md). Start from `sprites/example-miner.png` and the labelled `sprites/character-template-guide.png`.

## Saving
Each player's progress and the team's total progress are saved in **both** players' browsers. To continue later, the host clicks **Reopen lobby** (same code) and the friend rejoins with that code. If either player's save is further ahead, that one is used. **Export save** downloads a backup.

## Hosting
Served with GitHub Pages: **Settings → Pages**, branch `main`, folder `/ (root)`.
