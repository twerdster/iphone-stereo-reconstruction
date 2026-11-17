# Updated browser example

Added 17 November 2026 as a new, project-specific interaction. It is separate from the recovered software and is not the students' implementation.

## What runs

Select a textured patch in generated rectified images, run a horizontal block match and change baseline or focal length to calculate depth.

The right image is an exact horizontal shift of a deterministic generated texture. A 9 × 9 sum-of-absolute-differences search checks disparities 0–56 px on one scanline. This clean, constant-depth example excludes occlusion, distortion, noise and real stereo calibration; its zero error is not an accuracy benchmark.

## Run

Open https://twerdster.github.io/iphone-stereo-reconstruction/ or serve the repository's `docs/` directory with any static HTTP server. For example, from the repository root:

```sh
python3 -m http.server 8000 --directory docs
```

Open `http://localhost:8000`. The demo uses standard Canvas 2D and local browser controls. No additional demo packages, SDKs or credentials are required. Downloads are generated JSON files. No camera permission is requested.

## Implementation

`docs/index.html` contains the controls and factual scope labels; `docs/demo.js` implements the interaction; `docs/demo.css` contains the responsive layout. All generated images/data are illustrative. The clean constant-shift example is new JavaScript, not an OpenCV/iOS port or a validation of the original Q-matrix/disparity scaling.

## Recorded checks

[VALIDATION.json](VALIDATION.json) records 10 passed browser assertions on the new interaction, JSON export where present, local-only requests, error-free JavaScript and a 390-pixel responsive layout. These are interaction assertions on generated/local examples, not accuracy or compatibility benchmarks. Original native application/hardware coverage is unchanged; see [historical recovery notes](../docs/RECOVERY.md).

## Attribution and terms

Original project: Ron Slossberg, Omer Shaked. Supervision: Aaron Wetzler. The new browser example was prepared with Codex assistance in November 2026; Claude reviewed the README wording and factual scope. The new files have a [scoped MIT license](../docs/DEMO-LICENSE.txt); it does not relicense historical code, images, slides, reports or third-party dependencies.
