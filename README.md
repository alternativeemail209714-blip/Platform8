# CRAFT platform (compact deploy build of UPDATE_170)

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

## What's new in 170: TEAM ARENA
17 new team games (Blindle, Oracle, Shiftle, Forbackle, Rangedle, Codedle, Comparable, Shapedle, Fixle, Structle, Colorblindle, Colordle, PIN Breaker, Betweendle, Expandle Race, Word Hunt, Flag Showdown, Category Rush), per-game join time + a Begin-now button, half-height scoreboard, one-row toolbar, Memory starts face-down. Details: `CHANGES_UPDATE_170.md` (inside `app/` after first start). No new environment variables or npm packages. Flag Showdown loads flag pictures from flagcdn.com, like the Flagle game.
