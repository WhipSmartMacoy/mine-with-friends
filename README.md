# ⛏️ Mine with friends

A turn-based mining game for two players sharing one screen.

## How to play
- Players take turns. On your turn, pick a rock (levels 1–10) to mine.
- The game decides in the background if you succeed. Your odds depend on your pickaxe's power compared to the rock's level.
- Success earns gold and XP (and there's a 10% chance of a double haul). A failed swing still gives a little XP.
- Level up your miner to unlock higher rocks, and spend gold to upgrade your pickaxe (10 tiers, Wooden → Mythril). Upgrading doesn't use your turn.
- The Team panel tracks your combined progress and shared milestones.

## Saving
Each player's progress and the team's total progress save automatically in the browser (localStorage). Use **Export save** / **Import save** to move a game to another device.

## Hosting on GitHub Pages
1. Push this folder to a GitHub repository.
2. Go to **Settings → Pages**, pick the `main` branch and `/ (root)` folder, then save.
3. Your game will be live at `https://<your-username>.github.io/<repo-name>/`.
