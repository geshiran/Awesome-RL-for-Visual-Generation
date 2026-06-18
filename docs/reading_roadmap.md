# Reading Roadmap

This roadmap gives a staged path through reinforcement learning for visual generation, from model interfaces to rewards, methods, and evaluation.

## Stage 1: Generative Interfaces

- **DDPO**: Training Diffusion Models with Reinforcement Learning [[Paper]](https://openreview.net/forum?id=YCWjhGrJFD) [[Code]](https://github.com/kvablack/ddpo-pytorch) <sub>![ICLR 2024](https://img.shields.io/badge/ICLR-2024-blue) Diffusion · Scalar Reward · Policy Gradient · Full Trajectory</sub>
- **PFM**: Preference Alignment with Flow Matching [[Paper]](https://arxiv.org/abs/2405.20010) [[Code]](https://github.com/jadehaus/preference-flow-matching) <sub>![NeurIPS 2024](https://img.shields.io/badge/NeurIPS-2024-blue) Flow Matching · Pairwise Preference · Offline Preference Alignment · Time</sub>
- **SimpleAR**: Pushing the Frontier of Autoregressive Visual Generation through Pretraining, SFT, and RL [[Paper]](https://arxiv.org/abs/2504.11455) <sub>![arXiv 2025](https://img.shields.io/badge/arXiv-2025-lightgrey) Autoregressive · Scalar Reward · GRPO · Token</sub>
- **SeqGAN**: Sequence Generative Adversarial Nets with Policy Gradient [[Paper]](https://arxiv.org/abs/1609.05473) <sub>![AAAI 2017](https://img.shields.io/badge/AAAI-2017-blue) GAN/VAE · Scalar Reward · Policy Gradient · Generator</sub>
- **RIG**: Visual Reinforcement Learning with Imagined Goals [[Paper]](https://arxiv.org/abs/1807.04742) <sub>![NeurIPS 2018](https://img.shields.io/badge/NeurIPS-2018-blue) GAN/VAE · Scalar Reward · TD3 · Latent</sub>

## Stage 2: Reward and Preference Models

- **ImageReward**: ImageReward: Learning and Evaluating Human Preferences for Text-to-Image Generation [[Paper]](https://arxiv.org/abs/2304.05977) [[Code]](https://github.com/zai-org/ImageReward) <sub>![NeurIPS 2023](https://img.shields.io/badge/NeurIPS-2023-blue) Reward Evaluator · Human Preference · Reward Model · Image</sub>
- **PickScore**: Pick-a-Pic: An Open Dataset of User Preferences for Text-to-Image Generation [[Paper]](https://arxiv.org/abs/2305.01569) [[Code]](https://github.com/yuvalkirstain/PickScore) [[Project]](https://pickapic.io/) <sub>![NeurIPS 2023](https://img.shields.io/badge/NeurIPS-2023-blue) Reward Evaluator · Human Preference · Reward Model · Image</sub>
- **HPSv2**: Human Preference Score v2 [[Paper]](https://arxiv.org/abs/2306.09341) [[Code]](https://github.com/tgxs002/HPSv2) <sub>![arXiv 2023](https://img.shields.io/badge/arXiv-2023-lightgrey) Reward Evaluator · Human Preference · Reward Model · Image</sub>
- **UnifiedReward**: Unified Reward Model for Multimodal Understanding and Generation [[Paper]](https://arxiv.org/abs/2503.05236) [[Code]](https://github.com/CodeGoat24/UnifiedReward) <sub>![arXiv 2025](https://img.shields.io/badge/arXiv-2025-lightgrey) Reward Evaluator · Unified Evaluation · Reward Model · Image + Video</sub>
- **VisionReward**: Fine-Grained Multi-Dimensional Human Preference Learning for Image and Video Generation [[Paper]](https://arxiv.org/abs/2412.21059) <sub>![AAAI 2026](https://img.shields.io/badge/AAAI-2026-blue) Reward Evaluator · Human Preference · Reward Model · Image + Video</sub>

## Stage 3: Diffusion Alignment

- **DPOK**: Reinforcement Learning for Fine-tuning Text-to-Image Diffusion Models [[Paper]](https://arxiv.org/abs/2305.16381) [[Code]](https://github.com/google-research/google-research/tree/master/dpok) <sub>![NeurIPS 2023](https://img.shields.io/badge/NeurIPS-2023-blue) Diffusion · Scalar Reward · Policy Gradient · Full Trajectory</sub>
- **DDPO**: Training Diffusion Models with Reinforcement Learning [[Paper]](https://openreview.net/forum?id=YCWjhGrJFD) [[Code]](https://github.com/kvablack/ddpo-pytorch) <sub>![ICLR 2024](https://img.shields.io/badge/ICLR-2024-blue) Diffusion · Scalar Reward · Policy Gradient · Full Trajectory</sub>
- **Diffusion-DPO**: Diffusion Model Alignment Using Direct Preference Optimization [[Paper]](https://arxiv.org/abs/2311.12908) [[Code]](https://github.com/SalesforceAIResearch/DiffusionDPO) <sub>![CVPR 2024](https://img.shields.io/badge/CVPR-2024-blue) Diffusion · Pairwise Preference · DPO · Full Trajectory</sub>
- **D3PO**: Using Human Feedback to Fine-Tune Diffusion Models without Any Reward Model [[Paper]](https://arxiv.org/abs/2311.13231) [[Code]](https://github.com/yk7333/D3PO) <sub>![CVPR 2024](https://img.shields.io/badge/CVPR-2024-blue) Diffusion · Pairwise Preference · DPO · Full Trajectory</sub>
- **DRaFT**: Directly Fine-Tuning Diffusion Models on Differentiable Rewards [[Paper]](https://arxiv.org/abs/2309.17400) <sub>![ICLR 2024](https://img.shields.io/badge/ICLR-2024-blue) Diffusion · Scalar Reward · Reward Backpropagation · Truncated</sub>
- **Parrot**: Pareto-Optimal Multi-Reward Reinforcement Learning Framework for Text-to-Image Generation [[Paper]](https://arxiv.org/abs/2401.05675) [[Project]](https://huggingface.co/spaces/parrot-multi-reward/Parrot) <sub>![ECCV 2024](https://img.shields.io/badge/ECCV-2024-blue) Diffusion · Multi-Reward Scalar · Policy Gradient · Prompt + T2I</sub>

## Stage 4: Flow and Autoregressive Alignment

- **Flow-GRPO**: Training Flow Matching Models via Online RL [[Paper]](https://arxiv.org/abs/2505.05470) [[Code]](https://github.com/yifan123/flow_grpo) <sub>![NeurIPS 2025](https://img.shields.io/badge/NeurIPS-2025-blue) Flow Matching · Scalar Reward · GRPO · Full Trajectory</sub>
- **MixGRPO**: Unlocking Flow-Based GRPO Efficiency with Mixed ODE-SDE [[Paper]](https://arxiv.org/abs/2507.21802) [[Code]](https://github.com/Tencent-Hunyuan/MixGRPO) <sub>![arXiv 2025](https://img.shields.io/badge/arXiv-2025-lightgrey) Flow Matching · Scalar Reward · GRPO · Truncated</sub>
- **SimpleAR**: Pushing the Frontier of Autoregressive Visual Generation through Pretraining, SFT, and RL [[Paper]](https://arxiv.org/abs/2504.11455) <sub>![arXiv 2025](https://img.shields.io/badge/arXiv-2025-lightgrey) Autoregressive · Scalar Reward · GRPO · Token</sub>
- **T2I-R1**: Reinforcing Image Generation with Collaborative Semantic-Level and Token-Level CoT [[Paper]](https://arxiv.org/abs/2505.00703) [[Code]](https://github.com/CaraJ7/T2I-R1) <sub>![NeurIPS 2025](https://img.shields.io/badge/NeurIPS-2025-blue) Autoregressive · Scalar Reward · GRPO · Token</sub>
- **UniRL**: Self-Improving Unified Multimodal Models via Supervised and Reinforcement Learning [[Paper]](https://arxiv.org/abs/2505.23380) <sub>![arXiv 2025](https://img.shields.io/badge/arXiv-2025-lightgrey) Autoregressive · Scalar Reward · GRPO · Token</sub>
- **HermesFlow**: Seamlessly Closing the Gap in Multimodal Understanding and Generation [[Paper]](https://arxiv.org/abs/2508.03039) [[Code]](https://github.com/gen-ai-team/HermesFlow) <sub>![NeurIPS 2025](https://img.shields.io/badge/NeurIPS-2025-blue) Autoregressive · Pairwise Preference · DPO · Token</sub>

## Stage 5: Evaluation Before Claims

- **GenEval**: An Object-Focused Framework for Evaluating Text-to-Image Alignment [[Paper]](https://arxiv.org/abs/2310.11513) [[Code]](https://github.com/djghosh13/geneval) <sub>![NeurIPS 2023](https://img.shields.io/badge/NeurIPS-2023-blue) Benchmark · Detector + Rules · Metric · Image</sub>
- **T2I-CompBench**: A Comprehensive Benchmark for Open-World Compositional Text-to-Image Generation [[Paper]](https://arxiv.org/abs/2307.06350) [[Project]](https://karine-h.github.io/T2I-CompBench/) <sub>![NeurIPS 2023](https://img.shields.io/badge/NeurIPS-2023-blue) Benchmark · Compositional Metrics · Metric · Image</sub>
- **TIFA**: Accurate and Interpretable Text-to-Image Faithfulness Evaluation with Question Answering [[Paper]](https://arxiv.org/abs/2303.11897) [[Code]](https://github.com/Yushi-Hu/tifa) <sub>![ICCV 2023](https://img.shields.io/badge/ICCV-2023-blue) Benchmark · VQA · Benchmark · Image</sub>
- **VQAScore**: Evaluating Text-to-Visual Generation with Image-to-Text Generation [[Paper]](https://arxiv.org/abs/2404.01291) [[Code]](https://github.com/linzhiqiu/t2v_metrics) <sub>![arXiv 2024](https://img.shields.io/badge/arXiv-2024-lightgrey) Benchmark · VQA · Benchmark · Image + Video</sub>
- **WISE**: World Knowledge-Informed Semantic Evaluation for Text-to-Image Generation [[Paper]](https://arxiv.org/abs/2503.07265) [[Code]](https://github.com/PKU-YuanGroup/WISE) <sub>![arXiv 2025](https://img.shields.io/badge/arXiv-2025-lightgrey) Benchmark · World Knowledge · Benchmark · Image</sub>
- **VBench**: VBench: Comprehensive Benchmark Suite for Video Generative Models [[Paper]](https://arxiv.org/abs/2311.17982) [[Code]](https://github.com/Vchitect/VBench) [[Project]](https://vchitect.github.io/VBench-project/) <sub>![CVPR 2024](https://img.shields.io/badge/CVPR-2024-blue) Benchmark · Video Quality Metrics · Benchmark · Video</sub>

## Suggested Paths

| Reader Background | Path |
| --- | --- |
| Diffusion researcher | Stage 2 -> Stage 3 -> Stage 5 -> Stage 4 |
| RL researcher | Stage 1 -> Stage 2 -> Stage 3 -> Stage 4 |
| Multimodal researcher | Stage 1 -> Stage 4 -> Stage 2 -> Stage 5 |
| Benchmark builder | Stage 2 -> Stage 5 -> Stage 3 |
| Newcomer | Stage 1 -> Stage 2 -> Stage 3 -> Stage 5 |
