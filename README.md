# A Film About Mansi

An interactive, cinematic birthday website, a 2000s-Bollywood "birthday movie" with a candle-wish scene (blow out the candles for confetti and a "Happy 22"), a museum gallery carousel of her photos, letters from alternate universes, a constellation named after her, a maths-teacher chapter, a final movie poster, and a perfumed letter from Deeksha as the closing scene.

Built as a **single static site** (no build step, no npm) so it deploys anywhere in minutes and a song just drops in.

---

## Do these 2 things first

### 1. Check her details
Open `index.html` and near the bottom (inside `<script>`) find:

```js
window.CONFIG = {
  name: "Mansi",
  age: 22,
  releaseDate: "2026",
  musicFile: "audio/song.mp3",
  albumCover: "images/photo1.jpg",   // the spinning record in the player
  trackTitle: "Her Main Theme",      // text shown in "Now Playing"
};
```

Everything is already set for Mansi. Change anything you like here (it updates across the whole site).

### 2. Add the song
Rename your music file to **`song.mp3`** and put it in the **`audio/`** folder, so the path is `audio/song.mp3`. Done, it plays after "Enter The Theatre".
(If you can't rename to `.mp3`, change `musicFile` in CONFIG to your filename instead.)

Optional: swap the little spinning record cover by dropping an image into `images/` and pointing `albumCover` at it (use art you have the rights to).

---

## What's inside
```
birthday-site/
├── index.html      the whole website
├── images/         her 7 photos (photo1 ... photo7)
├── audio/          put song.mp3 here
└── README.md
```

---

## How to deploy (pick ONE)

### Option A, GitHub Pages (free, recommended)
1. Create a new repo on GitHub (e.g. `happy-birthday`).
2. Upload **everything inside this folder**: `index.html`, the `images/` folder, and your `audio/song.mp3`. (On github.com: **Add file, Upload files**, then drag them in. Keep the folder structure.)
3. Go to the repo's **Settings, Pages**.
4. Under "Build and deployment": **Source: Deploy from a branch**, **Branch: `main` / `root`**, then **Save**.
5. Wait about a minute, refresh, your live link appears at the top (like `https://yourname.github.io/happy-birthday/`).

### Option B, Vercel (same host as the reference site)
1. Push this folder to a GitHub repo (as above).
2. Go to vercel.com, **Add New, Project**, import that repo.
3. Framework preset: **Other**. No build command needed. Click **Deploy**.

### Option C, Netlify (drag and drop, no GitHub)
1. Go to app.netlify.com/drop.
2. Drag the **whole `birthday-site` folder** onto the page. Instant live link.

> Add your `audio/song.mp3` **before** deploying (or re-upload after adding it), so the live site has the song.

---

## Good to know
- **Mobile-first**, she'll probably open it on her phone, and it's designed for that.
- Music **never autoplays** before she clicks "Enter The Theatre" (browsers block that anyway, and it's nicer).
- Works fine **with sound off**, there's a mute button in the player.
- **Candles:** tap each candle to blow it out (or the mic button to blow with your breath). When all are out, confetti and "Happy 22" appear.
- The photos are already optimised. To swap any, replace the matching `images/photoN.jpg` (keep the filename).
- Want to edit captions, letters, star messages, fortunes, or Deeksha's letter text? They're in plain arrays/variables near the top of the `<script>` (`EXHIBITS`, `LETTERS`, `STAR_CONTENT`, `FORTUNES`, `LITTLE`, `DEEKSHA_LETTER`), easy to find and change.

Happy building, and happy birthday to Mansi.
