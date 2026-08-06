# ÆTHER — Product

A browser instrument played on the open air. The webcam watches the player's
hands; MediaPipe HandLandmarker charts them, Web Audio sings for them. No
install, no account, no server: one HTML file, camera frames never leave the
device.

## The mechanism (user's spec, verbatim intent)

- **Closed fist = silence.** Absolute; the resting state of the instrument.
- **Each extended finger ignites a note.** Up to five per hand, ten total.
  Fingers are read with hysteresis so notes hold steady, not flicker.
- **Hand height = pitch.** Higher hand, higher note, quantized to the chosen
  scale. Left hand plays an octave below the right.
- **Distance between hands = timbre morph.** Close together: soft nebula glass
  (pure sine/triangle, dark filter). Wide apart: solar bell shimmer (octave
  partial + FM, open filter). Continuous, audible, and visualized.
- **Ethereal, adjustable sound.** Tuning panel: scale (5 modal flavors), root
  note, reverb/echo "Space", shimmer reach, glide, loudness, camera ghost.

## Audience & scene

One person at a desk or standing in a room, decent light, laptop/desktop with a
webcam, sound on. Mobile works but the instrument is built for arms-width play.

## Constraints

- Chrome/Edge/Firefox current; camera requires localhost or HTTPS.
- MediaPipe tasks-vision 0.10.14 + hand model stream once from CDN, then run
  locally on-device (GPU delegate).
- No recording, no network calls beyond the CDN model fetch.

## Assumptions (inferred, user said "create this now")

- Web app (not native) was the right medium for camera + instant play.
- Pentatonic default so free-air playing always sounds consonant.
- Star-atlas visual world chosen to satisfy "out of this world" — see the
  direction contract in `index.html` head and DESIGN.md.

## Direction

Antique celestial cartography, alive: deep indigo plate, engraved declination
rows labeled with note names, hands drawn as constellations whose ignited
fingertips are catalog stars, audio-reactive aurora at the horizon. Marcellus
display type. Category default refused: black void + neon skeleton debug overlay.
