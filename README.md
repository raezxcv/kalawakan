# Kalawakan 🌌

> **Kalawakan** *(Tagalog for "outer space" / "cosmos")* is an interactive 3D WebGL particle simulation featuring real-time AI hand gesture tracking. Morph between intricate celestial bodies, biological structures, and mythic creations using your hands or keyboard/mouse.

Powered by **Three.js** and **Google MediaPipe Hand Landmarker**, the experience simulates **20,000 glowing particles** transitioning smoothly across parametric 3D point clouds against a procedural cinematic nebula sky.

---

## ✨ Features

- **20,000 Dynamic Particles**: Real-time morphing animations between complex 3D parametric point clouds with custom GLSL shaders, point sizing, and soft depth attenuation.
- **AI Hand Tracking**: Real-time multi-hand landmark detection running directly in the browser via WebAssembly/GPU acceleration with Google MediaPipe.
- **Cinematic Procedural Universe**: Dynamic starfield and procedural Milky Way nebula skybox with parallax drift and cosmic dust lanes.
- **Zero Build / Self-Contained**: Pure vanilla web implementation. No bundlers or build steps required.
- **Dual Input Modes**: Seamless support for both webcam hand gestures and classic mouse/keyboard controls.

---

## 🖐️ Hand Gesture Controls

Enable camera access to interact with the particle system using your hands. Everything runs locally on your device with complete privacy.

| Hand | Action | Effect |
| :--- | :--- | :--- |
| **Left Hand** *(Object Selector)* | **1 Finger** (Index) | Morph to **Saturn** 🪐 |
| | **2 Fingers** (Peace) | Morph to **DNA Double Helix** 🧬 |
| | **3 Fingers** | Morph to **Chibi Robot** 🤖 |
| | **4 Fingers** | Morph to **Dragon** 🐉 |
| | **5 Fingers** (Open Palm) | Morph to **Spiral Galaxy** 🌌 |
| **Right Hand** *(Motion Controller)* | **Open / Close Palm** | **Expand / Collapse** particle dispersion |
| | **Push Closer / Pull Away** | **Zoom In / Out** (depth scaling) |
| | **Move & Tilt Palm** | **Rotate & Roll** the 3D model in space |

> *Tip: Click the **"Swap Hands"** button on the bottom toolbar if you prefer using your right hand for shape selection and your left hand for motion control.*

---

## ⌨️ Mouse & Keyboard Fallback

No webcam? You can skip the camera and use full desktop controls:

- **Keys `1` – `5`**: Switch between shapes:
  - `1`: Saturn
  - `2`: DNA
  - `3`: Robot
  - `4`: Dragon
  - `5`: Galaxy
- **Left Click + Drag**: Rotate the camera / model around any axis
- **Mouse Wheel (Scroll)**: Expand / collapse particle dispersion
- **Shift + Mouse Wheel**: Zoom camera in / out

---

## 🪐 Morphing Shapes

1. **Saturn**: Gas giant featuring realistic atmospheric bands, Cassini and Encke divisions in the rings, planet-on-ring shadows, and orbiting moons (Titan and an icy moon).
2. **DNA**: Rotating double helix spiral with connecting base pairs.
3. **Robot**: 3D chibi-style robot with glossy visor, glowing digital eyes, chest emblem, and waving arm.
4. **Dragon**: Mythical serpentine dragon complete with scaled body, swan neck, horned head, bat wings, and spade tail.
5. **Galaxy**: Majestic deep-space spiral galaxy with core bulge, spiral dust arms, and a faint halo.

---

## 🚀 Getting Started

Because modern browsers enforce strict security policies (`getUserMedia` requires a secure context), camera access requires running via `localhost` or HTTPS.

### Quick Start with a Local Server

You can serve the project using any lightweight local server:

**Using Python:**
```bash
python -m http.server 8000
```
Then navigate to: `http://localhost:8000/hand-morph.html`

**Using Node / npx:**
```bash
npx serve .
```

**Using VS Code:**
- Install the **Live Server** extension.
- Right-click `hand-morph.html` and select **"Open with Live Server"**.

### GitHub Pages Deployment

To host Kalawakan live on GitHub Pages:
1. Go to repository **Settings** > **Pages**.
2. Under **Build and deployment**, select branch `main` and root `/`.
3. Save, and your app will be accessible at:
   `https://<your-username>.github.io/kalawakan/hand-morph.html`

---

## 🛠️ Built With

- [Three.js](https://threejs.org/) — 3D WebGL graphics and scene management
- [Google MediaPipe Tasks Vision](https://developers.google.com/mediapipe/solutions/vision/hand_landmarker) — Real-time on-device machine learning for hand tracking
- Vanilla JavaScript & GLSL shaders