# Visual SLAM

## Updates — 2026-10-26
- **AnchorFlow-VIO** (mono grayscale + IMU, Basalt-derived, LaMAria) and **CAOS-SLAM** (class-agnostic dynamic-object handling) appeared this week; **Lunar front-end matching evaluation** compares feature matchers for camera-only localisation. All [source fact] from abstracts; see [Papers](../Research/Papers.md).
- **Analysis:** front-end choice and dynamic-object handling are the recurring robustness levers; none of these has been run on our hardware yet. Candidate experiment (untested): run AnchorFlow-VIO against our own recordings on the target compute — see [Compute platforms](../Hardware/Compute-Platforms.md).

## Updates — 2026-11-09
- **Reflection-robust stereo VIO (2611.05938, [measured] by authors):** virtual features from specular floors are triangulated below the ground plane. A scalar Kalman filter with NIS gating (gate 10, 1 DoF) estimates ground height; only features below it by an uncertainty margin are rejected. Wrapped around VINS-Fusion and DynaVINS on 8 self-collected sequences, referenced to FAST-LIO2. Median ATE RMSE e.g. E4 0.722 → 0.335 m, N3 0.845 → 0.460 m; slightly worse on N7 (highly specular floor) and E11 (dark corridor). Filter 4.93 ms/update; VINS-Fusion 15.0 → 14.7 Hz; floor segmenter 8.96 ms/image. Desktop i9 + RTX 4080 laptop GPU, not embedded.
- **Analysis:** a cheap, geometry-based gate that is front-end agnostic; the segmenter, not the filter, is the cost to budget on an embedded target.
- Loop closure / matching this week (abstracts only): UniLoop 2611.06378, scale anchoring for VGGT-based SLAM 2611.06308, CoReMatch 2611.03932, UAV on-demand features 2611.07687. See [Weekly 2026-11-09](../Weekly/2026-11-09.md), [Papers](../Research/Papers.md).
