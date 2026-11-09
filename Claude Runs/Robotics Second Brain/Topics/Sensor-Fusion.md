# Sensor fusion

## Updates — 2026-11-09
Abstract-level notes from the 2026-11-02 → 2026-11-08 window ([Weekly 2026-11-09](../Weekly/2026-11-09.md)); all [source fact] unless stated.
- **LiDAR-camera extrinsics:** *Auditing Targetless Camera-LiDAR Extrinsic Correction before Recursive Use* (2611.04397) asks when a corrected transform may be admitted downstream; *MiCaDe* (2611.04912) detects miscalibration change online. Earlier: VeriCalib in [Papers](../Research/Papers.md).
- **LIVO:** *FREE-LIVO* (2611.07463) relaxes the fixed LiDAR-camera pose assumption.
- **Degraded sensing:** *Tightly Coupled Magnetic-Inertial SLAM* (2611.03106) for dust/smoke/GNSS-denied sites.
- **Measured example:** the reflection-robust VIO front-end in [Visual SLAM](Visual-SLAM.md) used FAST-LIO2 (Livox Mid-360) as the reference trajectory.
- **Analysis:** extrinsic validation is a low-cost safeguard worth adding before trusting any fused estimate; not yet tested on our rigs.
