---
name: RouteArt
description: A near-black, warm-champagne field-journal interface for turning GPS tracks into printable poster art.
colors:
  champagne: "#c9b896"
  ink-on-champagne: "#17150f"
  ink-black: "#0b0a08"
  deep-ink: "#0e0d0a"
  wet-ink: "#141209"
  dry-ink: "#1c1a12"
  ink-hover: "#211e15"
  ink-hover-deep: "#252118"
  hairline: "#1d1b16"
  hairline-soft: "#16140f"
  hairline-mid: "#1f1c14"
  hairline-strong: "#232017"
  control-line: "#2a2820"
  toggle-off: "#2b2922"
  parchment: "#efe9dd"
  parchment-faded: "#cfc8b8"
  pencil: "#b8b2a6"
  graphite: "#9a9385"
  graphite-soft: "#8f897c"
  charcoal-dust: "#6f6a5e"
  charcoal-dust-deep: "#5c574c"
  charcoal-dust-deepest: "#4c483e"
  moss: "#6cc08a"
  rust: "#6a4040"
  ember: "#c06060"
  ember-bright: "#f08080"
  dusk-violet: "#9090d8"
  river-blue: "#6090c0"
  fern: "#7aaa7a"
  go-wash-bg: "#141e14"
  go-wash-border: "#2a5028"
  alt-wash-bg: "#201808"
  alt-wash-border: "#5a4010"
  erase-wash-bg: "#200808"
  erase-wash-border: "#481818"
  recolor-wash-bg: "#14121e"
  recolor-wash-border: "#38307a"
  pan-wash-bg: "#101420"
  pan-wash-border: "#203050"
typography:
  display:
    fontFamily: "'DM Serif Display', Georgia, serif"
    fontSize: "21px"
    fontWeight: 400
    lineHeight: 1
    letterSpacing: "0.2px"
  body:
    fontFamily: "'Geist', system-ui, sans-serif"
    fontSize: "12.5px"
    fontWeight: 500
    lineHeight: 1.4
    letterSpacing: "normal"
  label:
    fontFamily: "'Geist Mono', 'DM Mono', monospace"
    fontSize: "10.5px"
    fontWeight: 400
    lineHeight: 1.3
    letterSpacing: "2px"
rounded:
  sm: "6px"
  md: "9px"
  lg: "11px"
  xl: "14px"
  full: "999px"
spacing:
  xs: "4px"
  sm: "8px"
  md: "12px"
  lg: "18px"
components:
  button-primary:
    backgroundColor: "{colors.champagne}"
    textColor: "{colors.ink-on-champagne}"
    rounded: "{rounded.md}"
    padding: "10px 15px"
  button-secondary:
    backgroundColor: "{colors.dry-ink}"
    textColor: "{colors.parchment-faded}"
    rounded: "{rounded.md}"
    padding: "10px 15px"
  button-warn:
    backgroundColor: "#180a0a"
    textColor: "{colors.ember}"
    rounded: "{rounded.md}"
    padding: "10px 15px"
  chip-on:
    backgroundColor: "#1a1609"
    textColor: "{colors.champagne}"
    rounded: "{rounded.sm}"
    padding: "5px 11px"
  chip-off:
    backgroundColor: "transparent"
    textColor: "{colors.graphite-soft}"
    rounded: "{rounded.sm}"
    padding: "5px 11px"
  stat-box:
    backgroundColor: "{colors.wet-ink}"
    textColor: "{colors.parchment}"
    rounded: "{rounded.md}"
    padding: "11px 12px"
  input-text:
    backgroundColor: "{colors.wet-ink}"
    textColor: "{colors.parchment}"
    rounded: "{rounded.md}"
    padding: "9px 11px"
  tab-active:
    backgroundColor: "transparent"
    textColor: "{colors.champagne}"
---

# Design System: RouteArt

## Overview

**Creative North Star: "The Trail Journal"**

RouteArt's interface reads like a well-worn field journal carried across a season of routes: warm low light, matter-of-fact technical readouts in mono type, and a single considered flourish — a serif headline, a wash of champagne gold — rather than decoration. Nothing about the chrome should compete with the artwork someone is actually making; the tool disappears into the work, the way a good notebook disappears into the writing.

Two tools, one voice. GPX Poster's generous, card-based control panel and Track Studio's dense, toolbar-driven canvas are visually one product — same near-black ground, same champagne accent, same mono labels — even though their information density is deliberately different: a leisurely poster-styling panel versus a compact multi-tool drawing toolbar. The system stays quiet everywhere except the moment it needs a flourish: a serif display headline, a warm glow under the one primary action on screen, or a hue-specific wash the instant Track Studio needs you to know exactly which tool is live.

The visual language is quiet on purpose. RouteArt runs entirely in the browser, with no account and no dashboard to check back into — the interface is built to feel like a private notebook you pick up, not a SaaS product vying for your attention. It draws nothing from the bright, badge-and-streak visual language of fitness-tracking dashboards; it draws instead from print, from journals, from the desk-lamp glow of working on something alone at night.

**Key Characteristics:**
- Near-black, warm-toned ground — never pure black; there's always a hair of brown/gold in the shadows.
- One accent color (champagne gold), used sparingly, escalating to hue-specific washes only inside Track Studio's tool modes.
- Serif display type reserved for true headline moments; mono type carries both tiny uppercase labels and every number.
- A quiet lift on every resting surface, a heavier contact shadow only for chrome that floats above the canvas.
- Soft, consistently rounded corners everywhere; no hard right angles in the chrome.

## Colors

Ink and champagne, with a small family of earthy trail hues that only appear when Track Studio needs to name a tool.

### Primary
- **Champagne** (`#c9b896`): the one accent. Primary buttons, active tab underlines, focus borders, the "on" state of toggles, selected-chip text, brand mark. Used sparingly — most of any screen should carry no champagne at all.
- **Ink on Champagne** (`#17150f`): the only text/icon color ever placed directly on a champagne fill (primary button label, toggle knob when on).

### Neutral
- **Ink Black** (`#0b0a08`): the app's page background.
- **Deep Ink** (`#0e0d0a`): header, tab bar, and side-panel background — one step up from the page.
- **Wet Ink** (`#141209`): the default surface for cards, inputs, stat/fact boxes, upload zones.
- **Dry Ink** (`#1c1a12`): the secondary surface — secondary buttons, alternate stat cards, mode buttons at rest.
- **Ink Hover** (`#211e15`) / **Ink Hover Deep** (`#252118`): hover backgrounds for rows, menu items, and export options.
- **Hairline** family — `#1d1b16` (border), `#16140f` / `#1f1c14` / `#232017` (bsub / bsub2 / bsub3), `#2a2820` (control-line): the entire border vocabulary. Always 1px, always this near-black warm gray — RouteArt has no bright or high-contrast border anywhere.
- **Parchment** (`#efe9dd`): primary text.
- **Faded Parchment** (`#cfc8b8`): secondary text (file names, chip labels, body copy inside dense toolbars).
- **Pencil** (`#b8b2a6`): form labels.
- **Graphite** (`#9a9385`) / **Graphite Soft** (`#8f897c`): muted text — helper copy, secondary metadata.
- **Charcoal Dust** (`#6f6a5e`), **Charcoal Dust Deep** (`#5c574c`), **Charcoal Dust Deepest** (`#4c483e`): the faintest text tier — eyebrow labels, disabled captions, the empty-canvas placeholder glyph.

### Signal & Mode Colors
Track Studio hands each drawing mode its own hue instead of reusing champagne for every active state — the one deliberate departure from the single-accent rule, and it's confined entirely to that tool's toolbar.
- **Moss** (`#6cc08a`): "go" / confirm / the active trace mode. Paired with the `go-wash` background (`#141e14`) and border (`#2a5028`).
- **Fern** (`#7aaa7a`): a lighter sibling of Moss, used only for "needs a name" (TBD) label pins — a deliberately unfinished-looking green.
- **Rust** (`#6a4040`) → **Ember** (`#c06060`) → **Ember Bright** (`#f08080`): the danger ramp. Rust is resting/default (the delete glyph at rest), Ember is the active-danger text/icon (erase mode, the Warn button), Ember Bright is the hover state. Paired with the `erase-wash` background (`#200808`) and border (`#481818`).
- **Dusk Violet** (`#9090d8`): the Recolor mode. Paired with the `recolor-wash` background (`#14121e`) and border (`#38307a`).
- **River Blue** (`#6090c0`): the Pan mode. Paired with the `pan-wash` background (`#101420`) and border (`#203050`).
- **Alt-wash** (`#201808` bg / `#5a4010` border): the Alt drawing mode reuses Champagne itself as its text color — only the wash is new — since "alternative" is still a variant of the standard trail, not a different tool.

### Named Rules
**The One Accent Rule.** Champagne is the only accent color in the GPX Poster tool and the only one that ever appears alone. The moment you're inside a multi-mode toolbar (Track Studio), each mode may claim its own hue — but only as a background wash + border pairing, never as a second free-floating accent competing with Champagne app-wide.

**The Wash, Don't Fill Rule.** "Selected" is expressed as a tinted background wash (roughly 8–12% of the hue) plus a full-strength border and text in that hue — never a solid fill. Solid fills are reserved for the single primary action per screen (the Champagne button).

## Typography

**Display Font:** DM Serif Display (with Georgia, serif fallback)
**Body Font:** Geist (with system-ui, sans-serif fallback)
**Label/Mono Font:** Geist Mono (with DM Mono as a secondary mono voice inside rendered poster content)

**Character:** A quiet serif for the rare true headline, a plain humanist sans for everything you read, and a monospace for everything the app is telling you rather than saying to you.

### Hierarchy
- **Display** (weight 400, 21–24px, line-height 1): the app title in the header and the rare full-screen moment (the "Generate 3 versions" overlay headline, the guided-tour bubble title). Reserved for true headline moments only — it never appears in body copy, labels, or buttons.
- **Body** (weight 400–600, 11.5–13px, line-height ~1.4): everything you read and act on — button labels, toggle labels, helper text, modal copy, support links. Weight climbs to 600 specifically for buttons and anything clickable, stays at 400–500 for descriptive text.
- **Label** (weight 400–700, 8.5–16px, letter-spacing 0.5–2px, uppercase for section eyebrows): does double duty as both the tiny uppercase section label (`SOURCE`, `TRACK STUDIO`, `OUTPUT`) *and* every numeric/technical value on screen (stat numbers, zoom %, coordinates, file metadata). Anything that reads as "the app reporting a fact" is mono; anything that reads as "the app speaking to you" is Geist or DM Serif Display.

**Poster Output Fonts (not chrome):** when someone adds a Title/Subtitle/Label element to their poster, they can additionally choose Bebas Neue (display-style condensed) or DM Mono (technical) for that specific canvas text. These render inside the exported artwork only — they are content choices the end user makes for their own poster, not part of RouteArt's own interface type system, and should never be introduced into chrome.

### Named Rules
**The Mono Dual-Duty Rule.** Geist Mono is simultaneously the app's label typeface and its data typeface. If a piece of text is a fact the app is stating (a number, a percentage, a filename, a coordinate) or a structural eyebrow (an all-caps section header), it's mono. If it's something the interface is telling the person to do or describing in prose, it's Geist.

**The Serif Whisper Rule.** DM Serif Display never runs smaller than the app title (21px) as a headline, but its italic/serif character does surface once more, tiny: the guided-tour bubble's title line borrows it at ~11px as a quiet accent, not a second headline size. Don't add a third scale between them.

## Layout

The app is a fixed-height, single-viewport shell (`height:100dvh; overflow:hidden`) — nothing scrolls except individually-scrollable regions (the control panel, the Track Studio label list). A 58px header sits above a two-tab bar (GPX Poster / Track Studio); below that, each tool owns the remaining space differently:

- **GPX Poster**: a fixed 322px left control panel (deep-ink, scrollable, organized into collapsible accordion `.section` blocks with a chevron that rotates −90° when collapsed) beside a flexible canvas stage with a floating, pill-shaped, glass toolbar centered at the bottom.
- **Track Studio**: a top toolbar that wraps into pill-bordered tool groups (File / Style / View / Draw / Color / Erase / Edit / Labels / Output), a fixed 220px label sidebar on the left, and the canvas filling the rest — denser and more technical than GPX Poster's leisurely panel, by design (this is the "hand tools" surface, not the "settings" surface).

**Spacing rhythm** runs in four steps, all observed in the implementation: `4px` (icon-group gaps, chip gaps), `8px` (control-to-control gaps, chip padding), `12px` (card padding, stat-grid gaps), `18px` (section padding, header padding). Nothing in the chrome uses an odd or ad-hoc gap outside this rhythm.

**Responsive behavior** collapses at **760px**: the left panel becomes a bottom sheet — a drag-handle grip, a dimming scrim, and a spring-eased `transform: translateY()` open/close — rather than a redesigned mobile layout. Touch targets grow accordingly (16px form-control font to block iOS auto-zoom, 42px toggle tracks, 20px range thumbs), and secondary header chrome (brand tag, export count, file chip, help dot) is hidden rather than shrunk.

## Elevation & Depth

**The Trail Journal is moving from fully flat toward a quiet lift.** Today's implementation still renders resting surfaces (cards, panels, stat/fact boxes, buttons) with nothing but a 1px hairline border — flat paper on a flat table. The confirmed direction going forward is that every resting surface should carry a soft ambient shadow instead: a card should read like a photograph laid on a dark table, not printed flat onto it. *This is a stated direction for the next component pass, not yet reflected in `index.html` — treat the values below as the target, and update this note once the app itself carries them.*

Floating chrome already earns real depth today and should keep doing exactly what it does: the bottom-centered stage toolbar, the Track Studio legend, context menus, modals, and the trim/render panels combine translucency, `backdrop-filter: blur()`, and a heavy, near-black contact shadow — they read as physically hovering above the canvas, distinct from the page beneath them.

### Shadow Vocabulary
- **Resting Lift** (`box-shadow: 0 2px 6px rgba(5,4,3,.4)`): the new default for every card, panel section, stat/fact box, and button at rest. Nothing should sit perfectly flat against the page.
- **Floating Contact** (`box-shadow: 0 14px 40px rgba(0,0,0,.5)`): already implemented — the stage toolbar, export menu, context menu, modals, and the "Generate 3 versions" overlay cards.
- **Accent Glow** (`box-shadow: 0 2px 10px rgba(201,184,150,.22)`): already implemented — the warm halo under the primary Export/CTA button. Reserved for the single highest-priority action on any given screen.

### Named Rules
**The Two-Tier Lift Rule.** Every resting surface carries the soft Resting Lift shadow — nothing is allowed to sit perfectly flat against the page. Anything that floats above the canvas escalates to the heavier Floating Contact shadow. Only the one primary action per screen additionally earns the warm Accent Glow.

## Shapes

Consistently soft rectangles, radius scaling with control size: small toolbar controls and icon cells run **6px**, the everyday unit — buttons, inputs, cards, stat boxes — runs **9px**, and anything that floats above the canvas (modals, the stage toolbar, floating panels, gen-cards) runs **11–14px**. Anything meant to read as a track or a toggle goes fully round (`50%` knobs and dots, `999px` pill chips and the support button). Borders are always a single 1px hairline in the near-black warm-gray family — RouteArt has no thick border, no double border, and no bright border anywhere in the chrome. There is no unrounded rectangle in the interface; even the mobile bottom sheet's top edge carries a 16px radius.

## Components

### Buttons
- **Shape:** 9px radius everywhere; Track Studio's toolbar buttons run tighter at 6px to match the denser control scale.
- **Primary:** solid Champagne fill, Ink-on-Champagne text, weight 600, Accent Glow shadow, `filter: brightness(1.07)` on hover — never a border, never an outline.
- **Secondary (`.sec`):** Dry Ink fill with a control-line border and Faded Parchment text; hover trades the neutral border/text for Champagne, ghost-style, with no filter change.
- **Warn (`.warn`):** a deliberately muted danger button — near-black red-tinted fill (`#180a0a`), a dark rust border, Ember text. RouteArt never uses a bright, saturated red for a destructive action.
- **Disabled:** flattens to Dry Ink with Charcoal-Dust-Deep text and no shadow — the one state that's allowed to go fully flat.
- **Track Studio mode buttons (signature):** the toolbar's own button language — smaller padding, 6px radius, and a hue-specific wash per active tool (Moss/go, Champagne/alt, Ember/erase, Dusk Violet/recolor, River Blue/pan) instead of the single global accent. Mode identity outranks brand consistency inside this one toolbar.

### Chips
- **Style:** unselected chips are transparent with a control-line border and Graphite-Soft text; selected chips wash to `#1a1609` background with Champagne border and text.
- **State:** used for lap filters and any multi-select filter list — never for single-choice controls (those use segmented `.mbtn` mode buttons instead).

### Cards / Containers
- **Corner Style:** 9–10px for stat/fact boxes and the loaded-file card; 11px for panels and modals.
- **Background:** Wet Ink for primary cards, Dry Ink for anything nested a level deeper.
- **Shadow Strategy:** see Elevation & Depth — Resting Lift going forward; a hairline border today.
- **Border:** always a single hairline in the bsub/bsub2/bsub3 family, matched to the card's nesting depth.
- **Internal Padding:** 11–12px for stat/fact/loaded-file cards; 18px for panel sections.

### Inputs / Fields
- **Style:** Wet Ink background, control-line border, 9px radius; the custom range-slider thumb is a dark disc ringed in a thick 3px Champagne border rather than a filled dot.
- **Focus:** border shifts to Champagne — no glow ring, no outline; the border color change is the only focus signal on desktop, so a stronger focus-visible treatment is worth adding for accessibility.
- **Error / Disabled:** no error state exists yet in text/select inputs; disabled follows the Buttons pattern.

### Navigation
- **Tabs (`.tab-btn`):** small icon + text, Graphite-Soft at rest, Champagne text with a 2px Champagne bottom border when active — a minimal underline-tab pattern, no background change.
- **Mobile:** the tab bar itself doesn't change at 760px; the panel beneath it becomes the bottom sheet described in Layout.

### Track Studio Legend (signature)
A draggable card anchored in canvas space (not screen space — it moves and scales with the track). Translucent near-black background (`rgba(8,8,6,.92)`) with backdrop blur, a hairline border, and small swatch/dash samples paired with tiny Charcoal-Dust-Deepest labels — a print-style map legend rendered live as a DOM overlay rather than baked into the canvas until export. In the light-ink export mode it inverts to a translucent white card with dark ink samples, so the legend always reads correctly against whichever background the person chose for their poster.

## Do's and Don'ts

### Do:
- **Do** use the Wash, Don't Fill pattern for anything selected — tinted background + full-strength border/text — reserving solid fills for the one primary action on screen.
- **Do** give each Track Studio tool mode its own hue (Moss/Champagne/Ember/Dusk Violet/River Blue) rather than reusing the global Champagne accent for every active toolbar state.
- **Do** keep floating/overlay chrome translucent and blurred (Floating Contact shadow); keep resting chrome opaque, moving toward the Resting Lift shadow.
- **Do** reserve DM Serif Display for true headline moments — the app title, full-screen overlay titles — never body copy, labels, or buttons.
- **Do** hold every corner radius to the 6 / 9 / 11–14 / full scale; nothing in the chrome should introduce a fifth radius value.

### Don't:
- **Don't** use a bright, saturated red for destructive actions — the Rust → Ember → Ember Bright ramp stays muted and near-black-rooted, matching the rest of the palette.
- **Don't** let a resting surface sit perfectly flat once the Resting Lift shadow lands — flat-with-only-a-border is the outgoing state, not the target.
- **Don't** introduce a second display font, or let DM Serif Display drift down into UI copy sizes beyond its one tiny accent use in the tour bubble.
- **Don't** borrow Bebas Neue or DM Mono (the poster's own content fonts) into app chrome — they belong to the artwork the user is making, not to RouteArt's own interface.
- **Don't** add a bright focus ring or glow; focus is communicated by a border-color shift to Champagne, consistent with the rest of the quiet, low-glow language.
