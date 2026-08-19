# MO_SITE

A personal olympiad-math site. Pure black background, animated starfield, three pages: home, about, and progress. No frameworks — plain HTML, CSS, and a bit of vanilla JS for the stars.

## Pages

- **`index.html`** — home. Hero, current snapshot, and the full IOQM→RMO→INMO→IMOTC→IMO roadmap.
- **`about.html`** — the pivot story: military school → math and coding.
- **`progress.html`** — topic-by-topic mastery bars, the 80-day study plan, and roadmap detail.

## Files

```
MO_SITE/
├── index.html
├── about.html
├── progress.html
├── styles.css
├── stars.js
└── README.md
```

## Running it in Codespaces

No build step — it's static.

1. Open the folder in your Codespace.
2. Right-click `index.html` → **Open with Live Server** (install the "Live Server" extension if it's not there), or just run:
   ```bash
   python3 -m http.server 8000
   ```
   then open the forwarded port 8000 in the browser tab Codespaces gives you.
3. Edit, save, refresh. That's it.

## Customizing

- **Colors / fonts**: all in `styles.css` under the `:root` block at the top — swap the hex values there and everything updates.
- **Starfield**: `stars.js` controls star density (`buildStars`) and twinkle speed. Fewer stars = better performance on older phones.
- **Content**: stats, roadmap stages, and topic bars are plain HTML in each page — just edit the numbers/text directly, no data file to wire up.

## Deploying

Free options that need zero config for a static site like this:
- **GitHub Pages**: push this repo, then Settings → Pages → deploy from `main` branch.
- **Netlify / Vercel**: drag-and-drop the folder or connect the repo.

## Notes

- Respects `prefers-reduced-motion` — the starfield stops animating if the visitor has that OS setting on.
- No external dependencies except the Google Fonts import in `styles.css` (Space Grotesk, Inter, IBM Plex Mono). Remove that line and set your own `font-family` stack if you want it fully offline-capable.
