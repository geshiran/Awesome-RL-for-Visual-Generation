# Awesome RL for Visual Generation

![Resource List](https://img.shields.io/badge/Resource%20List-RL%20for%20Visual%20Generation-blue)
![Maintained](https://img.shields.io/badge/Maintained-yes-brightgreen)
![Contributions Welcome](https://img.shields.io/badge/Contributions-welcome-blue)
![Paper Coming Soon](https://img.shields.io/badge/Paper-Coming%20soon-lightgrey)
![TechRxiv Coming Soon](https://img.shields.io/badge/TechRxiv-Coming%20soon-lightgrey)

Curated resources for reinforcement learning in visual generation.

This repository organizes public papers, code, projects, reward models, and benchmarks by the generative-model interface through which feedback is applied: diffusion, flow matching, autoregressive visual generation, GAN/VAE-style latent generators, reward models, and evaluation benchmarks.

## Updates

- **2026.06**: Expanded public preview with verified paper, code, and project links where official sources are available.
- **Coming soon**: Paper and TechRxiv links will be added after public release.

## Taxonomy Overview

| Part | Interface | Main Alignment View |
| ------ | ---------------- | ------------------------------------------------- |
| Part 1 | Diffusion models | Denoising trajectory as policy or preference path |
| Part 2 | Flow matching models | Deterministic flow, stochasticized flow, or dynamic control |
| Part 3 | Autoregressive models | Visual token policy and multimodal process alignment |
| Part 4 | GANs and VAEs | Generator control, adversarial extensions, and latent RL |
| Part 5 | Reward signals and evaluators | Metrics, preference rewards, and VLM/MLLM judges |
| Part 6 | Benchmarks and evaluation | Diagnostic suites for preference, composition, video, and semantics |
| Part 7 | Method selection | Practical mapping from interface and feedback to method family |

## Table of Contents

- [Legend](#legend)
- [Part 1: Diffusion Models](#part-1-diffusion-models)
- [Part 2: Flow Matching Models](#part-2-flow-matching-models)
- [Part 3: Autoregressive Models](#part-3-autoregressive-models)
- [Part 4: GANs and VAEs](#part-4-gans-and-vaes)
- [Part 5: Reward Signals and Evaluators](#part-5-reward-signals-and-evaluators)
- [Part 6: Benchmarks and Evaluation](#part-6-benchmarks-and-evaluation)
- [Part 7: Method Selection Guide](#part-7-method-selection-guide)
- [Citation](#citation)

## Legend

| Tag | Meaning |
| --- | --- |
| Paradigm | Model interface or resource family, such as diffusion, flow matching, autoregressive, GAN/VAE, reward evaluator, or benchmark. |
| Feedback | Supervision or evaluation signal: scalar reward, pairwise preference, binary feedback, VLM judgment, social preference, or diagnostic metric. |
| RL Type | Optimization form: policy gradient, PPO, GRPO, DPO, KTO, reward backpropagation, maximum-entropy control, or reward-model evaluation. |
| Scope | Where the method acts: full trajectory, truncated trajectory, initial noise, latent space, token sequence, generator, data filtering, or benchmark output. |
| Task | Visual-generation setting: text-to-image, video generation, unified multimodal generation, personalized generation, or evaluation. |

## Part 1: Diffusion Models

### 1.1 Trajectory-Level Scalar-Reward Optimization

- **AdaDiff**: Adaptive Step Selection for Fast Diffusion Models [[Paper]](https://arxiv.org/abs/2411.14768) <sub>![AAAI 2025](https://img.shields.io/badge/AAAI-2025-blue) Diffusion · Scalar Reward · Reward-Weighted Likelihood · Step Selection</sub>
- **DPOK**: Reinforcement Learning for Fine-tuning Text-to-Image Diffusion Models [[Paper]](https://arxiv.org/abs/2305.16381) [[Code]](https://github.com/google-research/google-research/tree/master/dpok) <sub>![NeurIPS 2023](https://img.shields.io/badge/NeurIPS-2023-blue) Diffusion · Scalar Reward · Policy Gradient · Full Trajectory</sub>
- **DDPO**: Training Diffusion Models with Reinforcement Learning [[Paper]](https://openreview.net/forum?id=YCWjhGrJFD) [[Code]](https://github.com/kvablack/ddpo-pytorch) <sub>![ICLR 2024](https://img.shields.io/badge/ICLR-2024-blue) Diffusion · Scalar Reward · Policy Gradient · Full Trajectory</sub>
- **RLCM**: RL for Consistency Models: Reward Guided Text-to-Image Generation with Fast Inference [[Paper]](https://openreview.net/forum?id=PEr4d7d7nE) [[Project]](https://rlcm.owenoertell.com/) <sub>![RLC 2024](https://img.shields.io/badge/RLC-2024-blue) Diffusion · Scalar Reward · Policy Gradient · Full Trajectory</sub>
- **Large-RL**: Large-Scale Reinforcement Learning for Diffusion Models [[Paper]](https://arxiv.org/abs/2401.12244) <sub>![ECCV 2024](https://img.shields.io/badge/ECCV-2024-blue) Diffusion · Scalar Reward · Policy Gradient · Full Trajectory</sub>
- **Noise PPO**: A Minimalist Method for Fine-tuning Text-to-Image Diffusion Models [[Paper]](https://arxiv.org/abs/2506.12036) <sub>![arXiv 2025](https://img.shields.io/badge/arXiv-2025-lightgrey) Diffusion · Scalar Reward · PPO · Initial Noise</sub>
- **LOOP**: A Simple and Effective Reinforcement Learning Method for Text-to-Image Diffusion Fine-Tuning [[Paper]](https://arxiv.org/abs/2503.00897) <sub>![TMLR 2026](https://img.shields.io/badge/TMLR-2026-blue) Diffusion · Scalar Reward · PPO · Full Trajectory</sub>
- **DPG-T2I**: Powerful and Flexible: Personalized Text-to-Image Generation via Reinforcement Learning [[Paper]](https://arxiv.org/abs/2407.12928) [[Code]](https://github.com/wfanyue/DPG-T2I-Personalization) <sub>![ECCV 2024](https://img.shields.io/badge/ECCV-2024-blue) Diffusion · Scalar Reward · DPG · Full Trajectory</sub>
- **LaSRO**: Reward Fine-Tuning Two-Step Diffusion Models via Learning Differentiable Latent-Space Surrogate Reward [[Paper]](https://arxiv.org/abs/2503.22561) [[Project]](https://sites.google.com/view/lasro) <sub>![CVPR 2025](https://img.shields.io/badge/CVPR-2025-blue) Diffusion · Scalar Reward · Actor-Critic · Latent</sub>
- **RLD**: Training Diffusion Models towards Diverse Image Generation with Reinforcement Learning [[Paper]](https://arxiv.org/abs/2408.16516) <sub>![CVPR 2024](https://img.shields.io/badge/CVPR-2024-blue) Diffusion · Scalar Reward · Policy Gradient · Full Trajectory</sub>
- **Parrot**: Pareto-Optimal Multi-Reward Reinforcement Learning Framework for Text-to-Image Generation [[Paper]](https://arxiv.org/abs/2401.05675) [[Project]](https://huggingface.co/spaces/parrot-multi-reward/Parrot) <sub>![ECCV 2024](https://img.shields.io/badge/ECCV-2024-blue) Diffusion · Multi-Reward Scalar · Policy Gradient · Prompt + T2I</sub>

### 1.2 Preference-Based Diffusion Alignment

- **Diffusion-DPO**: Diffusion Model Alignment Using Direct Preference Optimization [[Paper]](https://arxiv.org/abs/2311.12908) [[Code]](https://github.com/SalesforceAIResearch/DiffusionDPO) <sub>![CVPR 2024](https://img.shields.io/badge/CVPR-2024-blue) Diffusion · Pairwise Preference · DPO · Full Trajectory</sub>
- **D3PO**: Using Human Feedback to Fine-Tune Diffusion Models without Any Reward Model [[Paper]](https://arxiv.org/abs/2311.13231) [[Code]](https://github.com/yk7333/D3PO) <sub>![CVPR 2024](https://img.shields.io/badge/CVPR-2024-blue) Diffusion · Pairwise Preference · DPO · Full Trajectory</sub>
- **Dense Reward DPO**: A Dense Reward View on Aligning Text-to-Image Diffusion with Preference [[Paper]](https://arxiv.org/abs/2402.08265) <sub>![ICML 2024](https://img.shields.io/badge/ICML-2024-blue) Diffusion · Pairwise Preference · DPO · Full Trajectory</sub>
- **Inv-DPO**: Inversion-DPO: Precise and Efficient Post-Training for Diffusion Models [[Paper]](https://arxiv.org/abs/2503.13568) [[Code]](https://github.com/MIGHTYEZ/Inversion-DPO) <sub>![ACM MM 2025](https://img.shields.io/badge/ACM%20MM-2025-blue) Diffusion · Pairwise Preference · DPO · Full Trajectory</sub>
- **DSPO**: Direct Score Preference Optimization for Diffusion Model Alignment [[Paper]](https://openreview.net/forum?id=xyfb3HHvMe) <sub>![ICLR 2025](https://img.shields.io/badge/ICLR-2025-blue) Diffusion · Pairwise Preference · DPO · Truncated</sub>
- **DDIM-InPO**: Inversion Preference Optimization with Reparametrized DDIM for Efficient Diffusion Model Alignment [[Paper]](https://arxiv.org/abs/2505.04302) <sub>![CVPR 2025](https://img.shields.io/badge/CVPR-2025-blue) Diffusion · Pairwise Preference · DPO · Latent</sub>
- **IAPO**: Instance-Aware Preference Optimization for Aligning Diffusion Models [[Paper]](https://arxiv.org/abs/2601.03737) <sub>![CVPR 2026](https://img.shields.io/badge/CVPR-2026-blue) Diffusion · Pairwise Preference · DPO · Full Trajectory</sub>
- **SPO**: Step-by-Step Preference Optimization for Aesthetic Post-Training [[Paper]](https://arxiv.org/abs/2503.17045) [[Code]](https://github.com/RockeyCoss/SPO) <sub>![CVPR 2025](https://img.shields.io/badge/CVPR-2025-blue) Diffusion · Pairwise Preference · DPO · Truncated</sub>
- **LPO**: Diffusion Model as a Noise-Aware Latent Reward Model for Step-Level Preference Optimization [[Paper]](https://arxiv.org/abs/2504.09051) [[Code]](https://github.com/casiatao/LPO) <sub>![NeurIPS 2025](https://img.shields.io/badge/NeurIPS-2025-blue) Diffusion · Pairwise Preference · DPO · Latent</sub>
- **RPO**: Subject-Driven Text-to-Image Generation via Preference-Based Reinforcement Learning [[Paper]](https://arxiv.org/abs/2406.09418) <sub>![NeurIPS 2024](https://img.shields.io/badge/NeurIPS-2024-blue) Diffusion · Pairwise Preference · DPO · Full Trajectory</sub>
- **CaPO**: Calibrated Multi-Preference Optimization for Aligning Diffusion Models [[Paper]](https://arxiv.org/abs/2505.18739) <sub>![CVPR 2025](https://img.shields.io/badge/CVPR-2025-blue) Diffusion · Pairwise Preference · DPO · Full Trajectory</sub>
- **VideoDPO**: Omni-Preference Alignment for Video Diffusion Generation [[Paper]](https://arxiv.org/abs/2412.14167) [[Project]](https://videodpo.github.io/) <sub>![CVPR 2025](https://img.shields.io/badge/CVPR-2025-blue) Diffusion · Pairwise Preference · DPO · Full Trajectory</sub>
- **DenseDPO**: Fine-Grained Temporal Preference Optimization for Video Diffusion Models [[Paper]](https://arxiv.org/abs/2505.20712) <sub>![NeurIPS 2025](https://img.shields.io/badge/NeurIPS-2025-blue) Diffusion · Pairwise Preference · DPO · Full Trajectory</sub>
- **IterComp**: Iterative Composition-Aware Feedback Learning from Model Gallery for Text-to-Image Generation [[Paper]](https://arxiv.org/abs/2410.07171) [[Code]](https://github.com/YangLing0818/IterComp) <sub>![ICLR 2025](https://img.shields.io/badge/ICLR-2025-blue) Diffusion · Pairwise Preference · DPO · Truncated</sub>
- **RankDPO**: Scalable Ranked Preference Optimization for Text-to-Image Generation [[Paper]](https://arxiv.org/abs/2503.12325) <sub>![ICCV 2025](https://img.shields.io/badge/ICCV-2025-blue) Diffusion · Ranked Preference · DPO · Full Trajectory</sub>
- **Self-NPO**: Data-Free Diffusion Model Enhancement via Truncated Diffusion Fine-Tuning [[Paper]](https://arxiv.org/abs/2411.19996) <sub>![AAAI 2026](https://img.shields.io/badge/AAAI-2026-blue) Diffusion · Self-Negative Preference · DPO · Truncated</sub>
- **Curriculum DPO**: Curriculum Direct Preference Optimization for Diffusion and Consistency Models [[Paper]](https://arxiv.org/abs/2503.10248) <sub>![CVPR 2025](https://img.shields.io/badge/CVPR-2025-blue) Diffusion · Pairwise Preference · DPO · Truncated</sub>
- **SmPO**: Smoothed Preference Optimization via Renoise Inversion for Aligning Diffusion Models [[Paper]](https://arxiv.org/abs/2506.00548) [[Project]](https://jaydenlyh.github.io/SmPO-project-page/) <sub>![ICML 2025](https://img.shields.io/badge/ICML-2025-blue) Diffusion · Pairwise Preference · DPO · Full Trajectory</sub>
- **PatchDPO**: Patch-Level DPO for Finetuning-Free Personalized Image Generation [[Paper]](https://arxiv.org/abs/2504.07510) [[Code]](https://github.com/hqhQAQ/PatchDPO) <sub>![CVPR 2025](https://img.shields.io/badge/CVPR-2025-blue) Diffusion · Pairwise Preference · DPO · Full Trajectory</sub>
- **Diff-KTO**: Aligning Diffusion Models by Optimizing Human Utility [[Paper]](https://arxiv.org/abs/2409.14146) <sub>![NeurIPS 2024](https://img.shields.io/badge/NeurIPS-2024-blue) Diffusion · Binary Feedback · KTO · Full Trajectory</sub>
- **CRAFT**: Aligning Diffusion Models with Fine-Tuning Is Easier Than You Think [[Paper]](https://arxiv.org/abs/2509.02081) <sub>![CVPR 2026](https://img.shields.io/badge/CVPR-2026-blue) Diffusion · Scalar Reward · SFT · Data Filtering</sub>

### 1.3 Reward-Guided Fine-Tuning and Distillation

- **ReFL**: ImageReward: Learning and Evaluating Human Preferences for Text-to-Image Generation [[Paper]](https://arxiv.org/abs/2304.05977) [[Code]](https://github.com/zai-org/ImageReward) <sub>![NeurIPS 2023](https://img.shields.io/badge/NeurIPS-2023-blue) Diffusion · Scalar Reward · Reward Feedback Learning · Truncated</sub>
- **DRaFT**: Directly Fine-Tuning Diffusion Models on Differentiable Rewards [[Paper]](https://arxiv.org/abs/2309.17400) <sub>![ICLR 2024](https://img.shields.io/badge/ICLR-2024-blue) Diffusion · Scalar Reward · Reward Backpropagation · Truncated</sub>
- **RSA-FT**: Reward Sharpness-Aware Fine-Tuning for Diffusion Models [[Paper]](https://arxiv.org/abs/2603.21175) <sub>![CVPR 2026](https://img.shields.io/badge/CVPR-2026-blue) Diffusion · Scalar Reward · Reward Backpropagation · Truncated/Full</sub>
- **RG-LCD**: Reward Guided Latent Consistency Distillation [[Paper]](https://arxiv.org/abs/2404.05968) <sub>![TMLR 2024](https://img.shields.io/badge/TMLR-2024-blue) Diffusion · Scalar Reward · Consistency Distillation · Student Model</sub>
- **T2V-Turbo**: Breaking the Quality Bottleneck of Video Consistency Model with Mixed Reward Feedback [[Paper]](https://arxiv.org/abs/2405.18750) [[Project]](https://t2v-turbo.github.io/) <sub>![NeurIPS 2024](https://img.shields.io/badge/NeurIPS-2024-blue) Diffusion · Mixed Reward · Distillation · Student Model</sub>
- **Diff-Instruct++**: Training One-Step Text-to-Image Generator Model to Align with Human Preferences [[Paper]](https://arxiv.org/abs/2410.18881) <sub>![TMLR 2025](https://img.shields.io/badge/TMLR-2025-blue) Diffusion · Preference · Distillation · One-Step</sub>
- **Reward-Instruct**: A Reward-Centric Approach to Fast Photo-Realistic Image Generation [[Paper]](https://arxiv.org/abs/2503.13070) <sub>![arXiv 2025](https://img.shields.io/badge/arXiv-2025-lightgrey) Diffusion · Scalar Reward · Reward-Centric Training · Fast Generation</sub>

## Part 2: Flow Matching Models

### 2.1 Offline Alignment over Deterministic Flows

- **PFM**: Preference Alignment with Flow Matching [[Paper]](https://arxiv.org/abs/2405.20010) [[Code]](https://github.com/jadehaus/preference-flow-matching) <sub>![NeurIPS 2024](https://img.shields.io/badge/NeurIPS-2024-blue) Flow Matching · Pairwise Preference · Offline Preference Alignment · Time</sub>
- **Flow-DPO**: Improving Video Generation with Human Feedback [[Paper]](https://arxiv.org/abs/2506.11350) [[Project]](https://gongyeliu.github.io/Flow-DPO/) <sub>![NeurIPS 2025](https://img.shields.io/badge/NeurIPS-2025-blue) Flow Matching · Pairwise Preference · DPO · Full Trajectory</sub>
- **SkyReels-V2**: Infinite-Length Film Generative Model [[Paper]](https://arxiv.org/abs/2504.13074) [[Code]](https://github.com/SkyworkAI/SkyReels-V2) <sub>![arXiv 2025](https://img.shields.io/badge/arXiv-2025-lightgrey) Flow Matching · Pairwise Preference · DPO · Full Trajectory</sub>
- **RDPO**: Real Data Preference Optimization for Physics Consistency Video Generation [[Paper]](https://arxiv.org/abs/2506.18655) [[Project]](https://wwenxu.github.io/RDPO/) <sub>![arXiv 2025](https://img.shields.io/badge/arXiv-2025-lightgrey) Flow Matching · Pairwise Preference · DPO · Full Trajectory</sub>

### 2.2 Online RL in Deterministic Flows

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

### 2.3 Unified Dynamic-Control Views

- **Adjoint Matching**: Fine-Tuning Flow and Diffusion Generative Models with Memoryless Stochastic Optimal Control [[Paper]](https://arxiv.org/abs/2409.08861) <sub>![ICLR 2025](https://img.shields.io/badge/ICLR-2025-blue) Flow Matching · Scalar Reward · Maximum-Entropy Control · Full Trajectory</sub>
- **DanceGRPO**: Unleashing GRPO on Visual Generation [[Paper]](https://arxiv.org/abs/2505.07818) <sub>![arXiv 2025](https://img.shields.io/badge/arXiv-2025-lightgrey) Flow Matching · Scalar Reward · GRPO · Full Trajectory</sub>
- **BranchGRPO**: Stable and Efficient GRPO with Structured Branching in Diffusion Models [[Paper]](https://openreview.net/forum?id=0fouTGCZga) <sub>![ICLR 2026](https://img.shields.io/badge/ICLR-2026-blue) Flow Matching · Scalar Reward · GRPO · Structured Branching</sub>
- **TPDM**: Schedule on the Fly: Diffusion Time Prediction for Faster and Better Image Generation [[Paper]](https://arxiv.org/abs/2503.21474) <sub>![CVPR 2025](https://img.shields.io/badge/CVPR-2025-blue) Flow Matching · Scalar Reward · PPO · Time Prediction</sub>

## Part 3: Autoregressive Models

### 3.1 Outcome-Level AR Alignment

- **GPS**: Data Generation as Sequential Decision Making [[Paper]](https://proceedings.neurips.cc/paper/2015/hash/6da9003b743b65f4c0ccd295cc484e57-Abstract.html) <sub>![NeurIPS 2015](https://img.shields.io/badge/NeurIPS-2015-blue) Autoregressive · NLL · Guided Policy Search · Token</sub>
- **RAL**: Incorporating Reinforced Adversarial Learning in Autoregressive Image Generation [[Paper]](https://www.ecva.net/papers/eccv_2020/papers_ECCV/html/784_ECCV_2020_paper.php) <sub>![ECCV 2020](https://img.shields.io/badge/ECCV-2020-blue) Autoregressive · Scalar Reward · Policy Gradient · Token</sub>
- **SimpleAR**: Pushing the Frontier of Autoregressive Visual Generation through Pretraining, SFT, and RL [[Paper]](https://arxiv.org/abs/2504.11455) <sub>![arXiv 2025](https://img.shields.io/badge/arXiv-2025-lightgrey) Autoregressive · Scalar Reward · GRPO · Token</sub>
- **LightGen**: Efficient Image Generation through Knowledge Distillation and Direct Preference Optimization [[Paper]](https://arxiv.org/abs/2503.08619) <sub>![arXiv 2025](https://img.shields.io/badge/arXiv-2025-lightgrey) Autoregressive · Pairwise Preference · DPO · Token</sub>
- **VAR-GRPO**: Fine-Tuning Next-Scale Visual Autoregressive Models with Group Relative Policy Optimization [[Paper]](https://arxiv.org/abs/2505.23331) <sub>![arXiv 2025](https://img.shields.io/badge/arXiv-2025-lightgrey) Autoregressive · Scalar Reward · GRPO · Token</sub>
- **DreamVAR**: Taming Reinforced Visual Autoregressive Model for High-Fidelity Subject-Driven Image Generation [[Paper]](https://arxiv.org/abs/2601.22507) <sub>![ICASSP 2026](https://img.shields.io/badge/ICASSP-2026-blue) Autoregressive · Scalar Reward · GRPO · Token</sub>
- **GCPO**: Group Critical-Token Policy Optimization for Autoregressive Image Generation [[Paper]](https://openreview.net/forum?id=hSywqe1bYD) <sub>![ICLR 2026](https://img.shields.io/badge/ICLR-2026-blue) Autoregressive · Scalar Reward · GRPO · Critical Tokens</sub>
- **AdaNAT**: Exploring Adaptive Policy for Token-Based Image Generation [[Paper]](https://arxiv.org/abs/2407.00354) <sub>![ECCV 2024](https://img.shields.io/badge/ECCV-2024-blue) Autoregressive · Adversarial Reward · PPO · Meta Policy</sub>
- **InfLVG**: Reinforce Inference-Time Consistent Long Video Generation with GRPO [[Paper]](https://arxiv.org/abs/2505.17574) <sub>![arXiv 2025](https://img.shields.io/badge/arXiv-2025-lightgrey) Autoregressive · Scalar Reward · GRPO · Context</sub>

### 3.2 Process-Level Multimodal AR Alignment

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

### 3.3 Multimodal Interface Alignment

- **HermesFlow**: Seamlessly Closing the Gap in Multimodal Understanding and Generation [[Paper]](https://arxiv.org/abs/2508.03039) [[Code]](https://github.com/gen-ai-team/HermesFlow) <sub>![NeurIPS 2025](https://img.shields.io/badge/NeurIPS-2025-blue) Autoregressive · Pairwise Preference · DPO · Token</sub>
- **CoRL**: Co-Reinforcement Learning for Unified Multimodal Understanding and Generation [[Paper]](https://arxiv.org/abs/2509.21327) <sub>![NeurIPS 2025](https://img.shields.io/badge/NeurIPS-2025-blue) Autoregressive · Scalar Reward · GRPO · Token</sub>
- **SUDER**: Self-Improving Unified Large Multimodal Models for Understanding and Generation with Dual Self-Rewards [[Paper]](https://arxiv.org/abs/2506.07963) <sub>![arXiv 2025](https://img.shields.io/badge/arXiv-2025-lightgrey) Autoregressive · Self Reward · GRPO · Token</sub>
- **GvU**: Learning to Generate via Understanding [[Paper]](https://arxiv.org/abs/2603.06043) <sub>![CVPR 2026](https://img.shields.io/badge/CVPR-2026-blue) Autoregressive · Intrinsic Reward · GRPO · Token</sub>
- **UniRL**: Self-Improving Unified Multimodal Models via Supervised and Reinforcement Learning [[Paper]](https://arxiv.org/abs/2505.23380) <sub>![arXiv 2025](https://img.shields.io/badge/arXiv-2025-lightgrey) Autoregressive · Scalar Reward · GRPO · Token</sub>
- **X-Omni**: Reinforcement Learning Makes Discrete Autoregressive Image Generative Models Great Again [[Paper]](https://arxiv.org/abs/2507.22058) <sub>![arXiv 2025](https://img.shields.io/badge/arXiv-2025-lightgrey) Autoregressive · Scalar Reward · GRPO · Token</sub>
- **Selftok-Zero**: Discrete Visual Tokens of Autoregression, by Diffusion, and for Reasoning [[Paper]](https://arxiv.org/abs/2506.07538) [[Project]](https://selftok-team.github.io/report/) <sub>![NeurIPS 2025](https://img.shields.io/badge/NeurIPS-2025-blue) Autoregressive · Visual Tokens · Self-Improvement · Token</sub>
- **SILMM**: Self-Improving Large Multimodal Models for Compositional Text-to-Image Generation [[Paper]](https://arxiv.org/abs/2503.12014) <sub>![CVPR 2025](https://img.shields.io/badge/CVPR-2025-blue) Autoregressive · Self-Improvement · Self-Training · Token</sub>

## Part 4: GANs and VAEs

### 4.1 GANs: RL Beyond Standard Adversarial Gradients

- **PolicyGAN**: Training Generative Adversarial Networks Using Policy Gradient [[Paper]](https://arxiv.org/abs/1708.05717) <sub>![ICAPR 2017](https://img.shields.io/badge/ICAPR-2017-blue) GAN/VAE · Scalar Reward · Policy Gradient · Generator</sub>
- **TD3-GAN**: Controlling the Latent Space of GANs through Reinforcement Learning: A Case Study on Task-Based Image-to-Image Translation [[Paper]](https://arxiv.org/abs/2302.04888) <sub>![SAC 2024](https://img.shields.io/badge/SAC-2024-blue) GAN/VAE · Scalar Reward · TD3 · Latent</sub>
- **RL-GAN-Net**: A Reinforcement Learning Agent Controlled GAN Network for Real-Time Point Cloud Shape Completion [[Paper]](https://openaccess.thecvf.com/content_CVPR_2019/html/Sarmad_RL-GAN-Net_A_Reinforcement_Learning_Agent_Controlled_GAN_Network_for_Real-Time_Point_CVPR_2019_paper.html) <sub>![CVPR 2019](https://img.shields.io/badge/CVPR-2019-blue) GAN/VAE · Scalar Reward · RL Agent · Generator</sub>
- **PbIG**: Preference-Based Image Generation [[Paper]](https://openaccess.thecvf.com/content_WACV_2020/html/Kazemi_Preference-Based_Image_Generation_WACV_2020_paper.html) <sub>![WACV 2020](https://img.shields.io/badge/WACV-2020-blue) GAN/VAE · Pairwise Preference · Preference-Based Generation · Latent</sub>
- **SeqGAN**: Sequence Generative Adversarial Nets with Policy Gradient [[Paper]](https://arxiv.org/abs/1609.05473) <sub>![AAAI 2017](https://img.shields.io/badge/AAAI-2017-blue) GAN/VAE · Scalar Reward · Policy Gradient · Generator</sub>
- **RL-V2V-GAN**: Video to Video Generative Adversarial Network for Few-Shot Learning Based on Policy Gradient [[Paper]](https://ieeexplore.ieee.org/document/10467045) <sub>![TNNLS 2025](https://img.shields.io/badge/TNNLS-2025-blue) GAN/VAE · Scalar Reward · DDPG · Generator</sub>
- **SAEC**: Stochastic Actor-Executor-Critic for Image-to-Image Translation [[Paper]](https://www.ijcai.org/proceedings/2021/144) <sub>![IJCAI 2021](https://img.shields.io/badge/IJCAI-2021-blue) GAN/VAE · Scalar Reward · Maximum-Entropy RL · Latent</sub>
- **RL-I2IT**: Image-to-Image Translation with Deep Reinforcement Learning [[Paper]](https://arxiv.org/abs/2309.13672) <sub>![arXiv 2024](https://img.shields.io/badge/arXiv-2024-lightgrey) GAN/VAE · Scalar Reward · Actor-Critic · Generator</sub>
- **AGAN**: Towards Automated Design of Generative Adversarial Networks [[Paper]](https://arxiv.org/abs/1906.11080) <sub>![arXiv 2019](https://img.shields.io/badge/arXiv-2019-lightgrey) GAN/VAE · Scalar Reward · Policy Gradient · Architecture</sub>

### 4.2 VAEs: RL on Latent Interfaces

- **HVAE**: Improving Unsupervised Hierarchical Representation with Reinforcement Learning [[Paper]](https://arxiv.org/abs/2402.11170) <sub>![CVPR 2024](https://img.shields.io/badge/CVPR-2024-blue) GAN/VAE · Scalar Reward · Policy Gradient · Latent</sub>
- **RIG**: Visual Reinforcement Learning with Imagined Goals [[Paper]](https://arxiv.org/abs/1807.04742) <sub>![NeurIPS 2018](https://img.shields.io/badge/NeurIPS-2018-blue) GAN/VAE · Scalar Reward · TD3 · Latent</sub>

## Part 5: Reward Signals and Evaluators

### 5.1 Classical Proxy and Diagnostic Metrics

- **IS**: Improved Techniques for Training GANs [[Paper]](https://arxiv.org/abs/1606.03498) <sub>![NeurIPS 2016](https://img.shields.io/badge/NeurIPS-2016-blue) Reward Evaluator · Classifier Score · Metric · Image</sub>
- **FID**: GANs Trained by a Two Time-Scale Update Rule Converge to a Local Nash Equilibrium [[Paper]](https://arxiv.org/abs/1706.08500) <sub>![NeurIPS 2017](https://img.shields.io/badge/NeurIPS-2017-blue) Reward Evaluator · Feature Distribution · Metric · Image</sub>
- **CLIPScore**: CLIPScore: A Reference-free Evaluation Metric for Image Captioning [[Paper]](https://arxiv.org/abs/2104.08718) <sub>![EMNLP 2021](https://img.shields.io/badge/EMNLP-2021-blue) Reward Evaluator · Embedding Similarity · Metric · Image</sub>
- **GenEval**: An Object-Focused Framework for Evaluating Text-to-Image Alignment [[Paper]](https://arxiv.org/abs/2310.11513) [[Code]](https://github.com/djghosh13/geneval) <sub>![NeurIPS 2023](https://img.shields.io/badge/NeurIPS-2023-blue) Benchmark · Detector + Rules · Metric · Image</sub>
- **Aesthetic Score**: LAION Aesthetic Predictor [[Paper]](https://arxiv.org/abs/2210.08402) [[Code]](https://github.com/christophschuhmann/improved-aesthetic-predictor) <sub>![NeurIPS 2022](https://img.shields.io/badge/NeurIPS-2022-blue) Reward Evaluator · Aesthetic Quality · Reward Model · Image</sub>
- **DeQA-Score**: Teaching Large Language Models to Regress Accurate Image Quality Scores [[Paper]](https://arxiv.org/abs/2412.16824) [[Code]](https://github.com/zhiyuanyou/DeQA-Score) <sub>![CVPR 2025](https://img.shields.io/badge/CVPR-2025-blue) Reward Evaluator · Quality/Diversity · Reward Model · Image</sub>

### 5.2 Preference-Trained Reward Models

- **PickScore**: Pick-a-Pic: An Open Dataset of User Preferences for Text-to-Image Generation [[Paper]](https://arxiv.org/abs/2305.01569) [[Code]](https://github.com/yuvalkirstain/PickScore) [[Project]](https://pickapic.io/) <sub>![NeurIPS 2023](https://img.shields.io/badge/NeurIPS-2023-blue) Reward Evaluator · Human Preference · Reward Model · Image</sub>
- **ImageReward**: ImageReward: Learning and Evaluating Human Preferences for Text-to-Image Generation [[Paper]](https://arxiv.org/abs/2304.05977) [[Code]](https://github.com/zai-org/ImageReward) <sub>![NeurIPS 2023](https://img.shields.io/badge/NeurIPS-2023-blue) Reward Evaluator · Human Preference · Reward Model · Image</sub>
- **HPS**: Human Preference Score: Better Aligning Text-to-Image Models with Human Preference [[Paper]](https://arxiv.org/abs/2303.14420) [[Project]](https://tgxs002.github.io/align_sd_web/) <sub>![ICCV 2023](https://img.shields.io/badge/ICCV-2023-blue) Reward Evaluator · Human Preference · Reward Model · Image</sub>
- **HPSv2**: Human Preference Score v2 [[Paper]](https://arxiv.org/abs/2306.09341) [[Code]](https://github.com/tgxs002/HPSv2) <sub>![arXiv 2023](https://img.shields.io/badge/arXiv-2023-lightgrey) Reward Evaluator · Human Preference · Reward Model · Image</sub>
- **VP-Score**: Multimodal Large Language Model Is a Human-Aligned Annotator for Text-to-Image Generation [[Paper]](https://arxiv.org/abs/2404.15100) <sub>![arXiv 2024](https://img.shields.io/badge/arXiv-2024-lightgrey) Reward Evaluator · Human Preference · Reward Model · Image</sub>
- **SpatialScore**: Enhancing Spatial Understanding in Image Generation via Reward Modeling [[Paper]](https://arxiv.org/abs/2601.08126) <sub>![CVPR 2026](https://img.shields.io/badge/CVPR-2026-blue) Reward Evaluator · Spatial Preference · Reward Model · Image</sub>
- **MPS**: Learning Multi-Dimensional Human Preference for Text-to-Image Generation [[Paper]](https://openaccess.thecvf.com/content/CVPR2024/html/Zhang_Learning_Multi-dimensional_Human_Preference_for_Text-to-Image_Generation_CVPR_2024_paper.html) [[Code]](https://github.com/Kwai-Kolors/MPS) <sub>![CVPR 2024](https://img.shields.io/badge/CVPR-2024-blue) Reward Evaluator · Multi-Dimensional Human Preference · Reward Model · Image</sub>
- **ICT Score**: Enhancing Reward Models for High-Quality Image Generation: Beyond Text-Image Alignment [[Paper]](https://arxiv.org/abs/2504.08732) <sub>![ICCV 2025](https://img.shields.io/badge/ICCV-2025-blue) Reward Evaluator · Text-Image Alignment · Reward Model · Image</sub>
- **Social Reward**: Social Reward: Evaluating and Enhancing Generative AI through Million-User Feedback from an Online Creative Community [[Paper]](https://openreview.net/forum?id=0fh2aK8L8y) [[Code]](https://github.com/google-research/google-research/tree/master/social_rl) <sub>![ICLR 2024](https://img.shields.io/badge/ICLR-2024-blue) Reward Evaluator · Social Preference · Reward Model · Image</sub>

### 5.3 VLM / MLLM-Based Reward Judges

- **VisionReward**: Fine-Grained Multi-Dimensional Human Preference Learning for Image and Video Generation [[Paper]](https://arxiv.org/abs/2412.21059) <sub>![AAAI 2026](https://img.shields.io/badge/AAAI-2026-blue) Reward Evaluator · Human Preference · Reward Model · Image + Video</sub>
- **OneReward**: OneReward: Unified Mask-Guided Image Generation via Multi-Task Human Preference Learning [[Paper]](https://arxiv.org/abs/2508.21066) [[Code]](https://github.com/OneReward/OneReward) [[Project]](https://one-reward.github.io/) <sub>![arXiv 2025](https://img.shields.io/badge/arXiv-2025-lightgrey) Reward Evaluator · Task-Aware Preference · Reward Model · Image</sub>
- **EngageNet**: Measuring and Improving Engagement of Text-to-Image Generation Models [[Paper]](https://openreview.net/forum?id=tLo5UZW8Bt) <sub>![ICLR 2025](https://img.shields.io/badge/ICLR-2025-blue) Reward Evaluator · Engagement · Reward Model · Image</sub>
- **RewardDance**: RewardDance: Reward Scaling in Visual Generation [[Paper]](https://arxiv.org/abs/2509.08826) [[Code]](https://github.com/SenseThink/RewardDance) <sub>![arXiv 2025](https://img.shields.io/badge/arXiv-2025-lightgrey) Reward Evaluator · Human Preference · Reward Model · Token</sub>
- **VideoReward**: Improving Video Generation with Human Feedback [[Paper]](https://arxiv.org/abs/2501.13918) [[Project]](https://gongyeliu.github.io/videoalign) <sub>![NeurIPS 2025](https://img.shields.io/badge/NeurIPS-2025-blue) Reward Evaluator · Human Preference · Reward Model · Video</sub>
- **LiFT**: LiFT: Leveraging Human Feedback for Text-to-Video Model Alignment [[Paper]](https://arxiv.org/abs/2412.04814) <sub>![arXiv 2024](https://img.shields.io/badge/arXiv-2024-lightgrey) Reward Evaluator · Video Quality · Reward Model · Video</sub>
- **UnifiedReward**: Unified Reward Model for Multimodal Understanding and Generation [[Paper]](https://arxiv.org/abs/2503.05236) [[Code]](https://github.com/CodeGoat24/UnifiedReward) <sub>![arXiv 2025](https://img.shields.io/badge/arXiv-2025-lightgrey) Reward Evaluator · Unified Evaluation · Reward Model · Image + Video</sub>
- **UnifiedReward-Flex**: Unified Personalized Reward Model for Vision Generation [[Paper]](https://arxiv.org/abs/2602.02380) <sub>![arXiv 2026](https://img.shields.io/badge/arXiv-2026-lightgrey) Reward Evaluator · Human Preference · Reward Model · Image + Video</sub>

VLM/MLLM-based judges are treated here as an evaluator family. Concrete reward models and benchmark papers are listed above when they have a public paper, model, codebase, or project page.

## Part 6: Benchmarks and Evaluation

- **GenEval**: An Object-Focused Framework for Evaluating Text-to-Image Alignment [[Paper]](https://arxiv.org/abs/2310.11513) [[Code]](https://github.com/djghosh13/geneval) <sub>![NeurIPS 2023](https://img.shields.io/badge/NeurIPS-2023-blue) Benchmark · Detector + Rules · Metric · Image</sub>
- **T2I-CompBench**: A Comprehensive Benchmark for Open-World Compositional Text-to-Image Generation [[Paper]](https://arxiv.org/abs/2307.06350) [[Project]](https://karine-h.github.io/T2I-CompBench/) <sub>![NeurIPS 2023](https://img.shields.io/badge/NeurIPS-2023-blue) Benchmark · Compositional Metrics · Metric · Image</sub>
- **DrawBench**: Prompt Suite from Imagen [[Paper]](https://arxiv.org/abs/2205.11487) <sub>![NeurIPS 2022](https://img.shields.io/badge/NeurIPS-2022-blue) Benchmark · Human Evaluation · Benchmark · Image</sub>
- **TIFA**: Accurate and Interpretable Text-to-Image Faithfulness Evaluation with Question Answering [[Paper]](https://arxiv.org/abs/2303.11897) [[Code]](https://github.com/Yushi-Hu/tifa) <sub>![ICCV 2023](https://img.shields.io/badge/ICCV-2023-blue) Benchmark · VQA · Benchmark · Image</sub>
- **VQAScore**: Evaluating Text-to-Visual Generation with Image-to-Text Generation [[Paper]](https://arxiv.org/abs/2404.01291) [[Code]](https://github.com/linzhiqiu/t2v_metrics) <sub>![arXiv 2024](https://img.shields.io/badge/arXiv-2024-lightgrey) Benchmark · VQA · Benchmark · Image + Video</sub>
- **DSG**: Evaluating Text-to-Image Generative Models with Decomposed Scene Graphs [[Paper]](https://arxiv.org/abs/2310.15025) <sub>![arXiv 2023](https://img.shields.io/badge/arXiv-2023-lightgrey) Benchmark · Scene Graph · Benchmark · Image</sub>
- **WISE**: World Knowledge-Informed Semantic Evaluation for Text-to-Image Generation [[Paper]](https://arxiv.org/abs/2503.07265) [[Code]](https://github.com/PKU-YuanGroup/WISE) <sub>![arXiv 2025](https://img.shields.io/badge/arXiv-2025-lightgrey) Benchmark · World Knowledge · Benchmark · Image</sub>
- **GenAI-Bench**: Evaluating and Improving Compositional Text-to-Visual Generation [[Paper]](https://arxiv.org/abs/2406.13743) [[Code]](https://github.com/linzhiqiu/t2v_metrics) [[Project]](https://linzhiqiu.github.io/papers/genai_bench/) <sub>![arXiv 2024](https://img.shields.io/badge/arXiv-2024-lightgrey) Benchmark · Human Ratings · Benchmark · Image + Video</sub>
- **VBench**: VBench: Comprehensive Benchmark Suite for Video Generative Models [[Paper]](https://arxiv.org/abs/2311.17982) [[Code]](https://github.com/Vchitect/VBench) [[Project]](https://vchitect.github.io/VBench-project/) <sub>![CVPR 2024](https://img.shields.io/badge/CVPR-2024-blue) Benchmark · Video Quality Metrics · Benchmark · Video</sub>

## Part 7: Method Selection Guide

| Goal | Recommended Starting Point |
| ---------------------------------------- | ------------------------------------------------- |
| Improve scalar rewards for diffusion T2I | DDPO, DPOK, RLD, Large-RL, reward backpropagation |
| Use pairwise preferences for diffusion | Diffusion-DPO, D3PO, DSPO, SPO, CaPO |
| Align deterministic flow models | PFM, Flow-DPO, ORW-CFM-W2, Flow-GRPO |
| Optimize autoregressive visual tokens | SimpleAR, VAR-GRPO, GCPO, T2I-R1 |
| Align unified multimodal generators | HermesFlow, CoRL, SUDER, UniRL, X-Omni |
| Build a reward/evaluation stack | PickScore, HPSv2, ImageReward, GenEval, T2I-CompBench, VBench, VLM/MLLM judges |

## Citation

Paper: Coming soon  
TechRxiv: Coming soon

For now, please cite the individual papers, datasets, models, and codebases that you use.
