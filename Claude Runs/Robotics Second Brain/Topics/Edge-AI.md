# Edge AI

## Updates — 2026-10-26
- **Depth on Jetson AGX Orin (NODAR benchmark, [measured]):** JetPack 6.2, CUDA 12.6, TensorRT 10.3, MAXN, TensorRT FP16. NVIDIA ESS stereo: 0.70% AbsRel in 8.6 ms; libSGM 0.73% in 25 ms; Fast-FoundationStereo 0.33% with more compute; best monocular ~12% AbsRel with true focal length (Depth Anything 3 Metric-L, 33 ms; Depth Pro 803 ms). Authors note stereo error falls with resolution while monocular does not improve. TensorRT engine builds took 27–79 min and used most of the 64 GB. Paper: [Papers](../Research/Papers.md).
- **Analysis:** where a stereo pair exists, stereo is the better depth budget on this class of device; numbers are for Orin 64GB and do not transfer directly to RB5.
- Related this week: SPAR (VLA pruning) and AgentDP (automated embedded deployment), abstracts only.
