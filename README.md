# ÆTHER

**An instrument played on the open air.**

Your webcam watches your hands; MediaPipe charts them as constellations on a
living star atlas, and Web Audio sings for them. A theremin, but out of this
world.

![status](https://img.shields.io/badge/runs-entirely_on--device-4c5fd7)

## How to play

| Gesture | Sound |
|---|---|
| Closed fist | Silence |
| Each extended finger | Ignites its own note (up to 10 voices) |
| Hand height | Pitch, quantized to the chosen scale |
| Hands close together | Soft nebula glass (sine/triangle, dark filter) |
| Hands wide apart | Solar bell shimmer (octave partial + FM, open filter) |

Your left hand plays an octave below your right. Everything flows through a
long convolution reverb and a feedback echo, so it always sounds ethereal.

Open the **Tune** panel for five scales (Celestial pentatonic, Lydian dream,
Dorian haze, Whole-tone drift, Harmonic nebula), root note, reverb space,
shimmer reach, glide, loudness, and the camera-ghost toggle.

## Run it

Cameras only open on a secure page, so serve the file over localhost:

```sh
python3 -m http.server 8471
# then open http://localhost:8471 in Chrome / Edge / Firefox
```

Click **Begin the observation**, allow the camera, raise your hands.

## Privacy

Camera frames never leave your device. Hand tracking is
[MediaPipe HandLandmarker](https://ai.google.dev/edge/mediapipe/solutions/vision/hand_landmarker)
— the model streams once from a CDN, then runs locally (GPU-accelerated).
Nothing is recorded or sent anywhere.

## Stack

One HTML file. No build, no dependencies to install.

- [MediaPipe tasks-vision](https://www.npmjs.com/package/@mediapipe/tasks-vision) 0.10.14 for hand tracking
- Web Audio API — 10-voice synth (dual osc + shimmer partial + FM), convolution reverb, feedback delay, compressor
- Canvas 2D — engraved star-atlas plate, constellation hands, nova rings, stardust, audio-reactive aurora horizon
