# ⛏️ Mine with friends

A turn-based online mining game for two players, each on their own device.

## Getting into a game
0. The first time you open the game, **create your miner**: name, skin tone, hair style and colour, hat style and colour, shirt, pants and shoes. You can change it later with **Edit miner** in the lobby.
1. Enter your name and click **Create lobby**. You'll get a 5-character code.
2. Send the code (or the **Copy invite link** link) to your friend. They enter it and click **Join lobby**.
3. Lobbies hold exactly 2 players. Anyone else who tries the code is told the lobby is full.

Players connect directly browser-to-browser (via [PeerJS](https://peerjs.com)), so no server or account is needed.

## How to play
**Co-op, real time.** Both players play at the same time as a team. Gold, ore and bars go into one **team stash**.

### The world
- The **overworld** is 12 × 12 rooms (each 15 × 15 tiles) joined into one big map — no doors, just walk off the edge of a screen into the next. Grass, trees, lakes, boulders and roads. The **mini-map** (top-right) shows where you and your teammate are.
- **Home base** (centre): your cottage. You start here, wake up here after being knocked out, and slowly heal while you're home.
- **Shop** (one room east of home): the 🛒 Upgrade Cart, 🔥 Forge and ⚒️ Anvil stand outdoors.
- **Mine entrance** (one room west of home): walk into the cave mouth to go down to **depth 1**.

### The mine
- Each depth is its own level with rocks and enemies. Climb the **ladder** in the top wall to go back up.
- Mining a rock successfully has a **rare chance to open a tunnel** down to the next depth — 7% at depth 1, getting rarer the deeper you go. Walk into the hole to descend.
- **Deeper = tougher**: rock levels and enemies scale with depth, and it gets darker.
- **Mine**: face a rock and press **Space** / tap **Mine**. A miss cracks the rock and may disturb an enemy; enemies also creep in on their own now and then.
- **Fight**: face an enemy and press **Space** / tap **Attack** (dagger). 🟢 Pebble Slime · 🦇 Cave Bat · 💎 Crystal Golem.

### Controls & gear
- Walk with WASD / arrows (diagonals too) or the on-screen joystick on phones. Hold Space / the action button to keep swinging.
- **Health** ❤️: at 0 you're knocked out and wake at home base.
- **Shop**: Forge (2 ore + 1 Coal → 1 bar), Anvil (forge your next **pickaxe** or **dagger** from bars), Cart (🧪 Potion, 🥪 Lunch, 🍀 Charm, 🧨 Dynamite, 🪨 Coal).

## Custom sprites
You can add your own character, ore and station art as PNG sprite sheets — see [`sprites/README.md`](sprites/README.md). Start from `sprites/example-miner.png` and the labelled `sprites/character-template-guide.png`.

## Saving
Each player's progress and the team's total progress are saved in **both** players' browsers. To continue later, the host clicks **Reopen lobby** (same code) and the friend rejoins with that code. If either player's save is further ahead, that one is used. **Export save** downloads a backup.

## Hosting
Served with GitHub Pages: **Settings → Pages**, branch `main`, folder `/ (root)`.
