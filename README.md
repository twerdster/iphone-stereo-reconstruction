# 3D Stereo Reconstruction using iPhones

Block-matching stereo reconstruction using two iPhones mounted together, with video streams synchronized over Bluetooth.

Students: Ron Slossberg, Omer Shaked.

Supervision: Aaron Wetzler.

## Status

The [original student repository](https://github.com/ronslos/stereo_vision) is now pinned as the Git submodule [`source/original`](source/original) at revision `69a76767b2ce74f7b580ddb7b81a43fbb1dd346b`. Student headers identify Ron Slossberg and Omer Shaked. Its application includes stereo calibration/rectification, block-matching depth and GameKit/Bluetooth synchronization. This is historical source, not a verified current iOS release.

## Running

Clone with `git clone --recurse-submodules https://github.com/twerdster/iphone-stereo-reconstruction.git`, or run `git submodule update --init` in an existing clone. The source targets iOS 5.1, with historical OpenCV, isgl3d, PowerVR/Bullet and GameKit APIs. `isgl3d.h` was absent from the inspected checkout. Vendor dependencies retain their own notices and restrictions; linking the original repository is not a new redistribution or license grant. No successful current Xcode build or device run is claimed.

## Original code

The exact original public commit is preserved by a Git submodule instead of copying or altering student history. The inspected upstream contains 561 tracked files and 33 application `.h`/`.m`/`.mm` files; its larger vendor tree must be reviewed under the vendors’ terms before reuse. The pin does not imply that every dependency is present or safe to deploy.

The [source provenance manifest](source/PROVENANCE.json) records the published paths, hashes and any redactions. Original student/third-party notices remain in place. No blanket license is assigned to recovered work. Future ports belong in `updated/` and must be described and tested as updated implementations.

## Links

- [Project entry on Aaron Wetzler's website](https://twerdster.github.io/#3d-stereo-reconstruction-using-iphones)

- [Project page](https://gip.cs.technion.ac.il/last-projects-2012-1.html)
- [Demo](https://www.youtube.com/watch?v=IxVj-QZ1w6k)

## Attribution and Updates

Original student and third-party attribution will be retained. No new license for original source code is implied by this README. Original authors can open an issue to contribute updates or request corrections or removal of their material.

