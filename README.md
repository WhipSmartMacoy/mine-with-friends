# ⛏️ Mine with friends

A turn-based online mining game for two players, each on their own device.

## Getting into a game
0. The first time you open the game, **create your miner**: name, skin tone, hair style and colour, hat style and colour, shirt, pants and shoes. You can change it later with **Edit miner** in the lobby.
1. Enter your name and click **Create lobby**. You'll get a 5-character code.
2. Send the code (or the **Copy invite link** link) to your friend. They enter it and click **Join lobby**.
3. Lobbies hold exactly 2 players. Anyone else who tries the code is told the lobby is full.

Players connect directly browser-to-browser (via [PeerJS](https://peerjs.com)), so no server or account is needed.

## How to play
- Each player is a pixel-art miner. **Walk any time** with WASD / arrow keys (or the on-screen pad on phones). Walking never uses a turn.
- There are two rooms: the **mine** and the **Upgrades room**. Walk through the UPGRADES door in the mine's top wall (and the MINE door at the bottom of the Upgrades room) to switch. Each player moves between rooms on their own.
- Each turn has **5 actions**. Each of these uses one action (press **End turn** or **T** to pass early):
  - **Mine** (mine): face a rock and press **Space** / tap **Mine**. Rocks are random, levels 1–10; green badges are ones you can mine. Success gives gold, XP and the **ore** goes in your bag. A miss cracks the rock, making it easier next time.
  - **Smelt** (🔥 Forge, Upgrades room): 2 ore + 1 Coal → 1 bar (Stone needs no coal and makes Stone Bricks). Smelt one or all you can afford for a single action.
  - **Craft** (⚒️ Anvil, Upgrades room): forge your next pickaxe from bars of its material — Stone ×3, Copper ×3, Iron ×3, Silver/Gold/Emerald ×4, Ruby/Diamond/Mythril ×5.
  - **Buy** (🛒 Upgrade Cart, Upgrades room) with gold: 🍀 Lucky Charm (+15% on 3 swings), 🧨 Dynamite (next swing can't miss), 🥪 Miner's Lunch (half a level of XP), 🪨 Sack of Coal (3 Coal).
- Walking up to the cart, forge or anvil and pressing **Space** / **Use** opens its menu. Looking is free — only confirming an option uses an action.
- The **📊 Stats** panel shows both players' bags and bars, team progress, milestones and the log. On phones the whole game fits on one screen.

## Saving
Each player's progress and the team's total progress are saved in **both** players' browsers. To continue later, the host clicks **Reopen lobby** (same code) and the friend rejoins with that code. If either player's save is further ahead, that one is used. **Export save** downloads a backup.

## Hosting
Served with GitHub Pages: **Settings → Pages**, branch `main`, folder `/ (root)`.
