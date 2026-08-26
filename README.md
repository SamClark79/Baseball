# Chalk Talk — 6U Baseball Board ⚾

A personal iPad coaching whiteboard for teaching basic baseball to 6-year-olds.
A simplified, personal-use take on tools like Baseball Instincts: drag players
around a field, chalk arrows with your finger, and play back animated
situations so little players can *see* where to go.

Everything is one self-contained web page — no accounts, no server, no App
Store. It runs entirely on the iPad and keeps working offline once installed.

## Features

- **Touch tactical board** — 10 fielders (standard 6U setup with four
  outfielders: Left Field, Left Center, Right Center, Right Field), a batter,
  two bench crews (three green Base Invaders with antennae and three red
  opposing runners), and a ball, all draggable with a finger. Toggle position
  names on/off.
- **Chalk arrows in six colors** — white, violet, red, blue, green and black
  (yellow is reserved for the ball). Tap DRAW and sketch arrows on the field,
  press and hold DRAW to switch between solid and dotted lines; UNDO and CLEAR
  to tidy up.
- **Ball trails** — press and hold the ball to choose GROUND BALL (dotted),
  FLY BALL (arc), or LINE DRIVE (straight), then drag the ball to where it
  goes and the hit is drawn behind it. Trails always render as a glowing
  Statcast-style tracer in MLB tracker yellow, whatever chalk colour is
  selected — a yellow line on this board always means the ball.
- **Outs box** — a big scoreboard-style box in the corner of the field, sized to
  read from a huddle; tap a dot to set 0-3 outs, tap the lit dot again to back
  off one.
- **Signal band** — a green / yellow / red band across the top; tap a colour to
  light it up, tap it again to clear.
- **Base coaches** — whenever one of your runners (or the batter) is out on the
  field, a coach circle appears in foul ground past first and third. They are
  open circles marked C, and they take on the signal band's colour, so they
  double as the stoplight for a wristband running system.
- **Cones** — tap CONE + to drop a traffic cone on the field for laying out
  drills, drag it anywhere, and press and hold a cone to take it off. A
  CLEAR CONES button appears under CONE + whenever cones are on the field and
  sweeps them all at once. Add as many as you need; they save with the board
  and with named plays.
- **Situations** — one tap sets up the bases for teaching: runner on 1st,
  1st & 2nd, bases loaded, 2nd, 2nd & 3rd, or 3rd — each available as an
  offense drill (your green runners on base) or a defense drill (the other
  team on base), with a coaching tip for each.
- **My lineup** — arrange the fielders the way your team actually plays, then
  save it in the Situations tab; RESET and every Situation use it from then on.
  Position names are off by default and toggle on with NAMES.
- **Animated plays** — tap STEP + to snapshot the field, move the players, add
  more steps, then press PLAY to watch everyone move. Each step also captures
  the chalk drawn at that moment, so arrows appear as the play reaches them
  instead of cluttering earlier steps. Loading a saved play opens it at step 1,
  and PLAY always restarts from the beginning.
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
