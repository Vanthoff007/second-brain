# Compute platforms

## Updates — 2026-10-26
- **Jetson AGX Orin 64GB** — measured depth-estimation timings under JetPack 6.2/TensorRT 10.3 are summarised in [Edge AI](../Topics/Edge-AI.md) (NODAR benchmark, [measured]).
- **Jetson Thor** — NVIDIA's 2026-10-21 release lists 2,070 FP4 teraflops and 128 GB unified memory in the Agile ONE SN reference humanoid [source fact, vendor-published; no independent measurement]. Early-2027 availability for that platform.
- **Qualcomm RB5 / Dragonwing:** no new in-window information gathered.

## Updates — 2026-10-30
- **Luxonis OAK 4 FFC** — announced via Open Robotics Discourse: 70 mm x 53 mm vision computer handling sync, recalibration, depth and AI for up to five cameras [source fact, vendor-announced; no SoC, TOPS, power or latency figures seen, no measurements]. Source: https://discourse.openrobotics.org/t/luxonis-new-silver-osra-member-and-a-new-product-release-that-you-can-win/59245 . See [2026-10-30 digest](../Daily/2026-10-30.md).

## Updates — 2026-11-16
Measured (author setups):
- **Raspberry Pi 5 Model B, 16 GB, BCM2712 (4× Cortex-A76 at 2.4 GHz), Active Cooler, Ubuntu 24.04** — RGB-D SLAM on TUM sequences (2611.16472): ORB-SLAM3 26–62 ms/frame end to end, peak memory 490–790 MB (about 490 MB of that is the vocabulary); RTAB-Map 0.23.13 150–462 ms/frame in a per-frame worst-case configuration, peak memory up to 2,295 MB. CPU load 26–42% of four cores. Peak temperature at most 59.0 °C, no throttling; under-voltage flags appeared on a marginal power supply.
- **Jetson AGX Orin 64 GB, MAXN** — HiPFuse LiDAR segmentation 14.2 FPS (SemanticKITTI), 22.4 FPS (MCD), 19.6 FPS (indoor Semantic-ITC); 660 MiB peak GPU memory on SemanticKITTI (2611.14025).

Published specs (vendor claims, not measured):
- **Qualcomm Dragonwing IQ-9075 modules:** Quectel SP900BF-AP (up to 100 TOPS, four cameras, engineering samples only, Linux support in development) and Forlinx FET9075AA-C ("100 dense TOPS"); Forlinx FET8275AA-C on IQ-8275 ("40 dense TOPS"). Sources: https://www.dronenews.org/story/quectel-announces-a-module-for-running-robot-ai-on-the-device (secondary) and https://www.forlinx.net/company-news/forlinx-electronica-2026-global-debut-on-device-ai-871.html
- **Forlinx robot controllers:** FCU3021 (Jetson Orin NX), FCU3031 (Jetson AGX Thor). Same Forlinx source.
- **NXP drone reference designs (2026-11-09):** NavQ95 companion computer (i.MX 95), Tropic VMU/FMU (i.MX RT1064), 100BASE-T1 sensor node (MCX N947), AM32-compliant ESC (MCX A13); open-source SDK with PX4, Zephyr and ROS 2. No TOPS or power figures in the release. https://media.nxp.com/news-releases/news-release-details/nxp-unveils-unified-robotics-platform-speed-trusted-physical-ai/
- **IDS GMSL2 Discovery Kit (2026-11-10):** Jetson Orin NX embedded PC with GMSL2 camera modules (onsemi AR0233, Full HD at 30 fps, HDR), V4L2 interface. https://en.ids-imaging.com/press-releases-article/items/gmsl2-discovery-kit.html
- **Qualcomm RB5:** no new in-window information found. See [Weekly 2026-11-16](../Weekly/2026-11-16.md).
