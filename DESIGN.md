---
name: "ÆTHER"
description: "An antique celestial chart made playable through constellated hands and an audio-reactive aurora."
colors:
  celestial-ground: "#04060f"
  atlas-ink: "#e3e9ff"
  atlas-ink-dim: "#9aa3d0"
  atlas-ink-faint: "#5b638f"
  engraved-hairline: "rgba(190, 205, 255, 0.16)"
  observatory-panel: "rgba(7, 10, 26, 0.82)"
  atlas-accent: "#9db8ff"
  slider-star: "#eaf0ff"
  spectral-degree-1: "hsl(190, 90%, 72%)"
  spectral-degree-2: "hsl(262, 90%, 72%)"
  spectral-degree-3: "hsl(318, 90%, 72%)"
  spectral-degree-4: "hsl(40, 90%, 72%)"
  spectral-degree-5: "hsl(152, 90%, 72%)"
  spectral-degree-6: "hsl(214, 90%, 72%)"
  spectral-degree-7: "hsl(288, 90%, 72%)"
typography:
  display:
    fontFamily: "Marcellus, Georgia, serif"
    fontSize: "clamp(52px, 9vw, 96px)"
    fontWeight: 400
    lineHeight: 1
    letterSpacing: "0.3em"
  headline:
    fontFamily: "Marcellus, Georgia, serif"
    fontSize: "22px"
    fontWeight: 400
    lineHeight: 1.2
    letterSpacing: "0.2em"
  title:
    fontFamily: "Marcellus, Georgia, serif"
    fontSize: "21px"
    fontWeight: 400
    lineHeight: 1.2
    letterSpacing: "0.34em"
  body:
    fontFamily: "Marcellus, Georgia, serif"
    fontSize: "14px"
    fontWeight: 400
    lineHeight: 1.9
    letterSpacing: "0.03em"
  label:
    fontFamily: "Marcellus, Georgia, serif"
    fontSize: "11px"
    fontWeight: 400
    lineHeight: 1.8
    letterSpacing: "0.16em"
rounded:
  rectilinear: "0px"
  celestial: "50%"
spacing:
  inset-fine: "4px"
  control: "8px"
  plate: "14px"
  field: "16px"
  panel: "22px"
  overlay: "24px"
  chrome: "26px"
components:
  tune-button:
    backgroundColor: "transparent"
    textColor: "{colors.atlas-ink-dim}"
    typography: "{typography.label}"
    rounded: "{rounded.rectilinear}"
    padding: "9px 18px 8px"
  tune-button-hover:
    backgroundColor: "transparent"
    textColor: "{colors.atlas-ink}"
    typography: "{typography.label}"
    rounded: "{rounded.rectilinear}"
    padding: "9px 18px 8px"
  observatory-panel:
    backgroundColor: "{colors.observatory-panel}"
    textColor: "{colors.atlas-ink}"
    rounded: "{rounded.rectilinear}"
    padding: "22px 22px 20px"
    width: "268px"
  tuning-select:
    backgroundColor: "rgba(12, 16, 38, 0.9)"
    textColor: "{colors.atlas-ink}"
    typography: "{typography.body}"
    rounded: "{rounded.rectilinear}"
    padding: "8px 10px"
    width: "100%"
  begin-observation:
    backgroundColor: "transparent"
    textColor: "{colors.atlas-ink}"
    typography: "{typography.label}"
    rounded: "{rounded.rectilinear}"
    padding: "17px 44px 15px"
  camera-ghost-toggle:
    backgroundColor: "transparent"
    textColor: "{colors.atlas-ink-dim}"
    typography: "{typography.label}"
    rounded: "{rounded.rectilinear}"
    padding: "5px 12px 4px"
---

# Design System: ÆTHER

## Overview

**Creative North Star: "The Living Star Atlas"**

ÆTHER is an antique celestial engraving that has learned to listen. A deep indigo plate fills the viewport; fine declination rules, note labels, minute ticks, corner marks, catalog glyphs, and a Latin plate caption establish the quiet authority of a historical star chart. The interface chrome is sparse and typographic so the instrument remains the world, not a control panel laid over it.

Sound and gesture supply the living layer. Hands are reduced to low-contrast constellation structures, while active fingers ignite in a scale-degree spectrum, cast nova rings, shed upward stardust, illuminate their pitch rows, and feed a waveform aurora along the lower horizon. The visual hierarchy depends on rarity: pale engraved geometry is persistent, but saturated color appears only when the instrument is responding.

The system is immersive rather than app-like. It rejects the category default of a black void with a neon hand-tracking skeleton; camera imagery is only a faint mirrored ghost, controls are observatory instruments, and every visible state speaks in the language of charting, stars, veils, and observation.

**Key Characteristics:**
- Full-bleed, deep-indigo celestial plate with fixed, sparse chrome.
- Hairline engraving, square controls, double rules, ticks, and catalog notation.
- One classical typeface used at multiple scales with wide tracked capitals.
- Spectral color keyed deterministically to musical scale degree.
- Hands rendered as constellations, never as a generic landmark-debug overlay.
- Audio energy and hand distance drive light, scale, hue, and the aurora horizon.

## Colors

The palette is an indigo monochrome engraving at rest and a seven-hue spectral instrument in performance.

### Primary
- **Atlas Accent** (`atlas-accent`): the cool blue-violet authority color for focus outlines, tuning states, rune strokes, and controlled glows.
- **Atlas Ink** (`atlas-ink`): the brightest persistent text and line color, reserved for the wordmark, active labels, button copy, and star cores.
- **Slider Star** (`slider-star`): the compact white-blue highlight used for range thumbs; it should read as a small luminous object rather than a conventional form handle.

### Secondary
- **Spectral Cyan** (`spectral-degree-1`, hue 190°): first scale degree.
- **Spectral Violet** (`spectral-degree-2`, hue 262°): second scale degree.
- **Spectral Magenta** (`spectral-degree-3`, hue 318°): third scale degree.
- **Spectral Gold** (`spectral-degree-4`, hue 40°): fourth scale degree.
- **Spectral Verdant** (`spectral-degree-5`, hue 152°): fifth scale degree.
- **Spectral Blue** (`spectral-degree-6`, hue 214°): sixth scale degree.
- **Spectral Orchid** (`spectral-degree-7`, hue 288°): seventh scale degree.

The hue sequence is cyclic and indexed by the current scale degree. Saturation, lightness, and alpha vary by layer: active bones use a crisp mid-light value, labels are lighter, glows are radial and translucent, and particles are softer. The hue identity does not vary.

### Neutral
- **Celestial Ground** (`celestial-ground`): the page and canvas ground; all atmospheric color is composited over it.
- **Observatory Panel** (`observatory-panel`): a translucent indigo-black field that preserves the chart beneath the tuning controls.
- **Atlas Ink Dim** (`atlas-ink-dim`): secondary copy, field labels, control labels, and explanatory text.
- **Atlas Ink Faint** (`atlas-ink-faint`): tertiary chrome, privacy copy, legend framing, and idle status text.
- **Engraved Hairline** (`engraved-hairline`): borders, dividers, ticks, and chart geometry. Related canvas rules use the same blue-white family at lower or slightly higher alpha according to emphasis.

### Named Rules

**The Plate Before Glow Rule.** Persistent structure stays low-contrast and engraved; saturated light is earned by sound, gesture, focus, or ignition.

**The Degree-Hue Rule.** Musical scale degree, not hand, finger, or component category, owns spectral hue. Preserve the 190° / 262° / 318° / 40° / 152° / 214° / 288° cycle.

**The Indigo Ground Rule.** Never lift the instrument onto a neutral gray, pure black, or colored card canvas. The built world begins with the deep indigo plate.

## Typography

**Display Font:** Marcellus (with Georgia, serif fallback)  
**Body Font:** Marcellus (with Georgia, serif fallback)  
**Label/Mono Font:** No separate label or monospaced face is used.

**Character:** The single-face system makes interface language feel engraved rather than typeset by an application. Hierarchy comes from scale, tracking, case, opacity, and placement—not from mixing font families or weights.

### Hierarchy
- **Display** (400, fluid 52–96px, 1 line-height, 0.3em tracking): the entry-veil ÆTHER title. Apply matching text indent when centered so the final tracked letter does not make the word appear off-center.
- **Headline** (400, 22px, 1.2 line-height, 0.2em tracking): error-state headings, set in uppercase.
- **Title** (400, 21px, 1.2 line-height, 0.34em tracking): the persistent wordmark; also balanced with matching text indent.
- **Body** (400, 14px, 1.9 line-height, 0.03em tracking): explanatory or error prose, constrained to approximately 46 characters where used.
- **Label** (400, typically 10–13px, 0.14–0.34em tracking): tuning labels, status, legend, buttons, plate captions, pitch labels, and catalog annotations. Interface labels are predominantly uppercase; note names retain musical case and symbols.

### Named Rules

**The One-Face Rule.** Use Marcellus for display, prose, controls, canvas labels, and plate captions; hierarchy must not rely on introducing a modern sans-serif.

**The Engraved Capital Rule.** Controls and chrome use small uppercase text with generous tracking. Wider tracking belongs to shorter, ceremonial phrases; dense operational labels stay near the 0.14–0.18em range.

## Layout

The stage is a fixed, full-viewport canvas. All DOM interface elements float above it and do not reflow the chart: top chrome sits at z-index 5, the tuning panel at 6, the entry veil at 20, and the blocking error field at 30. The hidden camera video is an input source only and never occupies layout space.

Desktop chrome uses a 26px left/right inset and begins 22px from the top. The wordmark anchors the upper left, the Tune control the upper right, the gesture legend the lower left, and status the lower right. The tuning panel is 268px wide, 26px from the right, and begins 70px from the top. Its 22px internal padding, 16px field intervals, 7px label-to-control gap, and 8–10px control padding create a compact observatory-instrument density.

The canvas chart uses 12 horizontal pitch rows between 9% and 84% of viewport height. Labels begin at x=34px; rules run from x=74px to 30px short of the right edge. Each row carries 24 subdivisions, with a longer tick every sixth division. The aurora horizon is fixed 84px above the bottom, leaving the chart caption and edge chrome legible.

At 640px and below, the panel becomes fluid between 12px side insets, top chrome tightens to 16px, the legend moves to 16px/14px with smaller type, and status rises to 96px above the bottom to avoid collision. Entry runes wrap and contract from 150px to 118px. The canvas remains full bleed; responsive behavior compresses chrome rather than turning the experience into stacked cards.

The spacing rhythm is intentionally mixed: a restrained 4/8/16px operational sequence inside controls, 22–26px chrome and panel offsets, and broad 54–56px ceremonial separations on the entry veil.

### Named Rules

**The Full-Plate Rule.** The chart always owns the viewport. Controls overlay it at the edges and must not create a central application shell.

**The Clear Center Rule.** Persistent chrome remains in corners and lower edges so arms, hands, pitch rows, and ignition labels have an unobstructed performance field.

## Elevation & Depth

The default world is flat in the sense of engraved paper, but not visually shallow. Depth comes from translucent indigo veils, nested hairline borders, low-alpha radial nebulae, screen-blended camera imagery, luminous point glows, and animated alpha—not from a stack of elevated cards.

The tuning panel is the one structurally lifted surface. It combines a translucent field, a 1px outer border, a second inset rule 4px inside, and a deep ambient shadow (`0 18px 40px rgba(0,0,0,0.45)`). The entry veil uses a broad radial indigo gradient; the error field uses an almost-opaque ground wash. Neither receives a card silhouette.

### Shadow Vocabulary
- **Panel Depth** (`0 18px 40px rgba(0,0,0,0.45)`): separates the opened tuning instrument from the moving canvas without making it feel like a generic popover.
- **Star Thumb Glow** (`0 0 10px 2px rgba(157,184,255,0.55)`): turns the range thumb into a point source.
- **Ceremonial Title Glow** (`0 0 46px rgba(130,160,255,0.35)`): used only on the large entry wordmark.
- **Observation Hover Glow** (`0 0 34px rgba(140,170,255,0.28), inset 0 0 18px rgba(140,170,255,0.12)`): the active invitation state for the primary entry action.

### Named Rules

**The Luminous Point Rule.** Glow belongs to stars, active spectral paths, the aurora, and ceremonial activation—not to every border or text label.

**The Single Lifted Surface Rule.** Only the tuning panel uses conventional ambient elevation; all other hierarchy is built through opacity, line weight, compositing, and light.

## Shapes

Interface controls and containers are rectilinear with 0px corner radius. Their shape language comes from thin rules, nested frames, and measured padding. The tuning panel repeats the atlas-plate construction with an outer border and a faint inset border, while the canvas itself uses a double-ruled frame 14px and 19px from the viewport edge with 12px corner registration marks.

Circles are semantic celestial geometry, not a general rounding preference. They form stars, slider thumbs, rune diagrams, catalog marks, nova rings, fingertip glows, and point landmarks. Crosses and paired dots expand the catalog vocabulary. Dashed geometry is reserved for measurement and implied celestial construction: ecliptic arcs use a 1/7 dash rhythm, and the hand-distance measure uses a 2/6 rhythm.

### Named Rules

**The Square Instrument Rule.** Buttons, selects, panels, and error actions keep square corners; do not soften the observatory into rounded app chrome.

**The Celestial Circle Rule.** Circular shapes denote stars, orbits, measurements, and ignitions. They should carry meaning rather than decorate unrelated containers.

**The Double-Rule Rule.** Important fields are framed twice at different alpha levels, like an engraved plate, rather than thickened into a single heavy border.

## Components

### Chrome Buttons

Chrome controls are restrained, square, transparent observatory labels.

- **Shape:** 1px hairline border, no fill, no radius.
- **Tune button:** 9px 18px 8px padding; dim label color; 11px uppercase copy with 0.22em tracking.
- **Hover / Focus:** text brightens and the border increases in opacity over 250ms; keyboard focus uses the same visible treatment and removes the browser outline only because the border state replaces it.
- **Expanded:** `[aria-expanded="true"]` holds the bright text and stronger border while the panel is open.
- **Camera ghost toggle:** smaller 5px 12px 4px geometry. `[aria-pressed="true"]` retains the bright state with an accent-tinted border; copy switches between “Visible” and “Hidden.”

### Primary Observation Button

The entry action is ceremonial rather than filled.

- **Shape:** square, transparent, 1px luminous border; 17px 44px 15px padding.
- **Type:** 13px uppercase with 0.34em tracking and matching text indent.
- **Hover / Focus:** border brightens and gains both outer and inset blue-violet glow over 400ms.
- **Loading / Disabled:** opacity drops to 0.45, cursor becomes `wait`, glow is removed, and copy changes to “Opening the dome…”.

### Tuning Panel

The tuning panel is a compact right-edge instrument with a plate-within-a-plate anatomy.

- **Container:** 268px fixed width on desktop, translucent panel field, 1px hairline border, 22px 22px 20px padding, 4px inset rule, ambient panel shadow.
- **Header:** 12px uppercase, 0.26em tracking, dim ink, 18px bottom separation.
- **Fields:** 16px vertical interval. Labels align names left and live numeric outputs right; outputs brighten and reduce tracking.
- **Open motion:** begins 16px to the right, invisible and hidden; opens to x=0 and full opacity with a 350ms `cubic-bezier(0.16, 1, 0.3, 1)` transform and a 300ms opacity/visibility transition.
- **Mobile:** spans between 12px side insets instead of retaining a fixed width.

### Inputs / Fields

- **Selects:** full width, deep translucent indigo fill, 1px hairline border, 8px 10px padding, 13px text, and square corners. Keyboard focus uses a 1px accent outline with 1px offset.
- **Ranges:** transparent 18px interaction area over a 1px track. The 11px circular thumb is a bright star with a compact glow. Keyboard focus adds a 1px accent outline offset by 4px.
- **Scale marks:** ten one-pixel ticks sit 3px below each range; ordinary marks are 4px high and every third mark grows to 6px.
- **Field labels:** 10.5px uppercase, 0.16em tracking, dim ink, 7px above the control.

### Entry Veil

The entry state is a centered, translucent ritual laid over an already animated atlas.

- **Field:** full viewport radial indigo gradient, 24px edge padding, centered text, and no card container.
- **Title and tag:** fluid display wordmark followed by a 13px, widely tracked uppercase proposition.
- **Rite:** three 72px line-art runes explain silence, ignition, and hand distance. The row begins 54px below the tag, wraps when necessary, and uses broad fluid gaps.
- **Exit:** opacity and visibility fade over 1.2s ease after camera, audio, and hand tracking have initialized.
- **Privacy copy:** quiet tertiary text remains attached to the start ritual rather than hidden in settings.

### Legend and Status

The lower edge carries two independent, non-interactive text systems.

- **Legend:** lower left, faint 11px uppercase copy with 0.14em tracking and 2.1 line-height; gesture nouns brighten to dim ink through unitalicized `em` elements.
- **Status:** lower right, faint 11px uppercase copy with 0.16em tracking and right alignment.
- **States:** after 2.5 seconds without hands, status reads “Raise your hands into view.” With hands present but no active fingers, it reads “Fists closed — silence held.” It clears while notes are active.

### Living Atlas Canvas

The canvas is the signature component and the primary visual system carrier.

- **Plate frame:** two 1px rules at 14px and 19px insets; brighter 12px L-shaped corner marks; centered 10px caption “TABULA ÆTHERIS · CARTA SONORA” above the lower frame.
- **Chart rows:** 12 engraved pitch rules with note labels and 24 tick subdivisions. Active pitch rows adopt the matching scale-degree hue, brighten, and increase from 1px to 1.2px.
- **Catalog field:** 240 softly twinkling fixed stars plus 26 randomly placed engraved glyphs cycling through circled star, cross, and double-star forms. Two faint dashed great-circle arcs imply chart projection.
- **Atmosphere:** three oversized radial nebulae drift at independent, very slow rates. Their alpha increases with audio energy and slightly with hand-distance morph.
- **Camera ghost:** mirrored cover-fit video at 0.16 alpha with `screen` compositing, followed by a translucent indigo wash. It may be hidden from the tuning panel, but never becomes the dominant image layer.
- **Constellation hands:** 21 landmarks become 1.6px star points linked by 1px, low-alpha bones. Active finger chains brighten to 1.6px spectral paths and terminate in a radial star whose radius grows with voice level and audio energy. A white 2.2px core and adjacent musical note label establish the active pitch.
- **Shimmer measure:** when two hands are present, a dashed line connects palm centers, shifts hue from blue toward magenta with hand distance, and labels the midpoint `SHIMMER 0–100`.
- **Nova rings:** a newly ignited finger emits a ring beginning at 4px radius; it expands by 2.6px per frame while alpha decays by a 0.93 multiplier until invisible.
- **Stardust particles:** active fingertips emit upward, wobbling particles capped at 380 total. Particles shrink and fade over their lifetime while retaining the voice hue.
- **Aurora horizon:** the live waveform sits 84px above the bottom and is drawn in three coincident strokes (9px haze, 4px glow, 1.4px core). Amplitude grows from 34px with audio energy, and hue moves from 200° toward 296° as hands separate.

### Error Field

A blocking failure replaces the ritual with an almost-opaque indigo field.

- **Anatomy:** centered uppercase heading, 46ch explanatory paragraph, and square bordered retry action.
- **Copy world:** errors remain in-world (“The sky is veiled”) while the paragraph names the practical recovery step.
- **States:** separate messages cover audio startup, insecure camera context, camera denial or absence, and model-load failure. Retry dismisses the field and re-enters the observation action.

### Motion Rules

- Ambient canvas motion runs continuously before entry and during play: stars twinkle, nebulae drift, and the atlas remains alive beneath the veil.
- Interface transitions are slow and measured (200–400ms) while state-field transitions are more ceremonial (1–1.2s).
- Hand-distance morph is smoothed toward its target at 0.08 per frame; visual color and audio timbre should change continuously rather than snap.
- Pitch transitions use audio glide; visual labels and row highlights update to the quantized result without detached decorative animation.
- Ignition creates the fastest motion—nova expansion and rising particles—so note-on events read as singular celestial events.

## Do's and Don'ts

### Do:
- **Do** preserve the full-viewport indigo chart as the primary surface, with chrome held to the edges.
- **Do** use hairline geometry, nested rules, ticks, labels, and catalog marks to make new surfaces feel engraved and measured.
- **Do** reserve spectral hues for scale-degree response, active rows, ignited hands, particles, measurement, and the aurora.
- **Do** keep camera imagery mirrored, screen-blended, indigo-tinted, and subordinate to the chart.
- **Do** use square, transparent controls with small tracked capitals and explicit hover, focus, pressed, expanded, loading, and error states.
- **Do** keep canvas motion causally tied to audio energy, voice level, ignition, or hand distance whenever it becomes prominent.

### Don't:
- **Don't** replace the celestial plate with pure black, generic gradients, glassmorphic cards, or a neon hand-skeleton debug aesthetic.
- **Don't** round panels, selects, or buttons; circles belong to celestial data and instrument points.
- **Don't** introduce a sans-serif UI layer or heavy font weights; the one-face engraved hierarchy is part of the instrument.
- **Don't** make every line glow. Persistent chart geometry must remain faint enough for ignition to feel exceptional.
- **Don't** assign spectral color by arbitrary component category or finger identity; preserve the scale-degree hue cycle.
- **Don't** let panels, onboarding, or error containers obscure the performance center with conventional app-shell composition.
