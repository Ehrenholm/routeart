# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Users

Solo endurance athletes and outdoors people (runners, cyclists, hikers) who have a GPX track from an activity and want to turn it into something to keep, print, or share. The same person uses both tools on the same page: GPX Poster to auto-generate a styled poster, and Track Studio as a manual drawing/annotation layer on top of a track or image (tracing sections, marking standard vs. alternate routes, labeling, adding a legend). These are not two separate audiences — one user, two levels of control over one track.

## Product Purpose

RouteArt is a single-file, no-install, no-account web app that turns a GPS track into poster art. GPX Poster ingests a `.gpx` file and auto-generates a customizable poster: track processing (outlier removal, smoothing, lap detection, simplification), styling (solid/speed/elevation coloring, map tile backgrounds, drag-and-drop art elements, stat blocks), and an animated "route reveal" that can be recorded to video. Track Studio is a second, manual tool for hand-tracing and annotating a track or any uploaded image — drawing standard/alternate sections, labels, start/finish markers, and a legend — for a more deliberate, hand-built route diagram rather than an auto-styled poster. Success is the user leaving with an exported PNG, SVG, or video they're proud enough of to print, post, or share, produced entirely on their own device.

## Positioning

Privacy and independence: everything runs client-side in the browser. No account, no server-side processing, no subscription — the user's GPX track never leaves their machine (the one exception is map tile requests to third-party tile providers when a map background is enabled). This is the mechanism a cloud/SaaS competitor (Strava's route art, VeloViewer, Wandrer, RideWithGPS poster makers) cannot truthfully copy, since their model requires an account and server-side processing.

## Operating Context

Typical flow: drop in a GPX file → adjust track processing → style the poster (color, map background, art elements, stats) → optionally switch to Track Studio, using the rendered poster ("⬇ From RouteArt") or an uploaded image as the background, to manually trace/label sections and build a legend → export PNG/SVG, or record the animated route reveal as video for sharing (e.g. Instagram Reels, saved to iOS Photos via the native share sheet, best captured in Safari for guaranteed MP4). Map backgrounds are the only external network dependency (OpenStreetMap, OpenTopoMap, CartoDB, ESRI, OpenCycleMap, Thunderforest); tiles are cached client-side after first load. No login or server-side session — persistence is local browser state (a "tour seen" flag) and explicit session save/load as a JSON file the user manages themselves.

## Capabilities and Constraints

- Ships today as a single static `index.html` — no build step, no backend, no account/auth, deployed on GitHub Pages. Not yet confirmed as a binding future constraint (see below) — recorded here as current architecture.
- Two tools live on one page: **GPX Poster** (auto-generates from a GPX file) and **Track Studio** (manual drawing/annotation, can start from an uploaded image or the current poster as background). They are one product, not two disconnected apps.
- Track processing is statistical: median-absolute-deviation outlier removal, Gaussian smoothing, Douglas-Peucker simplification, Catmull-Rom "pen-trace" interpolation.
- Export formats: PNG (high-res raster), SVG (vector), and video (webm/mp4) for the animated route reveal; MP4/H.264 is preferred for Apple Photos/Instagram compatibility.
- Touch and pointer events are implemented for canvas interactions (drag, pinch-zoom, timeline trim), so mobile/tablet use is supported for at least core interactions. Whether Track Studio's dense toolbar is actually well-suited to small screens is an open question, not resolved here.
- No accessibility affordances exist in the current markup (no ARIA attributes anywhere). This is a known gap to flag, not a stated requirement — no accessibility standard has been established for this product.
- Monetization is donation-only today (Ko-fi, GitHub Sponsors) and the user confirmed this stays fixed: the tool stays free, with no pricing/paywall to design around.
- Not confirmed as binding constraints (raised but not selected during init): whether the single-file/no-backend architecture and GitHub Pages/MIT-license hosting must stay fixed for future work, versus just describing today's implementation. Treat as current state, not an instruction to preserve, unless the user says otherwise.

## Brand Commitments

Name "RouteArt", tagline "GPX Poster Studio", 📍 pin-emoji mark/favicon. The current codebase carries a completed "RouteArt Studio redesign": a dark, warm atelier palette (near-black app background, warm sand/gold accent `#c9b896`), DM Serif Display for headline type, Geist/Geist Mono for UI text. Treat this as the incumbent visual identity to preserve unless a redesign is explicitly requested.

## Evidence on Hand

README.md documents the full feature set and supported export resolutions (Portrait A3 2480×3508, Square 3000×3000, Landscape A3 3508×2480, Reel 9:16 video 1080×1920). No testimonials, customer names, usage benchmarks, or analytics data exist anywhere in the repo — future work must not invent any.

## Product Principles

1. Nothing leaves the browser that doesn't have to — privacy and independence are the core promise, not a footnote.
2. Auto-generation (GPX Poster) and hand-built control (Track Studio) are both first-class; neither is a lesser fallback of the other.
3. A track/session can move between the two tools in one flow — they read as one product, not two apps bolted together.
4. Free and donation-supported by design — no feature should ever be gated behind payment.
5. Export quality (true high-res PNG/SVG, real MP4 for Apple/Instagram) matters as much as the editing experience — the point is to leave the app with something real.

## Accessibility & Inclusion

No standard or user-specific requirement has been established. The current markup has no ARIA support at all — recorded as a known gap for future work to address, not as a requirement stated by the user.
