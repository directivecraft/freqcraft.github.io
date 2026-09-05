---
name: FreqCraft
description: Precision binaural-beat and isochronic-tone generator for Android — every Hz visible, nothing hidden.
colors:
  ground: "#0B0B0C"
  panel: "#141416"
  panel-2: "#1B1B1E"
  rule: "#2C2C30"
  rule-lit: "#3C3C42"
  lit: "#FFAA2B"
  lit-dim: "#CE9440"
  ghost: "#38332B"
  band-unlit: "#93856A"
  live: "#4FD98A"
  alert: "#FF6152"
  prose: "#DAD6CD"
  prose-dim: "#9A968D"
typography:
  display:
    fontFamily: "Hubot Sans, system-ui, -apple-system, Segoe UI, Roboto, sans-serif"
    fontSize: "clamp(1.9rem, 6vw, 3.4rem)"
    fontWeight: 700
    lineHeight: "1.1"
    letterSpacing: "-0.02em"
  headline:
    fontFamily: "Hubot Sans, system-ui, -apple-system, Segoe UI, Roboto, sans-serif"
    fontSize: "clamp(1.2rem, 3vw, 1.7rem)"
    fontWeight: 700
    lineHeight: "1.2"
    letterSpacing: "-0.015em"
  title:
    fontFamily: "Hubot Sans, system-ui, -apple-system, Segoe UI, Roboto, sans-serif"
    fontSize: "1.02rem"
    fontWeight: 700
    lineHeight: "1.3"
    letterSpacing: "normal"
  body:
    fontFamily: "Hubot Sans, system-ui, -apple-system, Segoe UI, Roboto, sans-serif"
    fontSize: "16px"
    fontWeight: 400
    lineHeight: "1.64"
    letterSpacing: "normal"
  label:
    fontFamily: "Hubot Sans, system-ui, -apple-system, Segoe UI, Roboto, sans-serif"
    fontSize: "0.82rem"
    fontWeight: 700
    lineHeight: "1.3"
    letterSpacing: "0.14em"
  readout:
    fontFamily: "DSEG7, ui-monospace, monospace"
    fontSize: "1.02rem"
    fontWeight: 400
    lineHeight: "1"
    letterSpacing: "normal"
  unit-label:
    fontFamily: "DSEG14, ui-monospace, monospace"
    fontSize: "0.82rem"
    fontWeight: 400
    lineHeight: "1"
    letterSpacing: "0.02em"
  mono:
    fontFamily: "ui-monospace, SF Mono, JetBrains Mono, Menlo, Consolas, monospace"
    fontSize: "0.86em"
    fontWeight: 400
    lineHeight: "1.5"
    letterSpacing: "normal"
rounded:
  none: "0"
  dot: "50%"
spacing:
  hairline: "1px"
  tight: "11px"
  snug: "16px"
  pad: "clamp(18px, 5vw, 40px)"
  bay: "clamp(24px, 5vw, 52px)"
components:
  cta:
    backgroundColor: "{colors.panel}"
    textColor: "{colors.live}"
    typography: "{typography.label}"
    rounded: "{rounded.none}"
    padding: "14px 24px"
  cta-hover:
    backgroundColor: "{colors.panel}"
    textColor: "{colors.live}"
  cta-ghost:
    backgroundColor: "{colors.panel}"
    textColor: "{colors.lit-dim}"
    rounded: "{rounded.none}"
    padding: "13px 22px"
  input-email:
    backgroundColor: "{colors.panel-2}"
    textColor: "{colors.prose}"
    typography: "{typography.body}"
    rounded: "{rounded.none}"
    padding: "13px 16px"
  panel:
    backgroundColor: "{colors.panel}"
    textColor: "{colors.prose}"
    rounded: "{rounded.none}"
    padding: "20px 22px"
  nav-link:
    backgroundColor: "{colors.ground}"
    textColor: "{colors.lit-dim}"
    typography: "{typography.unit-label}"
    padding: "0"
---

# Design System: FreqCraft

## Overview

**Creative North Star: "The Matte Instrument Panel"**

FreqCraft is drawn as a piece of bench equipment photographed in a dark room: a matte near-black chassis, a few lit amber readouts, and everything else — the seams, the unlit segments, the disabled rows — rendered with the same care as the lit parts. It borrows the visual grammar of bedside clocks, scoreboards and frequency counters: seven-segment numerals sitting over their own dim "off" state, hairline rules dividing bays, no gloss. The product's promise is transparency — every Hz visible, nothing hidden — and the design keeps that promise literally: a numeral is shown lit over the ghost of all-eights, so you can see the display is honest about what it can and cannot show.

The system refuses three things by name: the meditation-app gradient wash, the feature-card grid, and the incumbent site's neon-glow "audio tech" look with its always-on background wave canvas. There is no shadow anywhere and no border-radius anywhere except one 8px status dot. Colour is rationed hard — amber is the only ink that lights up, green appears only where something is genuinely actionable, red appears only in the medical register. Body copy is a warm off-white, never pure white. The page is a single centred column bordered left and right (the "rack"), divided into stacked "bay" sections by 1px top rules.

Motion is one authored moment: a power-on sweep where the numeric readouts animate up from the ghost colour to lit, staggered per row, then the class is removed. Everything else is a link or arrow micro-transition, and `prefers-reduced-motion` removes even the power-on.

**Key Characteristics:**
- Matte near-black chassis, four tonal steps, zero shadow
- Amber is the only "lit" ink; green = live, red = medical
- Seven-segment numerals over a visible "ghost" off-state
- Hairline (1px) rules are the only divider; a bordered centre column
- One authored animation (power-on), reduced-motion-safe
- Square corners everywhere except a single 8px LED dot

## Colors

A four-step matte greyscale chassis lit by a single rationed amber, with green and red held in reserve for two specific registers.

### Primary
- **Lit Amber** (`#FFAA2B`): the one ink that "lights up." Every numeric readout (seven-segment), every single-word segment label (band names, waveform tags, voice numbers), every section label (`.lit`), heading accent `<em>`, the `+`/`−` FAQ markers, and the wordmark's "Craft". This is the display glow of the instrument.
- **Amber Dim** (`#CE9440`): secondary amber for supporting labels — spec captions, feature-row prose that isn't lit, table headers, figcaptions, footer nav, inactive-but-present states, the scope waveform's back traces.

### Secondary
- **Live Green** (`#4FD98A`): actionable-only. The Google Play CTA border and text, the Studio waitlist submit, the "on" voice status dot, active nav ("Get it"), all body links (green text + 42%-opacity green underline), the `:focus-visible` ring, and the scoreboard "supported" check.
- **Alert Red** (`#FF6152`): the medical / epilepsy / cardiac register only. Rendered as a 1px left rule on safety blocks (`.safety`, `.legal` warning, protocol footer, `.panel.flag`) plus the bullet markers on BWGen pain-point lists. Never used decoratively.

### Neutral
- **Ground** (`#0B0B0C`): page background; also the `::selection` text colour on amber.
- **Panel** (`#141416`): the primary raised surface — stacks, spec rows, studio card, panels, table body, active band cell.
- **Panel 2** (`#1B1B1E`): the recessed step — band bar, table headers, input fields, inset plate frames.
- **Rule** (`#2C2C30`): the 1px seam between bays, rows, table cells, and the rack's own left/right edges.
- **Rule Lit** (`#3C3C42`): the slightly brighter 1px stroke on standalone framed objects (stack, specs, panels, plates, scope, studio, inputs) and the scrollbar thumb.
- **Ghost** (`#38332B`): the unlit segment — the `888.888` / `8` / `88%` mask drawn behind every readout, and the colour disabled rows and the scoreboard "not supported" minus fall back to.
- **Band Unlit** (`#93856A`): a dedicated warmer grey for the inactive guide-word band names in the delta→gamma scale, lifted off `--ghost` so the full scale stays legible even when only one band is lit.
- **Prose** (`#DAD6CD`): warm off-white body text and emphasized `<strong>`.
- **Prose Dim** (`#9A968D`): secondary body text, standfirsts, hero sub, captions, disabled-context prose.

### Named Rules
**The One Ink Rule.** Amber is the only colour that reads as "lit." It marks numbers and the labels that name them, nothing else. If a new element isn't a readout, a reading, or the label for one, it is not amber.

**The Reserved Register Rule.** Green means a human can act on this right now (install, submit, follow a link). Red means medical/safety. Neither colour is available for decoration, emphasis, or hierarchy — if you reach for green or red to make something stand out, use amber or a tonal step instead.

**The Honest Display Rule.** Every seven-segment readout is drawn over its own ghost mask (`data-g` / `::before`) showing the full-eights off-state in `--ghost`. A number is never shown floating without the unlit segments it sits in.

## Typography

**Display / Body / Label Font:** Hubot Sans (self-hosted variable, weights 400–700; falls back to system-ui, -apple-system, Segoe UI, Roboto). Everything a person reads as a sentence — headlines, prose, nav, captions, buttons, section labels — is Hubot Sans. This is the deliberate fused adaptation: one humanist sans carries the whole reading surface.
**Readout Font:** DSEG7 (`--seg7`, self-hosted, OFL) — seven-segment; numeric readouts only.
**Segment-Label Font:** DSEG14 (`--seg14`, self-hosted, OFL) — fourteen-segment; single lit words only: band names (DELTA…GAMMA), waveform tags (SINE / SQR), voice numbers (V1…V5), privacy fact values (NONE / NO).
**Mono Font:** system monospace stack (`--mono`) — `/protocol` and `/support` inline `code`, a few technical figcaptions, effective-date stamps.

**Character:** Hubot Sans is confident and slightly mechanical without being cold — it reads as instrument-panel signage, not clinical. Against the two DSEG faces it sets up a clear division of labour: sentences in the humanist sans, values in the segment displays. The segment fonts are never used for running text or multi-word labels.

### Hierarchy
- **Display** (700, `clamp(1.9rem, 6vw, 3.4rem)`, line-height 1.1, tracking -0.02em): page `h1` only. Tight, balanced, `max-width` ~16–20ch. Accent words wrapped in `<em>` go amber (upright on the landing, italic on `/protocol` and `/story`).
- **Headline** (700, `clamp(1.2rem, 3vw, 1.7rem)`, tracking -0.015em, colour `--prose`): `h2` section titles.
- **Title** (700, `1.02rem`, colour `--lit`): `h3` sub-headings inside long documents.
- **Body** (400, 16px, line-height 1.62–1.68): prose, constrained to `max-width: 56ch`. `<strong>` goes to `--prose` (full off-white) for emphasis against dim body text.
- **Label** (700, `0.80–0.82rem`, tracking 0.14em, UPPERCASE, colour `--lit`): the `.lit` panel/section label — Hubot, not a segment font. `.lit.dim` variant is weight 600 in `--lit-dim`. Smaller uppercase-tracked labels (feature `.ft`, spec `.sk`, status chips) share this treatment at 0.72–0.80rem.
- **Readout** (400/700, DSEG7, `font-variant-numeric: tabular-nums`): voice frequencies (~1.02rem), spec values (~1.55rem), the `/story` "98%" score (`clamp(3.4rem, 14vw, 6rem)`), stimulus-table Hz. Always over a ghost mask.
- **Unit Label** (400, DSEG14, ~0.78–0.92rem): single lit words as listed above.

### Named Rules
**The Sentence / Value Split Rule.** If it is a sentence or a phrase, it is Hubot Sans. If it is a bare number, it is DSEG7. If it is a single all-caps token that names a band, wave, voice or fact, it is DSEG14. There is no fourth case.

**The Lit-Label-Is-Not-A-Segment Rule.** `.lit` section labels are Hubot 700 uppercase tracked in amber — they look "lit" by colour and tracking, never by using the segment font. Segment fonts stay on actual readouts.

## Layout

**The rack.** Every page is a single centred column, `max-width: 60rem` (`52rem` on `/protocol`), carried jointly by `header`, `main` and `footer`, each with a 1px left and right border (`--rule`) so the column reads as a continuous bordered chassis. Horizontal padding is `--pad` = `clamp(18px, 5vw, 40px)`.

**Bays.** Content is stacked `.bay` sections separated by a single 1px top border (`--rule`); the first bay in `main` drops its border. Vertical padding is `clamp(24px–30px, 4.5–5vw, 40px–52px)` depending on page. No bay has a background of its own — depth comes only from framed objects inside it.

**Measure.** Prose columns are held to `max-width: 56ch` (`.measure` / `.lead` / default `p`). Data objects (stacks, tables, spec grids) run the full column width and scroll horizontally on narrow screens rather than reflowing, except the voice stack which reflows to 2 lines per voice at ≤620px.

**Grids.** Fixed small-count grids only: 5-up band bar, 6-up spec row, 3-up privacy facts, 2-up release cards. Each collapses at a specific breakpoint (band bar → 3-up at 460px; specs → 3-up at 720px; facts → 2-up at 560px; release cards → 1-up at 600px) by re-drawing internal borders, never by restacking into cards.

**Header.** `.topbar` (wordmark + nav, `space-between`, wrapping) over an optional `.bandbar` (the delta→gamma guide-word scale, one cell `.on`).

**Spacing rhythm.** Built on 1px seams and a loose set of steps around 11 / 13 / 16 / 20px for internal padding and gaps; section rhythm is the `clamp()` bay padding. There is no strict 4- or 8-pt grid in the build.

## Elevation & Depth

No shadows anywhere. `box-shadow` does not appear in the system. Depth is entirely tonal and linear: four background steps (`--ground` → `--panel-2` → `--panel`, plus `--rule`/`--rule-lit` strokes) plus 1px borders. A framed object (stack, spec row, panel, plate, studio card, input) is a `--panel` fill inside a `--rule-lit` 1px border sitting on the bay; a recessed object (band bar, table header, input) drops to `--panel-2`. Nothing lifts, nothing floats, nothing glows — the amber "glow" is pure hue, not a blur.

### Named Rules
**The No-Shadow Rule.** There is no `box-shadow`, `text-shadow` or `filter: blur()` in this system. If something needs to separate from its background, give it a 1px `--rule`/`--rule-lit` border or move it one tonal step.

**The No-Glow Rule.** Amber never gets a shadow, halo or bloom. The incumbent site's neon-glow treatment is the anti-reference; lit elements are flat fills of `--lit`.

## Shapes

Square. `border-radius` is `0` on every surface, control, input, frame and table in the build. The single exception is the voice-status LED (`.vd`): an 8px circle (`border-radius: 50%`), green when the voice is on, `--ghost` when off — the one round element on the site, and it earns it by being a literal indicator lamp. Rules and borders are always exactly 1px. The scope figure and its beat envelope are the only curves, and they are data (drawn sine waves), not decoration.

## Components

### Buttons
- **Shape:** square (0 radius), 1px border.
- **Primary (`.cta`):** `--panel` fill, 1px `--live` border, `--live` uppercase Hubot 700 text tracked 0.05–0.06em, padding `13–14px 22–24px`, often with a trailing `→` arrow. Used for the Play install and the Studio waitlist submit.
- **Hover:** background shifts to `color-mix(in srgb, var(--live) 12%, var(--panel))`; the arrow translates 3px right (`transition: transform 0.15s`). Reduced-motion cancels the arrow move.
- **Ghost (`.cta.ghost`):** same shape, `--lit-dim` text, border drops to `--rule-lit`. Secondary action ("Notify me about Studio").
- **Focus:** global `:focus-visible` — 2px `--live` outline, 2px offset.

### Inputs / Fields
- **Style:** `--panel-2` fill, 1px `--rule-lit` border, 0 radius, `--prose` text in Hubot 0.95rem, padding `13px 16px`, placeholder in `--prose-dim`.
- **Focus:** border-colour shifts to `--live` (no ring beyond the global focus outline, no glow).
- Only instance: the Buttondown waitlist email field (`.wl input`), which posts through a hidden iframe; on submit the form hides and a green `--live` confirmation line replaces it.

### Navigation
- **Top nav (`.topnav`):** Hubot 600, ~0.82rem, `--lit-dim`, no underline; hover → `--lit`. The Play link (`a.play`) is `--live`. Wraps under the wordmark on narrow screens; no hamburger, no disclosure.
- **Footer nav (`.foot nav`):** same treatment, smaller; hover → `--lit`.
- **Body links (`a`):** `--live` text with a 1px underline at 42% green opacity; hover brings the underline to full `--live`.

### Panels (`.panel`)
- **Corner:** square. **Background:** `--panel`. **Border:** 1px `--rule-lit`, or a 1px *left-only* rule for register panels: `--lit` on `.panel.key` (the claim / null-criteria callout on `/protocol`), `--alert` on `.panel.flag` (the "what this does not test" block).
- **Padding:** `20px 22px`.

### Band Bar (`.bandbar` / `.band`)
The delta→gamma brainwave scale as a 5-cell strip on `--panel-2`, cells split by 1px `--rule`. Each cell: a DSEG14 band name over a `--mono` Hz range. Exactly one cell carries `.on` — it fills to `--panel`, its name goes `--lit`, its range `--lit-dim`. Inactive names are `--band-unlit` (`#93856A`), deliberately lifted off ghost so the whole scale reads. Collapses to 3-up at 460px. `aria-hidden` — decorative orientation, not content.

### Voice Stack (`.stack` / `.vrow` / `.seg7`)
The signature component: a framed five-row readout of a session. Each `.vrow` is a grid of voice number (DSEG14), carrier Hz (DSEG7 over `888.888` ghost), beat Hz (DSEG7 over `88.888` ghost), waveform tag (DSEG14), and an 8px status LED. A `.vrow.off` row drops every value to `--ghost` and the LED to `--ghost`. Reflows to 2 lines per voice at ≤620px; scrolls horizontally above that until it fits. This is where the power-on animation lives.

### Spec Row (`.specs` / `.spec`)
A 6-up grid of big DSEG7 values (5 / 4 / 2 / ∞ / 1 / 0) each over a single `8` ghost, with a `--lit-dim` uppercase Hubot caption under it. The `∞` value (`.sv.inf`) switches to Hubot 700 and drops its ghost mask. Collapses to 3-up at 720px.

### Scoreboard Table (`table.board`, `/alternatives`)
Full-width `--panel` table, 1px `--rule` cell borders, `--panel-2` `--lit-dim` header row. Capability column in `--prose`; support cells centred with a `--live` check (supported), a `--ghost` minus (not supported), or a small `--lit-dim` uppercase "Planned" chip (roadmap). A `.dim` sub-note in `--prose-dim` can sit under any cell value. Scrolls horizontally under 640px. The generic document table on `/protocol` follows the same skin, with `td.num` frequencies in DSEG7 `--lit`.

### FAQ (`details` / `summary`, `/support`)
No-JS disclosure list. Rows split by 1px `--rule` top borders. `summary` is Hubot 600 1rem `--prose`, list-marker removed, with a `--mono` `+` at the right that becomes `−` when `[open]`; hover turns the summary `--lit`. Answer body prose is `--prose-dim`, held to 56ch.

### Screenshot Plates (`.plates` / `.plate`)
Horizontal scroll-snap strip of bordered figures (1px `--rule-lit`, `--panel-2` frame, 0 radius). The app screenshots inside are **the only full-colour imagery on the site** and are kept at the app's real cyan — the design does not recolour them. `figcaption` in `--lit-dim` Hubot over a 1px `--rule` top border.

### Scope Figure (`.scope`)
Framed inline-SVG: two close carrier sine traces in `--lit-dim` at 0.5 opacity plus the summed beat envelope in `--lit` at 2.4px stroke, over `--panel`, with a `--mono` figcaption. The wave motif appears here as data only — never as background or decoration.

### Status Chips
Small inline uppercase Hubot 700 tokens at ~0.7–0.72rem: `.rt.now` in `--live` ("Available now"), `.rt.soon` in `--lit-dim` ("In development"), `td.plan` "Planned". Not bordered — colour and tracking carry them.

## Do's and Don'ts

### Do:
- **Do** build every page as a `rack` (1px-bordered centred column, `max-width` 60rem / 52rem on long-form docs) of `bay` sections divided by single 1px `--rule` top borders.
- **Do** render every bare number in DSEG7 over its ghost mask, and every single lit token (band, wave, voice, fact) in DSEG14.
- **Do** keep amber for readouts and their labels only; reach for a tonal step (`--panel`, `--rule-lit`, `--prose-dim`) for any other emphasis.
- **Do** separate surfaces with a 1px border or one tonal step — `--panel` inside `--rule-lit`, recessed things to `--panel-2`.
- **Do** hold prose to `max-width: 56ch` and set `<strong>` to `--prose` against `--prose-dim` body text.
- **Do** gate the one animation behind `body.boot` and remove it after load; honour `prefers-reduced-motion` on every motion, including scroll-behavior.
- **Do** use the left-1px-rule register: `--lit` for key callouts, `--alert` for safety and medical blocks.

### Don't:
- **Don't** add any `box-shadow`, `text-shadow`, `filter: blur()`, or amber glow. The neon-glow "audio tech" look is the anti-reference.
- **Don't** use `border-radius` on anything except the 8px voice-status LED.
- **Don't** use green or red for decoration or hierarchy — green is "actionable now," red is "medical," and nothing else.
- **Don't** set running text, multi-word labels, or headings in DSEG7 or DSEG14 — segment fonts are for values and single tokens only.
- **Don't** introduce a feature-card grid or a gradient background; data objects run full-width and scroll rather than reflowing into cards.
- **Don't** recolour the app screenshots — they stay at the app's real cyan and are the only full-colour imagery allowed.
- **Don't** use pure white (`#FFF`) for text; body copy is warm off-white `--prose` / `--prose-dim`.
- **Don't** add a background wave animation or an always-on canvas; the wave motif is allowed only as a static data figure.
