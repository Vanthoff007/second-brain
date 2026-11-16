# Visual odometry
Links: [Home](../Home.md) · [Visual SLAM](Visual-SLAM.md) · [Sensor fusion](Sensor-Fusion.md) · [Papers](../Research/Papers.md)

## Updates — 2026-11-16
- **Problem: monocular scale drift.** Bundle adjustment cannot fix scale in a monocular system, because scaling translations and landmarks together leaves the reprojections unchanged, so scale error accumulates as new keyframes and landmarks are added [source fact, 2611.11934].
- **Method (S²D-FVO, 2611.11934):** a light depth network (14.85 M parameters) supplies the scale reference; bundle adjustment uses tangent-space angular residuals on the unit sphere rather than pixel residuals, so the same code serves different fisheye models; a median-depth term regularises scale. Bundle adjustment also replaces the pose network while the depth network is trained without labels. [source fact]
- **Results [measured, authors]:** KITTI-360 average ATE 31.5 m against 335.4 m for OV²SLAM, both with full tracking; translational drift 4.45% against 57.7%. TUM-VI room sequences: mean ATE 0.012 m. About 10 FPS on an Intel Core Ultra 9 285K with an RTX 5090 (tracking 70.7 ms/frame, depth network 8.5 ms/frame).
- **Analysis:** the runtime is from a desktop GPU; the 8.5 ms depth step is the part that might move to an embedded target, the learned matcher (SuperPoint + SphereGlue) is the larger cost. Not tested on our hardware. Full context: [Weekly 2026-11-16](../Weekly/2026-11-16.md).
