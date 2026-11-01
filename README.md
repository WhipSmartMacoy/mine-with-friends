# ⛏️ Mine with friends

A turn-based online mining game for two players, each on their own device.

## Getting into a game
1. Enter your name and click **Create lobby**. You'll get a 5-character code.
2. Send the code (or the **Copy invite link** link) to your friend. They enter it and click **Join lobby**.
3. Lobbies hold exactly 2 players. Anyone else who tries the code is told the lobby is full.

Players connect directly browser-to-browser (via [PeerJS](https://peerjs.com)), so no server or account is needed.

## How to play
- Each player is a pixel-art miner in a shared mine room. **Walk any time** with WASD / arrow keys (or the on-screen pad on phones). Walking never uses a turn.
- The room is scattered with random rocks, levels 1–10. Each rock shows its level: green means you can mine it, red means it's still too tough.
- On **your turn**, walk up to a rock, face it and press **Space** (or click/tap the rock). Mining uses your turn.
- The game decides in the background if you succeed, based on your pickaxe vs. the rock's level. Success shatters the rock for gold and XP, and a new random rock appears. A miss cracks the rock, making it easier next time.
- Level up to reach higher rocks, and spend gold on pickaxe upgrades (Wooden → Mythril). Upgrading doesn't use your turn.
- The Team panel tracks combined progress and shared milestones.

## Saving
Each player's progress and the team's total progress are saved in **both** players' browsers. To continue later, the host clicks **Reopen lobby** (same code) and the friend rejoins with that code. If either player's save is further ahead, that one is used. **Export save** downloads a backup.

## Hosting
Served with GitHub Pages: **Settings → Pages**, branch `main`, folder `/ (root)`.
