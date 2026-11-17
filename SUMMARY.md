# iphone-stereo-reconstruction: maintenance context

Read this file, then SKILL.md, README.md and linked recovery/provenance records. Current update: 17 November 2026.

This two-phone iOS project implemented stereo calibration, rectification, disparity calculation and a manual Q-matrix point-cloud calculation, with GameKit peer coordination.

## Original material

The original source remains pinned at 69a76767b2ce74f7b580ddb7b81a43fbb1dd346b. A current build is blocked by missing resources and legacy dependencies; no device or depth-accuracy result is recorded. Original source, submodule pins, images, reports, slides, notices and author-response records are unchanged. [Historical implementation and recovery notes](docs/RECOVERY.md) retain the earlier setup and failed-build evidence; existing PROVENANCE.md or source/PROVENANCE.json remains authoritative where present.

## Updated demo

Select a textured patch in generated rectified images, run a horizontal block match and change baseline or focal length to calculate depth. This is new independent JavaScript/Canvas code in docs/, not a restored or ported historical application. The clean constant-shift example is new JavaScript, not an OpenCV/iOS port or a validation of the original Q-matrix/disparity scaling.

Run https://twerdster.github.io/iphone-stereo-reconstruction/ or `python3 -m http.server 8000 --directory docs` from the repository root. No build, account, SDK or external service is required. Serve docs/ as the GitHub Pages source.

## Checks and review

updated/VALIDATION.json records 10 passing Chromium browser assertions for the new demo, including responsive layout checks; these are scoped interaction checks on synthetic/local examples. No original native build, sensor accuracy or physical-mobile/Safari/Firefox coverage was added. Two Claude CLI editorial passes reviewed the concise README and new-demo guide; useful wording and scope qualifications were checked against code and recovery records. Detailed review records are private.

Preserve attribution, original bytes and licensing boundaries. New demo code has a scoped MIT license in docs/DEMO-LICENSE.txt; it does not cover historical materials or third-party dependencies. Correspondence, personal contact data and machine-specific setup details stay private. Before every commit review and synchronize this file and SKILL.md.
