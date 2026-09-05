---
version: 1
slug: "index-html"
primary_target: "index.html"
related_targets: []
---

# Surface brief — freqcraft.app (site-wide)

Scope: full site redesign, 6 pages — `/` (landing, Persuade), `/story` (new, Read/persuade),
`/privacy` (Read), `/support` (Operate/Read), `/protocol` (Read), `/alternatives/brainwave-generator` (Persuade).
Primary visitor mode: Persuade on `/` and `/alternatives`; Read on the rest.
Audience: brainwave-entrainment users who want instrument-grade control on a phone — heavily
"Brainwave Generator refugees" and subscription-app defectors.
Action: Google Play install; capture BWGen-replacement searchers; secondary Studio waitlist.
Constraints: single-file static HTML/CSS, GitHub Pages, one third-party dependency kept (the
Buttondown Studio waitlist form). All app specs and the medical/legal disclaimers verbatim.
Prefers-reduced-motion must be honoured (the old site ignored it).

## Direction contract

THESIS: Every FreqCraft site is a matte instrument panel where every Hz is a lit readout and the
unlit segments are drawn as deliberately as the lit ones. It refuses the meditation-app gradient,
the feature-card grid, and the neon-glow "audio tech" look the old site wore.

OWN-WORLD: Matte near-black ground (#0B0B0C / panels #141416 / recessed #1B1B1E). Amber
`--lit #FFAA2B` is the primary ink — every numeric readout, band name, voice tag, section label.
`--ghost #38332B` is the unlit segment, shown behind every readout as an "888.888" mask.
`--live #4FD98A` (green) is reserved for live / actionable: the Google Play action, "ON" voice
states, active nav. `--alert #FF6152` (red) is the medical/epilepsy register only. Structure is
1px seams (`--rule #2C2C30`), never shadows, never radius. Fonts: DSEG7 (numeric readouts),
DSEG14 (single-word lit labels: band names, SINE/SQR), **Hubot Sans for everything a person
reads as a sentence** (the fused prose adaptation — the winning challenger required it), system
mono for `/protocol` code. No background animation.

STORY: Visitor sees a precision instrument, not a wellness app; believes it because every value
is on screen with its ghost mask and its provenance; acts by tapping Get it on Google Play (the
one green control) or the "From Brainwave Generator" cross-reference.

FIRST VIEWPORT (landing): FreqCraft wordmark + "On Google Play" status; a band bar
(delta→gamma, one lit); the H1 sentence with its last line in amber; the five-voice session as a
zero-padded segment readout stack over ghost cells; "Get it on Google Play" as a green bordered
control; the price line; "Came from Brainwave Generator? See the migration →".

FORM: Seven-Segment Panel (bedside clocks / scoreboards / frequency counters). The WINNING
challenger on the direction roll, `challenger-seven-segment`, fused with a prose face for
long-form. Seed key 7937bf3c, kind challenger, code-led. Declined-hand raises folded in:
running guide words (lexicon) as the band bar; accent-for-active-only + asymmetric composition
(raku); voice-stacking shown as overlapping traces that beat at the overlap (riso — the scope
figure); a single moving marker in a fixed field (cityscape — the lit band).

FINISH: unreviewed and undocumented is unfinished; this build ends with the finish review, the verdict, DESIGN.md, and every shipping raster carrying its provenance
