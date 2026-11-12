# iphone-stereo-reconstruction: maintenance context

Read this file first, then SKILL.md and README.md. This context describes the repository as of 2026-11-12.

## Purpose and current source

Two-phone stereo calibration/rectification, StereoBM/StereoSGBM disparity and manual Q-matrix XYZ calculation, with historical GameKit (GKSession) peer coordination.

source/original pins ronslos/stereo_vision at 69a76767b2ce74f7b580ddb7b81a43fbb1dd346b. OpenCVCalculations.mm contains stereoCalibrate, stereoRectify, StereoBM/StereoSGBM and a manual Q-based XYZ loop after 8-bit disparity conversion/median filtering; SessionManager.mm uses GKSession. Upstream and vendor notices are unchanged.

## Use and validation

Clone with --recurse-submodules or git submodule update --init --recursive. Inspect the Xcode project under source/original/. Read source/PROVENANCE.json.

Recorded November 2026 Xcode 16.1 check listed the project; simulator build had no compatible destination. Unsigned arm64 build failed on missing HelloGLKit/tile_floor.png. No current app build or device/numerical/benchmark result.

iOS 5.1-era OpenCV/isgl3d/PowerVR/Bullet/GameKit APIs; isgl3d.h and resources missing. No current metric depth or disparity-scaling validation. No updated port or notebook. 561 tracked upstream files and 33 application source files are inventory counts.

## Documentation maintenance

The 2026-11-12 documentation revision organizes the README around implementation, available source, setup, recorded checks and limits. It preserves historical visuals and links, with captions separating historical results from updated examples. No runnable code, source provenance, pinned revisions, licenses or validation results changed in this revision. Recorded earlier tests were not rerun for the prose-only edits.

Preserve original source and authorship. New ports belong under updated/ and require their own scope/validation. Do not infer a blanket license from recovery. Review this file and SKILL.md before every commit and synchronize changes to workflow, commands, validation or status. Check relative links and figure rendering; never describe inventory counts or component tests as full-application validation.

Two actual Claude editorial review rounds on 2026-11-12 covered the README and related changed documentation, including context files, component guides and applicable algorithm/build notes or schematic text. Useful qualifications were checked against source, preserved project records and saved validation logs, then applied. Editorial review adds no runtime coverage.
