# Learned inertial odometry

## Updates — 2026-10-26
- **Problem:** training an IMU-only odometry network for a new platform normally needs ground-truth trajectories.
- **Method (SSIO, [source fact]):** a "myopic teacher" integrates the IMU over short windows independently; the student learns velocity from those short-window changes, then pose-graph distillation adds sequence-consistent targets. Authors report average velocity error within 0.07 m/s of a same-architecture supervised AirIO baseline over six datasets (pedestrian, drone, quadruped, humanoid) [measured, authors]. Paper: [SSIO](../Research/Papers.md).
- **Analysis:** only IMU calibration and normal-operation logs are needed to start; whether this holds on a low-cost MEMS IMU is untested here [hypothesis].
