NEON RIFT RUNNER — LOOTLOCKER LEADERBOARD BUILD

This is still the original HTML5/JavaScript game. LootLocker is used for online player
sessions, player names, and the global leaderboard. LootLocker does not host the HTML
game files; upload index.html to your existing web host (for example GitHub Pages).

FIRST-TIME LOOTLOCKER SETUP
1. In the LootLocker Web Console, open your Neon Rift Runner game.
2. Open Game Settings / API and copy the Game API Key.
3. Open Systems > Leaderboards and create a PLAYER leaderboard:
   - Name: Neon Rift Runner Global
   - Key: neon_rift_global
   - Direction: Descending (higher scores rank first)
   - Enable Game API writes: ON
   - Overwrite score on submit: OFF (keeps a player's best score)
4. Open index.html in a text editor.
5. Find this line:
   const LOOTLOCKER_GAME_KEY = 'PASTE_GAME_API_KEY_HERE';
   Replace only the placeholder with your Game API Key.
6. If you chose a different leaderboard key, update:
   const LOOTLOCKER_LEADERBOARD_KEY = 'neon_rift_global';
7. Save index.html and upload it to the root of your website.

IMPORTANT KEY SAFETY
- The Game API Key is intended for client/game use in this integration.
- NEVER put a Server API key, Admin API key, x-auth-token, or other secret credential
  into index.html or any browser code.
- Do not send secret keys in chat or publish them in screenshots.

WHAT THIS BUILD DOES
- Starts a LootLocker guest session automatically.
- Stores the guest player identifier in this browser's localStorage so the same browser
  can return to the same guest player.
- Syncs the chosen username to the LootLocker player profile.
- Adds a Global Leaderboard screen showing the top 10 players.
- Submits a run score when the player achieves a new personal best.
- Keeps the existing game, six outfits, shop, coins, and local profile.

LIMITATIONS
- Guest identity is tied to this browser's local storage. Clearing site data or changing
  browsers/devices can make a different guest account.
- Existing coins/outfits/best score remain local to the browser in this first integration.
  Only player name and leaderboard score are online.
- Browser-submitted scores are not cheat-proof. A trusted server-side validation layer
  would be needed before treating scores as competitive or prize-eligible.
- Internet connection and a configured LootLocker Game API Key + leaderboard are required
  for online features. If not configured, the rest of the game still runs locally.

CONTROLS
SPACE, UP ARROW, or tap the game to jump.
