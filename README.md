# Спасибо за доверие — Gratitude Page

A personal, cinematic thank-you site built with React + Tailwind + Framer Motion.

---

## 🚀 Quick Start

```bash
npm install
npm run dev
```

Then open: http://localhost:5173

---

## 🏗️ Build for Production

```bash
npm run build
npm run preview
```

The `dist/` folder is ready to deploy to Netlify, Vercel, or any static host.

---

## 🎬 How to Add Your Video

In `src/GratitudePage.jsx`, find the VideoSection component (~line 215).

Look for the comment block:
```
{/* ── REPLACE BELOW WITH YOUR VIDEO ── */}
<VideoPlaceholder isPlaying={playing} onPlay={() => setPlaying(true)} />
{/* ── END REPLACE ── */}
```

### Option A — Local MP4 file
Place your video in the `public/` folder, then replace the placeholder:
```jsx
<video
  src="/your-video.mp4"
  controls
  autoPlay={playing}
  className="w-full h-full object-cover rounded-2xl"
/>
```

### Option B — YouTube Unlisted
```jsx
<iframe
  src="https://www.youtube.com/embed/YOUR_VIDEO_ID?autoplay=1"
  className="w-full h-full rounded-2xl"
  allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
  allowFullScreen
/>
```

### Option C — Any CDN/hosted URL
```jsx
<video
  src="https://your-cdn.com/video.mp4"
  controls
  className="w-full h-full object-cover rounded-2xl"
/>
```

---

## 📁 Project Structure

```
/
├── index.html
├── package.json
├── vite.config.js
├── tailwind.config.js
├── postcss.config.js
└── src/
    ├── main.jsx          ← Entry point
    ├── index.css         ← Global styles + Tailwind
    └── GratitudePage.jsx ← All sections & components
```

---

## 🎨 Sections

1. **Hero** — Full-screen cinematic opening
2. **Meaning** — What this moment meant
3. **Video** — Your personal video message
4. **Growth** — What changed in 6 months  
5. **Certificate** — The playful "future employee" section
6. **Final** — Emotional closing

---

## 🛠️ Tech Stack

- React 18
- Tailwind CSS 3
- Framer Motion 11
- Vite 5
- Google Fonts (Cormorant Garamond + Nunito + JetBrains Mono)