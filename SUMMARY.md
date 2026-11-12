# Historical student-project archive

## Current source state — 2026-11-12

The [original student repository](https://github.com/ronslos/stereo_vision) is now pinned as the Git submodule [`source/original`](https://github.com/ronslos/stereo_vision/tree/69a76767b2ce74f7b580ddb7b81a43fbb1dd346b) at revision `69a76767b2ce74f7b580ddb7b81a43fbb1dd346b`. Student headers identify Ron Slossberg and Omer Shaked. Its application includes stereo calibration/rectification, block-matching depth and GameKit/Bluetooth synchronization. This is historical source, not a verified current iOS release.

The exact original public commit is preserved by a Git submodule instead of copying or altering student history. The inspected upstream contains 561 tracked files and 33 application `.h`/`.m`/`.mm` files; its larger vendor tree must be reviewed under the vendors’ terms before reuse. The pin does not imply that every dependency is present or safe to deploy.

## Setup and validation

Clone with `git clone --recurse-submodules https://github.com/twerdster/iphone-stereo-reconstruction.git`, or run `git submodule update --init` in an existing clone. The source targets iOS 5.1, with historical OpenCV, isgl3d, PowerVR/Bullet and GameKit APIs. `isgl3d.h` was absent from the inspected checkout. Vendor dependencies retain their own notices and restrictions; linking the original repository is not a new redistribution or license grant. No successful current Xcode build or device run is claimed.

Publication validation covers the source allowlist, SHA-256 provenance, text/XML or project metadata where applicable, and credential/private-material scanning. It is not an end-to-end runtime result. Read README.md and source/PROVENANCE.json before further edits; preserve source/original and existing documents. Any future updated implementation belongs in updated/ with its own requirements, tests, attribution and a clear description of its differences. Do not introduce a blanket license. Review this context file before committing; keep actual validation and source counts accurate.

## Interactive possibilities

The stereo block-matching concept is a strong candidate for an offline OpenCV Python notebook with synthetic or openly licensed stereo pairs. A future demo would be newly updated code; it would not reproduce two-phone capture/Bluetooth behavior.

## Repository presentation

README includes an unchanged original website figure, three factual language/platform/source badges and the original-code section. Student credits, source provenance and build limitations remain intact. No source files, dependencies or licenses changed in this presentation update.

## Local build entrypoint check

A November 2026 Xcode 16.1 check could list the project. The stock simulator build found no compatible destination. A separate unsigned arm64 target build failed on the missing external `HelloGLKit/tile_floor.png` resource; `isgl3d.h` is also absent from the preserved checkout. These checks used a private native-filesystem copy, changed no original project settings, and did not run the app. They establish concrete restoration blockers, not a successful port.
