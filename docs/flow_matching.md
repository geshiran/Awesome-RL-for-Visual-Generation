# Flow Matching Models

Flow matching models expose continuous generation paths. Alignment methods either keep these paths deterministic for offline preference learning, introduce stochastic or regularized interfaces for online RL, or formulate generation as dynamic control.

## 2.1 Offline Alignment over Deterministic Flows

- **PFM**: Preference Alignment with Flow Matching [[Paper]](https://arxiv.org/abs/2405.20010) [[Code]](https://github.com/jadehaus/preference-flow-matching) <sub>![NeurIPS 2024](https://img.shields.io/badge/NeurIPS-2024-blue) Flow Matching · Pairwise Preference · Offline Preference Alignment · Time</sub>
- **Flow-DPO**: Improving Video Generation with Human Feedback [[Paper]](https://arxiv.org/abs/2506.11350) [[Project]](https://gongyeliu.github.io/Flow-DPO/) <sub>![NeurIPS 2025](https://img.shields.io/badge/NeurIPS-2025-blue) Flow Matching · Pairwise Preference · DPO · Full Trajectory</sub>
- **SkyReels-V2**: Infinite-Length Film Generative Model [[Paper]](https://arxiv.org/abs/2504.13074) [[Code]](https://github.com/SkyworkAI/SkyReels-V2) <sub>![arXiv 2025](https://img.shields.io/badge/arXiv-2025-lightgrey) Flow Matching · Pairwise Preference · DPO · Full Trajectory</sub>
- **RDPO**: Real Data Preference Optimization for Physics Consistency Video Generation [[Paper]](https://arxiv.org/abs/2506.18655) [[Project]](https://wwenxu.github.io/RDPO/) <sub>![arXiv 2025](https://img.shields.io/badge/arXiv-2025-lightgrey) Flow Matching · Pairwise Preference · DPO · Full Trajectory</sub>

## 2.2 Online RL in Deterministic Flows

- **ORW-CFM-W2**: Online Reward-Weighted Fine-Tuning of Flow Matching with Wasserstein Regularization [[Paper]](https://openreview.net/forum?id=DspGEmu1zp) <sub>![ICLR 2025](https://img.shields.io/badge/ICLR-2025-blue) Flow Matching · Scalar Reward · Reward-Weighted Regression · Full Trajectory</sub>
- **Flow-GRPO**: Training Flow Matching Models via Online RL [[Paper]](https://arxiv.org/abs/2505.05470) [[Code]](https://github.com/yifan123/flow_grpo) <sub>![NeurIPS 2025](https://img.shields.io/badge/NeurIPS-2025-blue) Flow Matching · Scalar Reward · GRPO · Full Trajectory</sub>
- **TempFlow-GRPO**: When Timing Matters for GRPO in Flow Models [[Paper]](https://openreview.net/forum?id=ycKbfmJ4cV) <sub>![ICLR 2026](https://img.shields.io/badge/ICLR-2026-blue) Flow Matching · Scalar Reward · GRPO · Truncated</sub>
- **MixGRPO**: Unlocking Flow-Based GRPO Efficiency with Mixed ODE-SDE [[Paper]](https://arxiv.org/abs/2507.21802) [[Code]](https://github.com/Tencent-Hunyuan/MixGRPO) <sub>![arXiv 2025](https://img.shields.io/badge/arXiv-2025-lightgrey) Flow Matching · Scalar Reward · GRPO · Truncated</sub>
- **Stepwise-GRPO**: Stepwise Credit Assignment for GRPO on Flow-Matching Models [[Paper]](https://arxiv.org/abs/2603.28718) <sub>![CVPR 2026](https://img.shields.io/badge/CVPR-2026-blue) Flow Matching · Scalar Reward · GRPO · Stepwise Credit</sub>
- **GRPO-Guard**: Mitigating Implicit Over-Optimization in Flow Matching via Regulated Clipping [[Paper]](https://arxiv.org/abs/2605.03038) <sub>![CVPR 2026](https://img.shields.io/badge/CVPR-2026-blue) Flow Matching · Scalar Reward · GRPO · Guarded Updates</sub>
- **Pro-GRPO**: Expand and Prune: Maximizing Trajectory Diversity for Effective GRPO in Generative Models [[Paper]](https://arxiv.org/abs/2603.17937) <sub>![CVPR 2026](https://img.shields.io/badge/CVPR-2026-blue) Flow Matching · Scalar Reward · GRPO · Trajectory Diversity</sub>
- **Pref-GRPO**: Pairwise Preference Reward-Based GRPO for Stable Text-to-Image Reinforcement Learning [[Paper]](https://arxiv.org/abs/2505.20747) <sub>![COLM 2025](https://img.shields.io/badge/COLM-2025-blue) Flow Matching · Preference Reward · GRPO · Full Trajectory</sub>
- **Adv-GRPO**: The Image as Its Own Reward: Reinforcement Learning with Adversarial Reward for Image Generation [[Paper]](https://arxiv.org/abs/2605.09588) <sub>![CVPR 2026](https://img.shields.io/badge/CVPR-2026-blue) Flow Matching · Adversarial Reward · GRPO · Full Trajectory</sub>
- **PaCo-RL**: Advancing Reinforcement Learning for Consistent Image Generation with Pairwise Reward Modeling [[Paper]](https://arxiv.org/abs/2601.05433) [[Project]](https://x-gengroup.github.io/PaCo-RL/) <sub>![CVPR 2026](https://img.shields.io/badge/CVPR-2026-blue) Flow Matching · Pairwise Reward · GRPO · Consistency</sub>
- **PSR**: Scaling Multi-Subject Personalized Image Generation with Pairwise Subject-Consistency Rewards [[Paper]](https://arxiv.org/abs/2603.16305) [[Code]](https://github.com/Xiaojiu-z/PSR) <sub>![CVPR 2026](https://img.shields.io/badge/CVPR-2026-blue) Flow Matching · Pairwise Reward · GRPO · Subject Consistency</sub>

## 2.3 Unified Dynamic-Control Views

- **Adjoint Matching**: Fine-Tuning Flow and Diffusion Generative Models with Memoryless Stochastic Optimal Control [[Paper]](https://arxiv.org/abs/2409.08861) <sub>![ICLR 2025](https://img.shields.io/badge/ICLR-2025-blue) Flow Matching · Scalar Reward · Maximum-Entropy Control · Full Trajectory</sub>
- **DanceGRPO**: Unleashing GRPO on Visual Generation [[Paper]](https://arxiv.org/abs/2505.07818) <sub>![arXiv 2025](https://img.shields.io/badge/arXiv-2025-lightgrey) Flow Matching · Scalar Reward · GRPO · Full Trajectory</sub>
- **BranchGRPO**: Stable and Efficient GRPO with Structured Branching in Diffusion Models [[Paper]](https://openreview.net/forum?id=0fouTGCZga) <sub>![ICLR 2026](https://img.shields.io/badge/ICLR-2026-blue) Flow Matching · Scalar Reward · GRPO · Structured Branching</sub>
- **TPDM**: Schedule on the Fly: Diffusion Time Prediction for Faster and Better Image Generation [[Paper]](https://arxiv.org/abs/2503.21474) <sub>![CVPR 2025](https://img.shields.io/badge/CVPR-2025-blue) Flow Matching · Scalar Reward · PPO · Time Prediction</sub>

## Practical Notes

| Issue | Recommendation |
| --- | --- |
| Deterministic paths | Add preference structure, stochasticization, or control regularization before online RL. |
| Over-optimization | Use clipped or guarded objectives and held-out evaluators. |
| Scope mismatch | Report whether optimization is full-trajectory, truncated, time-level, or branch-based. |
