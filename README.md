# 3D Stereo Reconstruction using iPhones

<p align="center"><img src="assets/project-preview.jpg" alt="Original two-phone stereo reconstruction project figure" width="380"></p>

![Code](https://img.shields.io/badge/code-Objective--C%20%2F%20C%2B%2B-blue)
![Platform](https://img.shields.io/badge/platform-iOS%205.1-lightgrey)
![Source](https://img.shields.io/badge/source-pinned%20original%20source-orange)

This project was designed to reconstruct a scene from stereo image pairs acquired by two iPhones. The recovered application source implements camera calibration, rectification, disparity calculation, a point-cloud calculation and GameKit (`GKSession`) peer coordination. These operations have not been validated on current devices.

Students: Ron Slossberg, Omer Shaked. Supervision: Aaron Wetzler.

*The figure is unchanged historical project imagery; it is not a new reconstruction or compatibility result.*

## Source and implementation

The students' [ronslos/stereo_vision](https://github.com/ronslos/stereo_vision) repository is pinned as the `source/original` Git submodule at `69a76767b2ce74f7b580ddb7b81a43fbb1dd346b`. Student headers identify Ron Slossberg and Omer Shaked. The pinned revision and upstream history are unchanged; [provenance](source/PROVENANCE.json) records the source reference.

The inspected upstream contains 561 tracked files, including 33 application `.h`/`.m`/`.mm` files. Those are inventory counts, not test counts.

`stereo_vision/OpenCVCalculations.mm` contains OpenCV stereo calibration, rectification and `StereoBM`/`StereoSGBM` disparity calculation. Its `reconstruct` function converts disparity to an 8-bit display map, applies a median filter, and uses entries of the calibration `Q` matrix to calculate per-pixel XYZ values; the standard OpenCV `reprojectImageTo3D` call is commented out. `SessionManager.mm` coordinates peers using the historical GameKit API. These identify the implemented operations; they do not establish synchronization accuracy, depth accuracy or current device compatibility.

## Inspect the project

```sh
git clone --recurse-submodules https://github.com/twerdster/iphone-stereo-reconstruction.git
cd iphone-stereo-reconstruction
```

For an existing checkout, run `git submodule update --init --recursive`. Inspect the Xcode project under `source/original/`. It targets iOS 5.1 and references historical OpenCV, isgl3d, PowerVR/Bullet and GameKit APIs. A complete restoration needs compatible dependencies, missing resources, signing and two suitable physical devices. There is no verified current installation procedure.

## Validation and limitations

The recorded November 2026 check used Xcode 16.1 on a private copy without changing original settings. Xcode could list the project; a stock simulator build found no compatible destination. An unsigned arm64 target build then failed on the absent external `HelloGLKit/tile_floor.png` resource. The checkout also lacks `isgl3d.h`.

These are project-inspection and failed-build results. No successful current app build, device capture, peer synchronization, numerical comparison or reconstruction benchmark has been recorded. Source inspection does not establish metric depth accuracy or validate the disparity scaling used by the manual XYZ calculation. The preserved vendor tree has its own terms and must be reviewed before reuse. The archive contains no updated port or notebook.

## Original code and attribution

Student and third-party notices remain intact, and no blanket license is added. Authors can open an issue to contribute updates, correct attribution or request removal.

On 2026-11-12, Ron Slossberg permitted Aaron Wetzler to post the project on Aaron Wetzler's website and to use the project code, and welcomed a rewrite for modern hardware. Omer Shaked separately agreed to Aaron Wetzler using the code. No rewrite or successful current-device build has been completed here. These replies do not replace third-party terms or add a repository-wide license.

## Links

- [Project entry on Aaron Wetzler's website](https://twerdster.github.io/#3d-stereo-reconstruction-using-iphones)
- [Project page](https://gip.cs.technion.ac.il/last-projects-2012-1.html)
- [Demo](https://www.youtube.com/watch?v=IxVj-QZ1w6k)
