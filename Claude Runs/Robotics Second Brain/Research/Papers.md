# Papers
Entries added by weekly digests. Labels: [source fact] from abstract; [measured] author-reported.

## Updates — 2026-10-26
- **Which Depth Estimator for Jetson AGX Orin?** (NODAR, 2026-10-19) — TensorRT FP16 benchmark of 9 depth families on Orin 64GB. Problem: [Edge AI](../Topics/Edge-AI.md). Hardware: [Compute platforms](../Hardware/Compute-Platforms.md). https://www.alphaxiv.org/abs/2610.27199
- **SSIO: Self-Supervised Inertial Odometry** (2026-10-19) — trains IMU odometry without GT trajectories. Problem/method: [Learned inertial odometry](../Topics/Learned-Inertial-Odometry.md). https://www.alphaxiv.org/abs/2610.25988
- **AnchorFlow-VIO** (2026-10-19) — Basalt-derived mono VIO on LaMAria. [Visual SLAM](../Topics/Visual-SLAM.md). https://www.alphaxiv.org/abs/2610.26210
- **CAOS-SLAM** (2026-10-19) — class-agnostic object-aware vSLAM, dynamic scenes. [Visual SLAM](../Topics/Visual-SLAM.md). https://www.alphaxiv.org/abs/2610.26633
- **Evaluation of Front-End Feature Matching for Lunar Visual SLAM** (2026-10-22). https://www.alphaxiv.org/abs/2610.30774
- **Learning Wheel Motion Uncertainty for Degeneracy-Aware LIO** (2026-10-19). https://www.alphaxiv.org/abs/2610.26550
- **Foundation4D** (NVIDIA, 2026-10-21). https://www.alphaxiv.org/abs/2610.30340
- **VeriCalib** (2026-10-20). https://www.alphaxiv.org/abs/2610.28791
- **AgentDP** (2026-10-22). https://www.alphaxiv.org/abs/2610.30760
- **SPAR** (2026-10-19). https://www.alphaxiv.org/abs/2610.26487

## Updates — 2026-11-09
- **Reflection-Robust Stereo VIO via Kalman-Filtered Ground-Height Estimation** (KAIST, 2026-11-04) — [measured] ATE better on 6/8 sequences with VINS-Fusion; +4.93 ms per update. [Visual SLAM](../Topics/Visual-SLAM.md), [Edge AI](../Topics/Edge-AI.md). https://www.alphaxiv.org/abs/2611.05938
- **FREE-LIVO** (2026-11-05). [Sensor fusion](../Topics/Sensor-Fusion.md). https://www.alphaxiv.org/abs/2611.07463
- **Not Losing Your Way: VIO drift via on-demand feature creation** (2026-11-05). https://www.alphaxiv.org/abs/2611.07687
- **Scale Anchoring ... for VGGT-Based SLAM** (2026-11-04). https://www.alphaxiv.org/abs/2611.06308
- **UniLoop** (2026-11-04). https://www.alphaxiv.org/abs/2611.06378
- **CoReMatch** (2026-11-02). https://www.alphaxiv.org/abs/2611.03932
- **Energy-Aware Open-Vocabulary Detection Scheduling** (2026-11-05). [Edge AI](../Topics/Edge-AI.md). https://www.alphaxiv.org/abs/2611.07663
- **Aero-VPA** (2026-11-03). https://www.alphaxiv.org/abs/2611.04392
- **Auditing Targetless Camera-LiDAR Extrinsic Correction** (2026-11-03). [Sensor fusion](../Topics/Sensor-Fusion.md). https://www.alphaxiv.org/abs/2611.04397
- **MiCaDe** (2026-11-03). https://www.alphaxiv.org/abs/2611.04912
- **Tightly Coupled Magnetic-Inertial SLAM** (2026-11-02). https://www.alphaxiv.org/abs/2611.03106
- **IMUDINO** (2026-11-05). https://www.alphaxiv.org/abs/2611.07437
- **VisionSIM** (2026-11-05). https://www.alphaxiv.org/abs/2611.08368
- **Open-Source Stack for Vision-Based Rover Navigation** (2026-11-05). https://www.alphaxiv.org/abs/2611.08100
Full context: [Weekly 2026-11-09](../Weekly/2026-11-09.md).

## Updates — 2026-11-13
- **Task-Driven Closed-Loop Design Optimization of Passively Morphing Quadrotors for Contact-Mediated Narrow Gap Traversal** — width 31.3 → 14.1 cm, passes a 15 cm opening at 2 m/s reference speed, NMPC control [measured, as quoted in Weekly Robotics #384]. Paper URL not resolved (tracked redirect). See [Daily 2026-11-13](../Daily/2026-11-13.md).

## Updates — 2026-11-16
- **RGB-D SLAM on the Edge: Benchmarking and Profiling RTAB-Map and ORB-SLAM3 on the Raspberry Pi 5** (IIT Bombay, IIT Mandi, 2026-11-12) — [measured] ORB-SLAM3 26–62 ms/frame, RTAB-Map 150–462 ms/frame (per-frame worst case). Problem: [Edge AI](../Topics/Edge-AI.md). Method and findings: [Visual SLAM](../Topics/Visual-SLAM.md). Hardware: [Compute platforms](../Hardware/Compute-Platforms.md). https://www.alphaxiv.org/abs/2611.16472
- **SLAM Dunk: A Recipe for Long-Horizon Egocentric SLAM in the Wild** (UC Berkeley, 2026-11-15) — [measured] LaMAria training ATE 1.02 → 0.43 m with time-varying camera calibration and gyroscope intrinsics; offline. [Visual SLAM](../Topics/Visual-SLAM.md), [Sensor fusion](../Topics/Sensor-Fusion.md). https://www.alphaxiv.org/abs/2611.slam-dunk
- **NIF-VIO** (2026-11-10) — [measured] correct-localisation rate above 98% inside moving carriers. [Visual SLAM](../Topics/Visual-SLAM.md), [Sensor fusion](../Topics/Sensor-Fusion.md). https://www.alphaxiv.org/abs/2611.13662
- **Differentiable Filtering for Inertial Odometry (DFIO)** (2026-11-10) — [measured] mean ATE −13.2% and RTE-1s −39.6% against TLIO. [Learned inertial odometry](../Topics/Learned-Inertial-Odometry.md). https://www.alphaxiv.org/abs/2611.13517
- **S²D-FVO: Scale-Consistent Monocular Fisheye Visual Odometry** (2026-11-09) — [measured] KITTI-360 average ATE 31.5 m against 335.4 m for OV²SLAM. [Visual odometry](../Topics/Visual-Odometry.md). https://www.alphaxiv.org/abs/2611.11934
- **HiPFuse** (University of Twente, 2026-11-10) — [measured] 14.2 FPS on Jetson AGX Orin at 63.7% mIoU (SemanticKITTI). [Edge AI](../Topics/Edge-AI.md), [Compute platforms](../Hardware/Compute-Platforms.md). https://www.alphaxiv.org/abs/2611.14025
- **Adapting Monocular Depth Estimation in Novel Scenes through Disparity Refinement and Robot Ego-Motion** (UC Riverside, JPL, 2026-11-11) — abstract only. https://www.alphaxiv.org/abs/2611.14958
- **GEMOR-GS** (2026-11-10) — abstract only. [Sensor fusion](../Topics/Sensor-Fusion.md). https://www.alphaxiv.org/abs/2611.13528
- **RAPA: Ray-Aware Physics Augmentation for Robust Camera-LiDAR Calibration** (Yonsei, 2026-11-09) — abstract only. [Sensor fusion](../Topics/Sensor-Fusion.md). https://www.alphaxiv.org/abs/2611.12129
Full context: [Weekly 2026-11-16](../Weekly/2026-11-16.md).
