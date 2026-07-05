# Dhanush Vishwanathan RK — Portfolio

A single-page, 3D-styled portfolio site with a video intro, animated neural-network background (Three.js), and interactive tilt cards.

## Files
- `index.html` — the entire site (HTML + CSS + JS in one file)
- `hero-video.mp4` — your intro video, used as the hero background

Both files must stay in the **same folder** — the page loads the video with a relative path (`hero-video.mp4`).

## Run it locally
Just double-click `index.html`, or open it in any browser. No build step, no server needed.

## Put it live on GitHub Pages (free)
1. Create a new repository on GitHub, e.g. `portfolio`.
2. Upload both `index.html` and `hero-video.mp4` to the repo root (drag-and-drop on the GitHub web UI works fine, or `git add . && git commit -m "portfolio" && git push`).
3. Go to **Settings → Pages**.
4. Under "Build and deployment", set **Source: Deploy from a branch**, branch **main**, folder **/(root)**.
5. Save. GitHub gives you a URL like `https://<your-username>.github.io/portfolio/` within a minute or two.

That's it — no configuration files, no dependencies to install.

## Things you'll want to personalize
- In `index.html`, search for `href="#"` in the **Links** contact card near the bottom and swap in your real LinkedIn / GitHub / Portfolio URLs.
- The video is muted+autoplay+loop so it works reliably across browsers (autoplay policies block videos with sound).

## Notes on the design
- Fonts: Space Grotesk (headings), Inter (body), JetBrains Mono (labels/data) — loaded from Google Fonts.
- Three.js (from cdnjs) draws the drifting particle/connection mesh behind the whole page — a nod to neural networks / security graphs, tying into your AI + cybersecurity focus.
- Cards tilt in real 3D based on your mouse position (`perspective` + `rotateX/rotateY`), not just box-shadows — that's what gives the "real" 3D feel.
- Respects `prefers-reduced-motion` and works fine on mobile (tilt effects are mouse-only; touch just gets clean static cards).
