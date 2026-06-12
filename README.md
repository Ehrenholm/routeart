# RouteArt — GPX Poster Studio

**Turn your GPS tracks into beautiful poster art.**

A single-file web app — no install, no backend, no account. Drop in a GPX file and export a high-resolution poster in seconds.

🔗 **[Try it live → ehrenholm.github.io/routeart](https://ehrenholm.github.io/routeart)**

☕ **[Support development on Ko-fi](https://ko-fi.com/ehrenholm)**

---

## Features

### Track Processing
- **Outlier removal** — statistically removes GPS spikes using median absolute deviation
- **Gaussian smoothing** — adjustable from raw to heavily smoothed
- **Lap detection** — automatically finds repeated circuits; filter or hide individual laps
- **Vectorize** — Douglas-Peucker simplification for clean minimal line art
- **Pen-trace** — Catmull-Rom spline interpolation for a hand-drawn aesthetic

### On-Canvas Editing
- **Timeline trim** — drag handles on a speed/elevation sparkline to trim the track by time
- **Trim mode** — click start/end points directly on the rendered route
- **Exclude zones** — drag a box to remove specific sections (deviations, pit stops)

### Track Colouring
- **Solid** — single theme colour
- **Speed gradient** — colour-mapped to GPS speed with 5-point median filtering
- **Elevation gradient** — colour-mapped to elevation
- Five colour ramps: Heat, Cool, Viridis, Mono, Terrain

### Map Background
- 7 tile providers: OpenStreetMap, OpenTopoMap, CartoDB Dark/Light, ESRI Satellite, OpenCycleMap, Thunderforest Outdoors
- Adjustable opacity and geographic padding
- Tile caching — re-renders are instant after first load

### Art Elements (drag & drop on canvas)
- **Text** — Title, Subtitle, Label (serif / mono / display fonts)
- **Stat block** — big number + small label (e.g. distance, elevation gain)
- **Icon / emoji** — 100+ built-in icons, drag to position
- **Line / arrow** — drag endpoints to rotate/extend; optional arrowheads, dashed style, custom colour
- **Divider** — decorative ruled line with diamond accent
- **Graph** — elevation profile, speed profile, or grade sparkline
- **Image** — import PNG/JPG; PNG transparency preserved; opacity control
- **Layer system** — Background / Middle / Foreground layers with per-layer visibility

### Track Facts
- Distance, elevation gain/loss, min/max elevation
- Average speed, moving average, top speed (median-filtered)
- Pace, duration
- **Add any fact to the poster** with one click

### Route Animation
- **Reveal the route over a set time** (3–60s) — watch it draw itself, with the head following the path
- **Four styles** — Draw / unspool, Comet trail, Snake / segment, and cinematic Camera follow + zoom
- **Live callouts** that update as it plays:
  - **HUD readout** — distance so far, current speed, current elevation, elapsed time
  - **Milestone pins** — pop-up markers for highest point, top-speed point, start & finish
  - **Progress bar + timer**
  - **Big hero stat** — a large number (distance / elevation / speed) front-and-centre
- Uses all your base poster settings — theme, colour gradient, map background, line weight
- **Record to video** — captures the play-through, then a **Save / Share** step delivers it:
  - On **iPhone / iPad** the native share sheet opens → **Save Video** drops it straight into **Photos**
  - On **Mac** it saves an **MP4** you can drag into Photos
  - Prefers **MP4 (H.264)** — the format Apple Photos & Instagram require. Record in **Safari** for guaranteed MP4 on any Apple device
- **Reel 9:16** format made for Instagram Reels & Stories

### Export
- **PNG** — full poster resolution (A3 portrait/landscape or square)
- **SVG** — clean vector export for further editing in Illustrator / Inkscape
- **Video** — animated route as `.webm`/`.mp4` (see Route Animation)

---

## Supported Formats

| Format | Resolution |
|--------|-----------|
| Portrait A3 | 2480 × 3508 px |
| Square | 3000 × 3000 px |
| Landscape A3 | 3508 × 2480 px |
| Reel 9:16 (video) | 1080 × 1920 px |

---

## GPX Data Used

| Tag | Used for |
|-----|---------|
| `<trkpt lat lon>` | Route geometry (required) |
| `<ele>` | Elevation profile, gradient colouring |
| `<time>` | Speed calculation, timeline trim, track facts |

---

## Running Locally

No build step needed — it's a single HTML file.

```bash
git clone https://github.com/ehrenholm/routeart.git
cd routeart
# Open index.html in any modern browser
open index.html
```

Or serve it:
```bash
npx serve .
# → http://localhost:3000
```

---


## Map Tile Attribution

When map backgrounds are enabled, tiles are served by:
- **OpenStreetMap** — © [OpenStreetMap contributors](https://www.openstreetmap.org/copyright) (ODbL)
- **CartoDB** — © [CARTO](https://carto.com/attributions)
- **ESRI** — © [Esri](https://www.esri.com/), Source: Esri, DigitalGlobe, GeoEye, Earthstar Geographics
- **Thunderforest** — © [Thunderforest](https://www.thunderforest.com/), © OpenStreetMap contributors

---

## Support

If RouteArt saves you time or creates something you're proud of, consider supporting its development:

☕ **[Buy me a coffee on Ko-fi](https://ko-fi.com/ehrenholm)**
⭐ **[Star the repo on GitHub](https://github.com/ehrenholm/routeart)**
💬 **[Open an issue](https://github.com/ehrenholm/routeart/issues)** for bugs or feature ideas

---

## License

MIT — free to use, modify, and distribute. Attribution appreciated.

```
MIT License © ehrenholm
```
