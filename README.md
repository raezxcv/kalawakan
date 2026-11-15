# Kalawakan

> **Kalawakan** *(Tagalog for "outer space" / "cosmos")* is an interactive 3D WebGL particle simulation featuring real-time vision hand tracking. Morph smoothly between celestial bodies, biological structures, and complex forms using your hands, touch, or mouse.
>
> - **Creator**: [rei](https://raelyivanreyes.vercel.app/)
> - **Portfolio**: [https://raelyivanreyes.vercel.app/](https://raelyivanreyes.vercel.app/)

Powered by **Three.js** and **Google MediaPipe Hand Landmarker**, the experience simulates up to **20,000 glowing particles** transitioning smoothly across parametric 3D point clouds against a procedural nebula sky.

---

## Features

- **Dynamic Particles**: Real-time morphing animations between parametric 3D point clouds with custom GLSL shaders, soft depth attenuation, and adaptive performance scaling (12,000 particles on mobile, 20,000 on desktop).
- **Vision Hand Tracking**: Real-time multi-hand landmark detection running locally in the browser via WebAssembly and GPU acceleration with Google MediaPipe. Video is processed 100% on-device and is never stored or transmitted.
- **Minimalist Modern Glassmorphism**: Polished monochrome UI with frosted glass cards, fluid entrance animations, and clean neutral typography.
- **Cinematic Procedural Universe**: Dynamic starfield and procedural nebula skybox with parallax drift and cosmic dust lanes.
- **Mobile-Optimized Experience**: Adaptive particle count, throttled hand landmark inference, prominent responsive camera preview with expand toggle, and native touch gestures (drag to rotate, pinch to zoom and expand).
- **Zero Build / Standalone**: Pure vanilla web implementation. No bundlers or dependencies required to run.
- **Multi-Input Controls**: Full support for webcam hand tracking, mobile multi-touch, and keyboard/mouse shortcuts.

---

## Hand Tracking Controls

Enable camera access to interact with the particle system using your hands. All processing is local and private.

| Hand | Action | Effect |
| :--- | :--- | :--- |
| **Left Hand** *(Object Selector)* | **1 Finger** (Index) | Morph to **Saturn** |
| | **2 Fingers** (Peace) | Morph to **DNA Double Helix** |
| | **3 Fingers** | Morph to **Robot** |
| | **4 Fingers** | Morph to **Dragon** |
| | **5 Fingers** (Open Palm) | Morph to **Galaxy** |
| **Right Hand** *(Motion Controller)* | **Open / Close Palm** | **Expand / Collapse** particle dispersion |
| | **Push Closer / Pull Away** | **Zoom In / Out** (depth scaling) |
| | **Move and Tilt Hand** | **Rotate and Roll** the 3D model |

> *Tip: Click the **"Swap (S)"** button on the bottom toolbar to switch which hand selects shapes and which hand controls motion.*

---

## Mobile and Touch Controls

- **Single Finger Drag**: Rotate the 3D model in space.
- **Two-Finger Pinch / Spread**: Zoom in/out and expand/collapse particle field.
- **Camera Preview**: Prominent display on mobile screens with an expand toggle for full-width view.
- **Floating Toolbar**: Single-row clean pill navigation for fast shape switching.
- **Controls Guide**: Tap `[ Controls Guide ]` in the top left to show or hide gesture instructions.

---

## Mouse and Keyboard Controls

When camera access is disabled, full desktop controls are supported:

- **Keys 1 to 5**: Select shapes:
  - `1`: Saturn
  - `2`: DNA
  - `3`: Robot
  - `4`: Dragon
  - `5`: Galaxy
- **Left Click + Drag**: Rotate the model around any axis
- **Mouse Wheel**: Expand / collapse particles
- **Shift + Mouse Wheel**: Zoom in / out
- **Key S**: Swap hand roles

---

## Morphing Shapes

1. **Saturn**: Gas giant featuring atmospheric bands, Cassini and Encke ring divisions, planet shadows, and orbiting moons.
2. **DNA**: Rotating double helix spiral with connecting base pairs.
3. **Robot**: 3D chibi robot with visor, glowing eyes, chest emblem, and waving arm.
4. **Dragon**: Mythical serpentine dragon with scaled body, swan neck, horned head, bat wings, and spade tail.
5. **Galaxy**: Deep-space spiral galaxy with galactic core bulge, spiral arms, and faint halo.

---

## Getting Started

Because browsers require a secure context for `getUserMedia` camera permissions, run the project on `localhost` or via HTTPS.

### Running Locally

**Using Python:**
```bash
python -m http.server 8000
```
Open `http://localhost:8000`

**Using Node:**
```bash
npx serve .
```

---

## License and Credits

Created by [rei](https://raelyivanreyes.vercel.app/).
Built with Three.js and Google MediaPipe.
