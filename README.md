# 🎮 MOOD SWING — Arcade

> Bure mood ko harao. Achhe wale ko maaro, bure wale ko chhodo. 😎

**MOOD SWING** ek desi, meme-themed whack-a-mole arcade game hai — single HTML file, zero dependencies, aur 70+ famous Indian meme voices ke saath. Double-click karo aur khelna shuru karo.

---

## ✨ Features

### 🎯 Gameplay
- **3 hand-designed levels** — har level ka apna identity aur difficulty curve:
  | Level | Name | Vibe |
  |---|---|---|
  | 1 | CHAI & CHILL | Aaram se shuruat, bad characters kam |
  | 2 | STREAK RUSH | Tez spawns, streak pe time bonus |
  | 3 | TOTAL CHAOS | Full mayhem, double spawns, zyada bad characters |
- **👑 Boss Round** — 3 level ke baad Mood Monster se ladai, **3 phases** (Calm → Enraged → Meltdown), har phase ke saath naya look, tez spawns aur taunts
- **✨ Gold Mole** — chamakdar mole, 5× points, alag halo + sound
- **🎁 Power-ups** — Freeze, Bomb, Double Points, Extra Life
- **Streak system** — combo multiplier + milestone rewards
- Progressive difficulty — level ke andar bhi dheere-dheere badhti hai

### 🔊 Audio — 73 comedy voice clips
- **Famous Indian voices:** Modi Ji ("Wah", "Sab Changasi", "Rona band kijiye"), Rahul Gandhi ("Khatam", "Maja aaya", "Tata Good Bye"), Arnab "Kuch Bhi", Bhaiya Ji, Hindustani Bhau, Baklol, "Kehna Kya Chahte Ho", "Bade Harami Ho Beta", "Choti Bacchi Ho Kya", Aap Kon, Namaste Billi, Indian Rizz, Tamatar, Dhinchak Pooja, aur bahut kuch
- **Context-aware random sounds** — har event (hit, miss, streak, win, boss) ka apna pool; sahi jagah pe sahi awaaz, anti-repeat ke saath
- **Smart audio engine** — 4-voice cap, priority ducking, debounce, smooth fades → koi sound overlap/conflict nahi
- **Dynamic music** — level aur combo ke saath BPM/intensity badhti hai
- **Brand sound layer** — har hit/miss pe wahi signature chime (game ki identity)

### 🎨 Visuals & Motion
- Hand-drawn cartoon SVG characters (photo/pixel art nahi)
- 3D arena plate, depth wale pits, neon rims, per-character accent colours
- Impact zoom-punch, chromatic split, 12 speed-lines, squash & stretch, comic word pops ("BONK!", "POW!")
- Gold halo + sparkles, boss rage aura, CRT scanlines, combo vignette
- Responsive canvas with devicePixelRatio support

### 📱 Mobile-ready & Deploy-ready
- Portrait/landscape, notch safe-areas, chhote phones ke liye optimized layout — board kabhi cut nahi hota
- Auto-pause when tab is hidden, keyboard controls (Space = hit, Esc/P = pause, M = mute)
- Progress save (best score + unlocked level) in `localStorage`
- Safe boot with friendly error screen, first-gesture audio unlock
- PWA meta tags, inline SVG favicon, installable

---

## 🚀 Play karo

### Option 1 — Direct (sabse aasan)
1. Is repo ko download/clone karo.
2. `index.html` ko double-click karo — browser me game chal jayega.
3. **`sounds/` folder ko `index.html` ke saath rakhna zaroori hai** (warna audio nahi aayega).

### Option 2 — Local server (recommended)
```bash
python -m http.server 8000
# phir browser me kholo: http://localhost:8000
```

### Option 3 — Deploy
Pure static files hain — kisi bhi host pe daalo: **GitHub Pages, Netlify, Vercel, Cloudflare Pages** ya koi bhi static server. Koi build step nahi, koi npm dependency nahi.

> **GitHub Pages:** Repo → Settings → Pages → Source: `main` branch / root → Save. Site `https://<username>.github.io/mood-swing/` pe milega.

---

## 📁 Structure

```
mood-swing/
├── index.html      # Poori game (HTML + CSS + JS, ~111 KB)
├── sounds/         # 88 MP3 files (73 active in sound bank)
└── README.md       # Ye file
```

---

## 🎮 Controls

| Action | Desktop | Mobile |
|---|---|---|
| Character maaro | Mouse click | Tap |
| Pause | `Esc` / `P` / ❚❚ button | ❚❚ button |
| Mute | `M` / 🔊 button | 🔊 button |
| Start / Next | `Enter` / `Space` | Button tap |

---

## 🛠️ Tech details

- Vanilla **HTML5 Canvas 2D** + Web Audio API (synth fallback ke saath)
- Audio playback `HTMLAudioElement` se — `file://` pe bhi kaam karta hai
- Single-file architecture — koi framework, bundler ya external CDN nahi
- Pre-rendered board cache → smooth performance (~1–2 ms/frame)

### Dev hook
Console me `window.MoodSwing` se state inspect aur levels test kar sakte ho:
```js
MoodSwing.startBoss();   // seedha boss
MoodSwing.step(1/60);    // ek frame manually chalao
MoodSwing.state          // poora game state
```

---

## ⚠️ Sound credits

Meme sound clips **MyInstants** (myinstants.com) se source kiye gaye hain aur personal/local entertainment ke liye hain. Agar game ko commercially release karna hai to clips ki licensing/permissions check kar leni chahiye.

---

## 💛 Banaya gaya

Desi meme culture ke naam. Haso, khelo, mood swing karo. 🎯

> "Aaj ka mood tumhara." 👑
