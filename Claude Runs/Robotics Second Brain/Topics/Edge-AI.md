# Edge AI

## Updates — 2026-10-26
- **Depth on Jetson AGX Orin (NODAR benchmark, [measured]):** JetPack 6.2, CUDA 12.6, TensorRT 10.3, MAXN, TensorRT FP16. NVIDIA ESS stereo: 0.70% AbsRel in 8.6 ms; libSGM 0.73% in 25 ms; Fast-FoundationStereo 0.33% with more compute; best monocular ~12% AbsRel with true focal length (Depth Anything 3 Metric-L, 33 ms; Depth Pro 803 ms). Authors note stereo error falls with resolution while monocular does not improve. TensorRT engine builds took 27–79 min and used most of the 64 GB. Paper: [Papers](../Research/Papers.md).
- **Analysis:** where a stereo pair exists, stereo is the better depth budget on this class of device; numbers are for Orin 64GB and do not transfer directly to RB5.
- Related this week: SPAR (VLA pruning) and AgentDP (automated embedded deployment), abstracts only.

## Updates — 2026-11-09
- **Energy-aware open-vocabulary detection scheduling (2611.07663)** skips inference on low-value frames; **Aero-VPA (2611.04392)** targets few-step action decoding on embedded aerial hardware. Abstract-level only; no hardware figures read [source fact]. Measured runtime numbers for a VIO front-end filter are in [Visual SLAM](Visual-SLAM.md). See [Weekly 2026-11-09](../Weekly/2026-11-09.md).

## Updates — 2026-11-13
- **ZED ROS 2 Wrapper 5.6** adds CUDA zero-copy image transport using `rosidl::Buffer` (ROS 2 Lyrical, Isaac ROS 5) [source fact, title only; no latency figures seen]. Relevant to camera-to-inference latency on Jetson-class targets. https://discourse.openrobotics.org/t/zed-ros-2-wrapper-5-6-cuda-zero-copy-with-rosidl-buffer-for-ros-2-lyrical-and-isaac-ros-5/59608

## Updates — 2026-11-16
- **Classical SLAM on a CPU-only board (2611.16472, [measured]):** on a Raspberry Pi 5 neither RTAB-Map nor ORB-SLAM3 held 30 fps at full or half resolution in RGB-D mode; ORB-SLAM3 at 160×120 did (26 ms/frame) but lost tracking on five of six sequences. ORB-SLAM3 was built at -O2 without `-march=native`, so its times are conservative. Numbers in [Compute platforms](../Hardware/Compute-Platforms.md).
- **LiDAR segmentation on Jetson AGX Orin (HiPFuse, 2611.14025, [measured]):** 14.2 FPS on SemanticKITTI and 22.4 FPS on MCD, FP32, batch 1, MAXN, timed from scan-file input to labels on the CPU. No TensorRT or quantised result is reported.
- **Core pinning for control loops (NVIDIA Holoscan 5 tutorial, [measured] by NVIDIA):** pinning a 400 Hz control partition to one CPU core cut p99.99 latency by about 5× (C++) and 9.6× (Python). https://developer.nvidia.com/blog/make-a-robot-arm-feel-weightless-with-nvidia-holoscan-5/
- **Analysis:** these are three different budgets (CPU SLAM, GPU perception, hard-latency control) that compete on one board; none of the sources measures them together. See [Weekly 2026-11-16](../Weekly/2026-11-16.md).
