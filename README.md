# Chalk Talk — 6U Baseball Board ⚾

A personal iPad coaching whiteboard for teaching basic baseball to 6-year-olds.
A simplified, personal-use take on tools like Baseball Instincts: drag players
around a field, chalk arrows with your finger, and play back animated
situations so little players can *see* where to go.

Everything is one self-contained web page — no accounts, no server, no App
Store. It runs entirely on the iPad and keeps working offline once installed.

## Features

- **Touch tactical board** — 9 fielders, a batter, 3 bench runners, and a ball,
  all draggable with a finger. Toggle position names on/off.
- **Chalk arrows** — tap DRAW and sketch arrows on the field; UNDO and CLEAR
  to tidy up.
- **Animated plays** — tap STEP + to snapshot the field, move the players, add
  more steps, then press PLAY to watch everyone move.
- **6 built-in tee-ball lessons** — where to stand, run through first, run the
  bases in order, ground ball to first, force at second, and throwing the ball
  in from the outfield. Each comes with a big coaching tip and most are
  animated.
- **My Plays** — save any board setup (including its animation steps) by name
  and pull it up at practice. Stored on the device via localStorage.

## Get it on your iPad

1. **Host the files** (one-time, free): in this GitHub repo go to
   **Settings → Pages**, choose **Deploy from a branch**, pick this branch and
   the `/ (root)` folder, and save. GitHub gives you a URL like
   `https://<username>.github.io/Baseball/`.
2. On the iPad, open that URL in **Safari**.
3. Tap the **Share** button → **Add to Home Screen**.

You now have a Chalk Talk icon on the home screen. It opens fullscreen like a
native app, and the service worker caches everything, so it works at fields
with no signal.

## Files

| File | Purpose |
|------|---------|
| `index.html` | The whole app — markup, styles, and logic in one file |
| `manifest.json` | Web-app manifest (name, icons, fullscreen display) |
| `sw.js` | Service worker: cache-first offline support |
| `icon-180.png` / `icon-192.png` / `icon-512.png` | Home-screen icons |

No build step and no dependencies — edit `index.html` and reload. The built-in
lessons live in the `LESSONS` array in `index.html` if you want to add your own.
