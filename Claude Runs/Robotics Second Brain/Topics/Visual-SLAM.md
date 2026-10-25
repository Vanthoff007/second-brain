# Visual SLAM

## Updates — 2026-10-26
- **AnchorFlow-VIO** (mono grayscale + IMU, Basalt-derived, LaMAria) and **CAOS-SLAM** (class-agnostic dynamic-object handling) appeared this week; **Lunar front-end matching evaluation** compares feature matchers for camera-only localisation. All [source fact] from abstracts; see [Papers](../Research/Papers.md).
- **Analysis:** front-end choice and dynamic-object handling are the recurring robustness levers; none of these has been run on our hardware yet. Candidate experiment (untested): run AnchorFlow-VIO against our own recordings on the target compute — see [Compute platforms](../Hardware/Compute-Platforms.md).
