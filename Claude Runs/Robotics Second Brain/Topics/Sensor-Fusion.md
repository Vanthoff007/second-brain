# Sensor fusion

## Updates — 2026-11-09
Abstract-level notes from the 2026-11-02 → 2026-11-08 window ([Weekly 2026-11-09](../Weekly/2026-11-09.md)); all [source fact] unless stated.
- **LiDAR-camera extrinsics:** *Auditing Targetless Camera-LiDAR Extrinsic Correction before Recursive Use* (2611.04397) asks when a corrected transform may be admitted downstream; *MiCaDe* (2611.04912) detects miscalibration change online. Earlier: VeriCalib in [Papers](../Research/Papers.md).
- **LIVO:** *FREE-LIVO* (2611.07463) relaxes the fixed LiDAR-camera pose assumption.
- **Degraded sensing:** *Tightly Coupled Magnetic-Inertial SLAM* (2611.03106) for dust/smoke/GNSS-denied sites.
- **Measured example:** the reflection-robust VIO front-end in [Visual SLAM](Visual-SLAM.md) used FAST-LIO2 (Livox Mid-360) as the reference trajectory.
- **Analysis:** extrinsic validation is a low-cost safeguard worth adding before trusting any fused estimate; not yet tested on our rigs.

## Updates — 2026-11-16
- **Camera–IMU consistency as a fusion gate:** NIF-VIO (2611.13662) tests whether image-based motion and IMU preintegration agree before trusting full fusion, and drops to selective IMU constraints when they do not. Details in [Visual SLAM](Visual-SLAM.md). [measured by authors]
- **Calibration is not constant over a long run:** SLAM Dunk estimates stereo extrinsics and focal lengths per 5 s chunk and a gyroscope scale/misalignment matrix; the two together cut mean ATE by 58% on LaMAria training recordings [measured by authors, offline].
- **Semantics feeding odometry:** HiPFuse (2611.14025) replaced only the semantic front end of a LiDAR–inertial odometry system and reduced ATE RMSE by 10.6% on average over two outdoor sequences [measured by authors, Jetson AGX Orin].
- **LiDAR–camera, abstract only:** RAPA (2611.12129) target-based calibration; GEMOR-GS (2611.13528) extrinsic refinement inside LiDAR–inertial–visual Gaussian-splatting SLAM; QVS-LIVO RiskMap (2611.16205) camera view selection for multi-camera LIVO.
- See [Weekly 2026-11-16](../Weekly/2026-11-16.md).
