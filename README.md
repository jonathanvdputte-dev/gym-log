# Gym Log

A small installable web app (PWA) for logging a 3-day in-season gym program: sets, reps and weights, with suggestions for the next session, an RPE rating per exercise, a rest timer, a finish checklist, a week and deload view, notes and an editable plan.

**Live app:** https://jonathanvdputte-dev.github.io/gym-log/

## Install on Android
1. Open the link above in Chrome.
2. Tap **Install app** (or ⋮ → **Add to Home screen**).
3. Gym Log now opens full-screen from its own icon and works without signal.

## Your data
- Everything you log stays **on your phone** (browser storage). Nothing is sent to a server, and nothing is stored in this repository.
- **Plan → Backup → Back up now** opens Android's share menu, so you can save the backup to Google Drive or send it to yourself. The app reminds you when your last backup is 2 weeks old.
- Import a backup on a new phone with **Import backup**.
- Clearing the browser's site data for this page deletes the log, so keep a recent backup.

## Rest timer with the screen locked
Allow notifications when the app asks. When you lock your phone during a rest, a notification shows when your next set is due. When the rest is over you get a vibrating alert if Android keeps the app running; otherwise the alert comes as soon as you unlock.

## Files
| File | What it does |
| --- | --- |
| `index.html` | The whole app: program, layout and logic |
| `manifest.webmanifest` | App name, icons and full-screen mode |
| `sw.js` | Offline support; new versions load on the next open |
| `icons/` | App icons |

## Updating
Edit `index.html` and push to `main`. GitHub Pages republishes in about a minute; the app picks up the new version the next time it opens. If you change files other than `index.html`, bump `CACHE` in `sw.js`.
