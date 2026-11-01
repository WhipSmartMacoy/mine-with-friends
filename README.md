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
- There are two rooms: the **mine** and the **shop**. Walk through the SHOP door in the mine's top wall (and the MINE door at the bottom of the shop) to switch. Each player moves between rooms on their own.
- **Mining** (in the mine): on your turn, face a rock and press **Space** / tap **Mine**. Rocks are random, levels 1–10; green badges are ones you can mine. Success shatters the rock for gold and XP; a miss cracks it, making it easier next time. Uses your turn.
- **Shopping** (in the shop): on your turn, face an item and press **Space** / tap **Buy**. Uses your turn.
  - **Pickaxe upgrade** – next tier (Wooden → Mythril): reach tougher rocks with better odds.
  - **Lucky Charm** – +15% success on your next 3 swings.
  - **Dynamite** – your next swing can't miss.
  - **Miner's Lunch** – half a level of XP right away.
- The **📊 Stats** panel has both players, team progress, milestones and the log. On phones the whole game fits on one screen with no scrolling.

## Saving
Each player's progress and the team's total progress are saved in **both** players' browsers. To continue later, the host clicks **Reopen lobby** (same code) and the friend rejoins with that code. If either player's save is further ahead, that one is used. **Export save** downloads a backup.

## Hosting
Served with GitHub Pages: **Settings → Pages**, branch `main`, folder `/ (root)`.
