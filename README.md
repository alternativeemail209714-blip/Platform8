# CRAFT platform (compact deploy build of UPDATE_167)

Same 6-file layout as before:

| File | Purpose |
|---|---|
| `package.json` | dependencies + `npm start` |
| `start.js` | launcher: unpacks `app.pack` into `app/` and starts the platform |
| `app.pack` | the entire platform (33 games, compressed) |
| `.env.example` | environment variable reference |
| `.gitignore` | keeps `app/`, `node_modules/`, runtime data out of git |
| `README.md` | this file |

## Deploy (Render)
1. Upload these files to GitHub (replace the UPDATE_166 files).
2. Render: Build Command `npm install`, Start Command `npm start`. Environment variables are unchanged.
3. The first start prints `[launcher] unpacked N files`, then `[TEAMARENA] Mounted at /teamarena`. Saved settings under `app/data/` are never overwritten.

## What's new in 167: TEAM ARENA
Up to 4 teams (Red / Blue / Green / Yellow) in the games that suit it, floating guess windows in every game, settings regrouped into 6 tabs with per-game options, new vector graphics and animations, and fixes for Capture the Word, Boss battle, Sudoku Race, Last Letter Standing and Relay Round. Full list: `CHANGES_UPDATE_167.md` (appears in `app/` after the first start).
No new environment variables and no new npm packages are needed.
