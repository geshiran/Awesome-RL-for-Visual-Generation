# Autoregressive Models

Autoregressive visual generators expose explicit token decisions. RL can therefore optimize final visual outcomes, intermediate reasoning or generation processes, and unified multimodal interfaces that mix understanding and generation.

## 3.1 Outcome-Level AR Alignment

- **GPS**: Data Generation as Sequential Decision Making [[Paper]](https://proceedings.neurips.cc/paper/2015/hash/6da9003b743b65f4c0ccd295cc484e57-Abstract.html) <sub>![NeurIPS 2015](https://img.shields.io/badge/NeurIPS-2015-blue) Autoregressive · NLL · Guided Policy Search · Token</sub>
- **RAL**: Incorporating Reinforced Adversarial Learning in Autoregressive Image Generation [[Paper]](https://www.ecva.net/papers/eccv_2020/papers_ECCV/html/784_ECCV_2020_paper.php) <sub>![ECCV 2020](https://img.shields.io/badge/ECCV-2020-blue) Autoregressive · Scalar Reward · Policy Gradient · Token</sub>
- **SimpleAR**: Pushing the Frontier of Autoregressive Visual Generation through Pretraining, SFT, and RL [[Paper]](https://arxiv.org/abs/2504.11455) <sub>![arXiv 2025](https://img.shields.io/badge/arXiv-2025-lightgrey) Autoregressive · Scalar Reward · GRPO · Token</sub>
- **LightGen**: Efficient Image Generation through Knowledge Distillation and Direct Preference Optimization [[Paper]](https://arxiv.org/abs/2503.08619) <sub>![arXiv 2025](https://img.shields.io/badge/arXiv-2025-lightgrey) Autoregressive · Pairwise Preference · DPO · Token</sub>
- **VAR-GRPO**: Fine-Tuning Next-Scale Visual Autoregressive Models with Group Relative Policy Optimization [[Paper]](https://arxiv.org/abs/2505.23331) <sub>![arXiv 2025](https://img.shields.io/badge/arXiv-2025-lightgrey) Autoregressive · Scalar Reward · GRPO · Token</sub>
- **DreamVAR**: Taming Reinforced Visual Autoregressive Model for High-Fidelity Subject-Driven Image Generation [[Paper]](https://arxiv.org/abs/2601.22507) <sub>![ICASSP 2026](https://img.shields.io/badge/ICASSP-2026-blue) Autoregressive · Scalar Reward · GRPO · Token</sub>
- **GCPO**: Group Critical-Token Policy Optimization for Autoregressive Image Generation [[Paper]](https://openreview.net/forum?id=hSywqe1bYD) <sub>![ICLR 2026](https://img.shields.io/badge/ICLR-2026-blue) Autoregressive · Scalar Reward · GRPO · Critical Tokens</sub>
- **AdaNAT**: Exploring Adaptive Policy for Token-Based Image Generation [[Paper]](https://arxiv.org/abs/2407.00354) <sub>![ECCV 2024](https://img.shields.io/badge/ECCV-2024-blue) Autoregressive · Adversarial Reward · PPO · Meta Policy</sub>
- **InfLVG**: Reinforce Inference-Time Consistent Long Video Generation with GRPO [[Paper]](https://arxiv.org/abs/2505.17574) <sub>![arXiv 2025](https://img.shields.io/badge/arXiv-2025-lightgrey) Autoregressive · Scalar Reward · GRPO · Context</sub>

## 3.2 Process-Level Multimodal AR Alignment

- **GoT-R1**: Unleashing Reasoning Capability of Autoregressive Visual Generation with Reinforcement Learning [[Paper]](https://openreview.net/forum?id=xXZ3Ix0ilF) <sub>![ICLR 2026](https://img.shields.io/badge/ICLR-2026-blue) Autoregressive · MLLM Feedback · GRPO · Token</sub>
- **ReasonGen-R1**: CoT for Autoregressive Image Generation Models through SFT and RL [[Paper]](https://arxiv.org/abs/2505.24875) <sub>![arXiv 2025](https://img.shields.io/badge/arXiv-2025-lightgrey) Autoregressive · VLM Feedback · GRPO · Token</sub>
- **NextStep-1**: Toward Autoregressive Image Generation with Continuous Tokens at Scale [[Paper]](https://openreview.net/forum?id=BEgFrrp94y) <sub>![ICLR 2026](https://img.shields.io/badge/ICLR-2026-blue) Autoregressive · Pairwise Preference · DPO · Sequence</sub>
- **UniGRPO**: Unified Policy Optimization for Reasoning-Driven Visual Generation [[Paper]](https://arxiv.org/abs/2603.23500) <sub>![arXiv 2026](https://img.shields.io/badge/arXiv-2026-lightgrey) Autoregressive · Scalar Reward · GRPO · Token + Flow</sub>
- **Vinci**: Deep Thinking in Text-to-Image Generation Using Unified Model with Reinforcement Learning [[Paper]](https://arxiv.org/abs/2509.06950) <sub>![NeurIPS 2025](https://img.shields.io/badge/NeurIPS-2025-blue) Autoregressive · Scalar Reward · GRPO · Token</sub>
- **PARM**: Let us Verify and Reinforce Image Generation Step by Step [[Paper]](https://arxiv.org/abs/2505.14962) [[Code]](https://github.com/ddongjs/PARM) <sub>![CVPR 2025](https://img.shields.io/badge/CVPR-2025-blue) Autoregressive · Pairwise Preference · DPO · Token</sub>
- **UnifiedGRPO**: Towards Unified Multimodal Interleaved Generation via Group Relative Policy Optimization [[Paper]](https://arxiv.org/abs/2505.14683) <sub>![NeurIPS 2025](https://img.shields.io/badge/NeurIPS-2025-blue) Autoregressive · Scalar Reward · GRPO · Sequence</sub>
- **T2I-R1**: Reinforcing Image Generation with Collaborative Semantic-Level and Token-Level CoT [[Paper]](https://arxiv.org/abs/2505.00703) [[Code]](https://github.com/CaraJ7/T2I-R1) <sub>![NeurIPS 2025](https://img.shields.io/badge/NeurIPS-2025-blue) Autoregressive · Scalar Reward · GRPO · Token</sub>
- **Visual-CoG**: Stage-Aware Reinforcement Learning with Chain of Guidance for Text-to-Image Generation [[Paper]](https://arxiv.org/abs/2508.18032) <sub>![arXiv 2025](https://img.shields.io/badge/arXiv-2025-lightgrey) Autoregressive · Scalar Reward · GRPO · Token</sub>
- **Janus-Pro-R1**: Advancing Collaborative Visual Comprehension and Generation via Reinforcement Learning [[Paper]](https://arxiv.org/abs/2504.00859) [[Project]](https://janus-pro-r1.github.io/) <sub>![NeurIPS 2025](https://img.shields.io/badge/NeurIPS-2025-blue) Autoregressive · Scalar Reward · GRPO · Token</sub>

## 3.3 Multimodal Interface Alignment

- **HermesFlow**: Seamlessly Closing the Gap in Multimodal Understanding and Generation [[Paper]](https://arxiv.org/abs/2508.03039) [[Code]](https://github.com/gen-ai-team/HermesFlow) <sub>![NeurIPS 2025](https://img.shields.io/badge/NeurIPS-2025-blue) Autoregressive · Pairwise Preference · DPO · Token</sub>
- **CoRL**: Co-Reinforcement Learning for Unified Multimodal Understanding and Generation [[Paper]](https://arxiv.org/abs/2509.21327) <sub>![NeurIPS 2025](https://img.shields.io/badge/NeurIPS-2025-blue) Autoregressive · Scalar Reward · GRPO · Token</sub>
- **SUDER**: Self-Improving Unified Large Multimodal Models for Understanding and Generation with Dual Self-Rewards [[Paper]](https://arxiv.org/abs/2506.07963) <sub>![arXiv 2025](https://img.shields.io/badge/arXiv-2025-lightgrey) Autoregressive · Self Reward · GRPO · Token</sub>
- **GvU**: Learning to Generate via Understanding [[Paper]](https://arxiv.org/abs/2603.06043) <sub>![CVPR 2026](https://img.shields.io/badge/CVPR-2026-blue) Autoregressive · Intrinsic Reward · GRPO · Token</sub>
- **UniRL**: Self-Improving Unified Multimodal Models via Supervised and Reinforcement Learning [[Paper]](https://arxiv.org/abs/2505.23380) <sub>![arXiv 2025](https://img.shields.io/badge/arXiv-2025-lightgrey) Autoregressive · Scalar Reward · GRPO · Token</sub>
- **X-Omni**: Reinforcement Learning Makes Discrete Autoregressive Image Generative Models Great Again [[Paper]](https://arxiv.org/abs/2507.22058) <sub>![arXiv 2025](https://img.shields.io/badge/arXiv-2025-lightgrey) Autoregressive · Scalar Reward · GRPO · Token</sub>
- **Selftok-Zero**: Discrete Visual Tokens of Autoregression, by Diffusion, and for Reasoning [[Paper]](https://arxiv.org/abs/2506.07538) [[Project]](https://selftok-team.github.io/report/) <sub>![NeurIPS 2025](https://img.shields.io/badge/NeurIPS-2025-blue) Autoregressive · Visual Tokens · Self-Improvement · Token</sub>
- **SILMM**: Self-Improving Large Multimodal Models for Compositional Text-to-Image Generation [[Paper]](https://arxiv.org/abs/2503.12014) <sub>![CVPR 2025](https://img.shields.io/badge/CVPR-2025-blue) Autoregressive · Self-Improvement · Self-Training · Token</sub>

## Practical Notes

| Issue | Recommendation |
| --- | --- |
| Sparse rewards | Use group-relative or process-aware objectives when final-image rewards are delayed. |
| Token drift | Track entropy, repetition, and tokenizer-specific failure modes. |
| Unified models | Evaluate understanding and generation jointly. |
