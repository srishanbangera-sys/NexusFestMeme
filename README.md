# 🎮 NexusFestMeme

> **Scan. Get rickrolled. Get registered.** 😭

A QR-code prank landing page for **Nexus Fest 2026** — a startup pitch event in Mangalore. Print QR codes around campus labelled _"Scan to claim free attendance"_ and watch the chaos unfold.

---

## 🤔 What Is This?

Students scan the QR code expecting free attendance. Instead, they get:

1. **A fake "Tap to Claim Attendance" screen** — looks totally legit
2. **A meme GIF + audio** — the bait-and-switch reveal
3. **Roast messages** — chat bubbles calling them out, line by line
4. **A CTA to actually register** — redirects to [fest.nexusclubs.in](https://fest.nexusclubs.in)

Built as a single-page, mobile-first HTML file with a Minecraft/voxel aesthetic. No frameworks, no dependencies, no build step.

---

## 🚀 How to Use

### 1. Host the page
Upload all files to any static hosting (GitHub Pages, Vercel, Netlify, or even a simple HTTP server):

```bash
# Local preview
python3 -m http.server 8080
# Open: http://localhost:8080/Nexus%20Fest%20QR%20Landing%20Preview.html
```

### 2. Generate a QR code
Point a QR code to the hosted URL. Print it with a label like:
- _"Scan to claim free attendance"_
- _"Free proxy — limited time only"_
- _"Attendance QR — Scan now"_

### 3. Stick them around campus
Classrooms, canteen, notice boards, library — you know the drill.

### 4. Sit back and watch
Open the browser console to see scan/click analytics logs.

---

## 📁 File Structure

```
NexusFestAD/
├── Nexus Fest QR Landing Preview.html   # The main landing page
├── cat_transparent.gif                   # Meme GIF (transparent background)
├── ReelAudio-46990.mp3                   # Meme audio (loops with GIF)
└── README.md                             # You are here
```

---

## 🎨 Design

- **Minecraft/voxel aesthetic** — dark teal background, pixel grid overlay
- **Fonts** — [Press Start 2P](https://fonts.google.com/specimen/Press+Start+2P) + [VT323](https://fonts.google.com/specimen/VT323) from Google Fonts
- **Wooden signboard** style cards with chunky pixel borders
- **Floating particles** — emeralds 💎, sparkles ✨, blocks 🧱 drifting in the background
- **Responsive** — works on 360px phones, tablets, and desktop (side-by-side layout at 768px+)

---

## ⚙️ Customization

### Change the meme
Replace `cat_transparent.gif` with any GIF. Transparent backgrounds work best.

### Change the audio
Replace `ReelAudio-46990.mp3` with your own audio file. It loops automatically.

### Change the roast text
Edit the `script` array in the `<script>` section:

```js
var script = [
  ["BRO. YOU REALLY THOUGHT. 💀", "big", 2200],
  ["Your custom roast here.", "", 1700],
  // ...
];
```

Each entry is `[text, cssClass, delayMs]`.

### Change the redirect URL
Update `NEXUS_FEST_URL` near the bottom of the script:

```js
var NEXUS_FEST_URL = 'https://fest.nexusclubs.in';
```

### Add analytics
Find the `Analytics` object in the script — replace the `console.log` calls with your tracking endpoint:

```js
var Analytics = {
  trackScan: function() { /* fires on page load */ },
  trackReveal: function() { /* fires on "claim" tap */ },
  trackButtonClick: function() { /* fires on CTA click */ }
};
```

---

## 📱 Compatibility

| Platform | Status |
|---|---|
| Android Chrome | ✅ Tested |
| iOS Safari | ✅ Tested (playsinline) |
| Desktop Chrome/Firefox/Edge | ✅ Tested |
| 360px screens | ✅ Responsive |

---

## 📄 License

Do whatever you want with it. It's a meme page. Go wild. 🤙

---

**Made with 💀 for Nexus Fest 2026, Mangalore**
