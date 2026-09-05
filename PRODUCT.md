# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Stack

Single-file static HTML/CSS per page (inline `<style>`, small inline vanilla JS).
No build step, no framework. Self-hosted fonts under `/assets/fonts`. Deploys to
GitHub Pages from `main`, folder `/`. `CNAME` = `www.freqcraft.app`. Decision
confirmed for the redesign: keep it single-file static HTML/CSS.

## Users

Primary: someone who already knows what brainwave entrainment is and wants
instrument-grade control of it on a phone. Two overlapping groups:

1. **Brainwave Generator (BWGen) refugees** — people who used the late-1990s /
   2000s Windows shareware entrainment tools (Brainwave Generator, SBaGen) for
   the layered, fully-parameterised sessions those allowed, and cannot find a
   modern equivalent that isn't a subscription with hidden presets. Actively
   searched-for: "brainwave generator alternative", "bwgen replacement".
2. **Subscription-app defectors** — people who tried the current crop of
   meditation / focus apps, found them to be preset black boxes that want an
   account and a monthly fee, and want to see and set the actual numbers.

Secondary: EEG tinkerers and students (the audience for the `/protocol` page);
people evaluating whether an audio tool respects their privacy.

Not a target: people looking for a guided-meditation or sleep-story experience,
or for a medical/therapeutic device.

## Product Purpose

FreqCraft is a precision binaural-beat and isochronic-tone generator for Android.
It lets a listener stack up to five simultaneous "voices", each with its own
carrier frequency, beat/pulse frequency, waveform and level envelope, in one
session — with every Hz value visible and editable, a live waveform display, and
true background mixing that plays under other audio without interrupting it.
It has no internet permission and collects nothing. It is a one-time purchase.

The website's job: convert a qualified visitor to a Google Play install, and
capture people searching for a Brainwave Generator replacement. Secondary: a
waitlist for FreqCraft Studio (the desktop successor, in active development).

## Positioning

The transparency and layering of the old desktop entrainment tools (BWGen's
multi-voice sessions, every parameter exposed), rebuilt for modern Android, with
zero data collection and no subscription — sold once. No current app offers
five independently-tuned voices with every value visible AND no account AND no
tracking AND a one-time price; the competition picks at most two of those.

## Operating Context

- Used in wired stereo headphones (binaural mode is headphone-dependent;
  isochronic works on speakers and transducers). The `/support` page's headphone
  and phone-audio-settings guidance is a real part of using the product.
- Often run in the background alongside music, podcasts or an ambient-noise app.
- Long sessions; OEM battery optimisation is a known real-world failure the
  support page addresses.
- The site is frequently reached from a Play Store listing, a BWGen-alternative
  search, or the `/protocol` page shared in an EEG/experiment context.

## Capabilities and Constraints

- Static hosting only (GitHub Pages). No server. One third-party dependency,
  confirmed to keep: the Studio waitlist form posts to Buttondown
  (`buttondown.com/api/emails/embed-subscribe/freqcraft`) via a hidden iframe.
  Everything else (fonts, images) is self-hosted; the app itself has no network.
- Pages after the redesign (all rebuilt): `/` (landing), `/story` (**new** — the
  personal origin story, moved off the landing), `/privacy`, `/support`,
  `/protocol` (the open EEG protocol, a Read-mode document, public domain),
  `/alternatives/brainwave-generator` (the BWGen comparison / migration page).
- Real, verbatim, non-negotiable content:
  - App specs: **5** simultaneous voices, **4** waveforms (sine, square,
    triangle, sawtooth), **2** tone modes (binaural, isochronic), unlimited saved
    presets, **0** data collected, **1** one-time purchase. Package
    `com.directivecraft.freqcraft`, Android, live on Google Play.
  - The medical / legal disclaimers on the landing, `/support` and `/protocol`
    (not a medical device, not FDA-regulated, epilepsy/seizure/cardiac/pregnancy
    warnings, "consult a physician") — regulatory, reproduce exactly.
  - Preset provenance facts (Michael Triggs frequency listing; the archived
    product listing recovered 2019; "Awakened Mind" named after Cade & Coxhead
    1979) — used on `/protocol` and the sources note.
  - The `/protocol` scientific content: hypothesis H1, the 3-condition stimulus
    table (A binaural / B isochronic / C control), procedure, analysis spec,
    null criteria, "what this does not test". Reproduce exactly; it is the
    credibility of the whole site.
- The origin story (dyscalculia; returning to college for chemistry in 2012;
  the accommodation; a 28-page final turned in unfinished; a 98% score) is real
  and stays verbatim — but on its own `/story` page, linked from the landing,
  not on the landing itself.

## Brand Commitments

- Name **FreqCraft** (one word, capital F and C). Published **by Directive Craft
  LLC** — the studio is directivecraft.com, which has its own separate visual
  system ("The Controlled Document"). FreqCraft gets its **own** world; it is the
  consumer product, not the studio.
- Wordmark currently rendered "Freq" + accent "Craft". The incumbent look
  (near-black `#0A0A0F`, neon cyan `#00E5FF`, Space Grotesk, an always-on wave
  canvas) is evidence and anti-reference only — the redesign replaces it.
- Voice: precise, plain, unhyped, quietly confident; names sources; states what
  it does not claim. Not clinical, not woo. "Every Hz visible. Nothing hidden."
- The wave / signal motif is genuine to the product (it draws live waveforms) —
  available to the new world if it earns its place, but not as decorative glow.

## Evidence on Hand

- Real: the app on Google Play; 8 real unretouched app screenshots
  (`assets/shots/1_hero.png` … `8_about.png`, 1080×1920) — the redesign uses the
  strongest 3–4, reworked into the design rather than a raw phone-frame strip;
  `assets/feature_graphic.png`; a SaaSHub "Approved" badge
  (`assets/saashub-approved.png`, links to saashub.com/freqcraft-app).
- Real external references: the Michael Triggs frequency listing
  (lunarsight.com/freq.htm); OSF (osf.io) cited in the protocol.
- Does NOT exist yet, must not be implied as shipping: FreqCraft Studio (desktop)
  — in active development, waitlist only; unlimited voices, session sequencing,
  ambient layers, harmonic filtering, .wav export, preset libraries are Studio
  roadmap, not current features. No testimonials, no user counts, no efficacy
  claims, no download numbers.

## Product Principles

1. Show every number. The differentiator is transparency: no preset a user
   can't inspect, no frequency they can't verify, full parameter access always.
2. Layering is the point. Five independent voices in one session is what BWGen
   users came for and what subscription apps removed.
3. Claim nothing about outcomes. It is an instrument for exploration, not a
   treatment; the site tests and states its own limits (the open protocol, the
   "what this does not test" list).
4. Your device, nothing else. No account, no analytics, no network permission;
   the app literally cannot phone home.
5. Bought once. No subscription, no ads, no paywalled features.
6. Cite sources. Where a preset's numbers came from is stated, and the
   distinction between measured and inferred values is kept.

## Accessibility & Inclusion

No product-specific standard established. Preserve semantic HTML, keyboard
operability, visible focus, adequate contrast; the site must stay legible and
usable without JavaScript (only the Buttondown form and any motion are JS). The
incumbent site runs an unconditional background canvas that ignores
`prefers-reduced-motion`; the redesign must honour reduced-motion.
