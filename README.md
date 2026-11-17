# CRAFT platform (compact deploy build of UPDATE_168)

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

## What's new in 168: TEAM ARENA
Guess panel no longer overlaps the games, cute bosses, redesigned Tug of War (worldwide trivia), Capture the Word and Last Letter Standing, scrolling/aligned settings with every game's options visible, and a 🎮 game picker in the toolbar. Details: `CHANGES_UPDATE_168.md` (inside `app/` after first start). No new environment variables or npm packages.
