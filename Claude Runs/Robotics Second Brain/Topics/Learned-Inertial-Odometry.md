# Learned inertial odometry

## Updates — 2026-10-26
- **Problem:** training an IMU-only odometry network for a new platform normally needs ground-truth trajectories.
- **Method (SSIO, [source fact]):** a "myopic teacher" integrates the IMU over short windows independently; the student learns velocity from those short-window changes, then pose-graph distillation adds sequence-consistent targets. Authors report average velocity error within 0.07 m/s of a same-architecture supervised AirIO baseline over six datasets (pedestrian, drone, quadruped, humanoid) [measured, authors]. Paper: [SSIO](../Research/Papers.md).
- **Analysis:** only IMU calibration and normal-operation logs are needed to start; whether this holds on a low-cost MEMS IMU is untested here [hypothesis].

## Updates — 2026-11-09
- **IMUDINO (2611.07437)** is a self-distilled foundation model for inertial sensing; the abstract names activity recognition, health and motion capture, not odometry. Whether its representations help inertial odometry is an untested [hypothesis]. [Weekly 2026-11-09](../Weekly/2026-11-09.md).

## Updates — 2026-11-16
- **Problem:** in TLIO-style systems the network that predicts displacement and its covariance is trained against local targets, separately from the filter that consumes it.
- **Method (DFIO, 2611.13517, [source fact]):** pre-train the displacement network, then freeze the encoder and refine the displacement and covariance heads with a loss on the filter's posterior position, back-propagated through the error-state Kalman filter update. IMU propagation stays analytical.
- **Results [measured, authors]:** 15 held-out TLIO trajectories, mean ATE 1.699 m against 1.957 m for TLIO (−13.2%) and RTE-1s 0.084 m against 0.140 m (−39.6%). RTE improved on all 15 trajectories; the 95% interval for the ATE difference spans zero. Trained on an RTX 3070; no inference timing given. Code "will be made publicly available".
- **Limits:** pedestrian motion only (Bosch BMI055 at 200 Hz, plus one smartphone sequence). Whether it holds for UAV dynamics is untested [hypothesis].
- Also this week, abstract only: **HeadIO** (2611.14895), body-frame heading decomposition for head-mounted devices. See [Weekly 2026-11-16](../Weekly/2026-11-16.md).
