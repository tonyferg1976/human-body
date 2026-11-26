# human-body

**Body Atlas 3D** — an interactive 3D atlas of the human body, built for a future doctor.

Rotate the body, switch body systems on and off, and click any part to fly the camera to it, highlight it and read about it.

## Features

- **Four body systems** you can layer: organs, skeletal, circulatory and nervous (43 parts in total).
- **Click to explore** — the camera flies to the part, everything else turns see-through, and a panel explains:
  - what it is
  - what it does
  - why doctors care (how it is examined or treated)
  - a "did you know?" fact
  - connected parts you can jump to
- **Search and parts list** grouped by system.
- **Quiz mode** — "Find the femur", three tries per question, with a score.
- Front / back / side views, auto-spin, and a see-through skin outline.
- Works with mouse (drag, scroll, right-drag to pan) and touch (drag, pinch).

## Running it

It's a single self-contained page: open `index.html` in a modern browser. It loads [Three.js r128](https://threejs.org/) from cdnjs, so an internet connection is needed.

To publish it with GitHub Pages: **Settings → Pages → Deploy from a branch → `main` / root**.

## Notes

- The 3D anatomy is a simplified model built from code (spheres, tubes and lathed shapes), so shapes, sizes and positions are approximate.
- Content is for learning, not medical advice.

## Ideas for next steps

- Swap in scan-based open anatomy models (e.g. BodyParts3D or Z-Anatomy — check their licences).
- More systems: muscular, respiratory, digestive, lymphatic.
- More parts and a medically reviewed content pass.
