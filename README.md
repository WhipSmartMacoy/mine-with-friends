# ⛏️ Mine with friends

A turn-based online mining game for two players, each on their own device.

## Getting into a game
1. Enter your name and click **Create lobby**. You'll get a 5-character code.
2. Send the code (or the **Copy invite link** link) to your friend. They enter it and click **Join lobby**.
3. Lobbies hold exactly 2 players. Anyone else who tries the code is told the lobby is full.

Players connect directly browser-to-browser (via [PeerJS](https://peerjs.com)), so no server or account is needed.

## How to play
- Players take turns, and you can only act on your own turn.
- Pick a rock (levels 1–10) to mine. The game decides in the background if you succeed. Your odds depend on your pickaxe's power compared to the rock's level.
- Success earns gold and XP (10% chance of a double haul). A failed swing still gives a little XP.
- Level up your miner to unlock higher rocks, and spend gold to upgrade your pickaxe (Wooden → Mythril). Upgrading doesn't use your turn.
- The Team panel tracks your combined progress and shared milestones.

## Saving
Each player's progress and the team's total progress are saved in **both** players' browsers. To continue later, the host clicks **Reopen lobby** (same code) and the friend rejoins with that code. If either player's save is further ahead, that one is used. **Export save** downloads a backup.

## Hosting
Served with GitHub Pages: **Settings → Pages**, branch `main`, folder `/ (root)`.
