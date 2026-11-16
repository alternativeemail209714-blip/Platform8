# CRAFT platform (compact deploy build of UPDATE_166)

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
1. Upload these files to GitHub (replace the UPDATE_165 files).
2. Render: Build Command `npm install`, Start Command `npm start`. Environment variables are unchanged.
3. The first start prints `[launcher] unpacked N files`, then `[TEAMARENA] Mounted at /teamarena`. Saved settings under `app/data/` are never overwritten.

## What's new in 166: TEAM ARENA polish
Richer graphics for every format, a fairer points scale (new "Points style" setting), and the Malaysia-vs-Indonesia and gift team splits removed. Details: `CHANGES_UPDATE_165.md` (contains the 166 section).
Open it from the HOME page. Press the gear for Host controls: pick a format, how viewers choose a team, and the options.
Full details are in `CHANGES_UPDATE_166.md` (inside the pack, it appears in `app/` after the first start).
No new environment variables and no new npm packages are needed.
