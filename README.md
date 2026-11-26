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

Open the GitHub Pages site, or serve the folder with any web server (for example `python3 -m http.server`) and open `index.html`. Opening the file directly from disk won't work, because the page loads `anatomy.json` and `anatomy.bin` alongside it. It loads [Three.js r128](https://threejs.org/) from cdnjs, so an internet connection is needed.

### Files

- `index.html` — the app (interface, descriptions, quiz, 3D viewer)
- `anatomy.bin` — the 3D meshes (about 4 MB, roughly 470,000 triangles)
- `anatomy.json` — which mesh belongs to which part, plus the paths for the nerves and limb blood vessels and the see-through skin outline

To publish it with GitHub Pages: **Settings → Pages → Deploy from a branch → `main` / root**.

## Notes

- Organs, bones, the brain, the heart and the main blood vessels are real 3D anatomy from BodyParts3D, simplified for the web.
- BodyParts3D has no nerves outside the brain and no arm or leg blood vessels, so the spinal cord, spinal nerves, arm nerves, sciatic and vagus nerves, and the arm and leg arteries and veins are drawn as tubes routed along the real bones. Their paths are approximate.
- Content is for learning, not medical advice.
- The first version, with all shapes built from code, is kept on the `backup/v1.0-simple-shapes` branch.

## Credits

3D anatomy: **BodyParts3D**, © The Database Center for Life Science, licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) ([database site](https://dbarchive.biosciencedbc.jp/en/bodyparts3d/)). The meshes were taken from the STL conversion at [Kevin-Mattheus-Moerman/BodyParts3D](https://github.com/Kevin-Mattheus-Moerman/BodyParts3D), then decimated, merged into one binary file and rescaled.

## Ideas for next steps

- Add the muscular system (BodyParts3D includes muscles).
- More systems: muscular, respiratory, digestive, lymphatic.
- More parts and a medically reviewed content pass.
