# Reward Signals and Evaluators

Reward design is the core bottleneck in RL for visual generation. Rewards differ by feedback source, output scope, cost, differentiability, and susceptibility to over-optimization.

## Classical Proxy and Diagnostic Metrics

- **IS**: Improved Techniques for Training GANs [[Paper]](https://arxiv.org/abs/1606.03498) <sub>![NeurIPS 2016](https://img.shields.io/badge/NeurIPS-2016-blue) Reward Evaluator · Classifier Score · Metric · Image</sub>
- **FID**: GANs Trained by a Two Time-Scale Update Rule Converge to a Local Nash Equilibrium [[Paper]](https://arxiv.org/abs/1706.08500) <sub>![NeurIPS 2017](https://img.shields.io/badge/NeurIPS-2017-blue) Reward Evaluator · Feature Distribution · Metric · Image</sub>
- **CLIPScore**: CLIPScore: A Reference-free Evaluation Metric for Image Captioning [[Paper]](https://arxiv.org/abs/2104.08718) <sub>![EMNLP 2021](https://img.shields.io/badge/EMNLP-2021-blue) Reward Evaluator · Embedding Similarity · Metric · Image</sub>
- **GenEval**: An Object-Focused Framework for Evaluating Text-to-Image Alignment [[Paper]](https://arxiv.org/abs/2310.11513) [[Code]](https://github.com/djghosh13/geneval) <sub>![NeurIPS 2023](https://img.shields.io/badge/NeurIPS-2023-blue) Benchmark · Detector + Rules · Metric · Image</sub>
- **Aesthetic Score**: LAION Aesthetic Predictor [[Paper]](https://arxiv.org/abs/2210.08402) [[Code]](https://github.com/christophschuhmann/improved-aesthetic-predictor) <sub>![NeurIPS 2022](https://img.shields.io/badge/NeurIPS-2022-blue) Reward Evaluator · Aesthetic Quality · Reward Model · Image</sub>
- **DeQA-Score**: Teaching Large Language Models to Regress Accurate Image Quality Scores [[Paper]](https://arxiv.org/abs/2412.16824) [[Code]](https://github.com/zhiyuanyou/DeQA-Score) <sub>![CVPR 2025](https://img.shields.io/badge/CVPR-2025-blue) Reward Evaluator · Quality/Diversity · Reward Model · Image</sub>

## Preference-Trained Reward Models

- **PickScore**: Pick-a-Pic: An Open Dataset of User Preferences for Text-to-Image Generation [[Paper]](https://arxiv.org/abs/2305.01569) [[Code]](https://github.com/yuvalkirstain/PickScore) [[Project]](https://pickapic.io/) <sub>![NeurIPS 2023](https://img.shields.io/badge/NeurIPS-2023-blue) Reward Evaluator · Human Preference · Reward Model · Image</sub>
- **ImageReward**: ImageReward: Learning and Evaluating Human Preferences for Text-to-Image Generation [[Paper]](https://arxiv.org/abs/2304.05977) [[Code]](https://github.com/zai-org/ImageReward) <sub>![NeurIPS 2023](https://img.shields.io/badge/NeurIPS-2023-blue) Reward Evaluator · Human Preference · Reward Model · Image</sub>
- **HPS**: Human Preference Score: Better Aligning Text-to-Image Models with Human Preference [[Paper]](https://arxiv.org/abs/2303.14420) [[Project]](https://tgxs002.github.io/align_sd_web/) <sub>![ICCV 2023](https://img.shields.io/badge/ICCV-2023-blue) Reward Evaluator · Human Preference · Reward Model · Image</sub>
- **HPSv2**: Human Preference Score v2 [[Paper]](https://arxiv.org/abs/2306.09341) [[Code]](https://github.com/tgxs002/HPSv2) <sub>![arXiv 2023](https://img.shields.io/badge/arXiv-2023-lightgrey) Reward Evaluator · Human Preference · Reward Model · Image</sub>
- **VP-Score**: Multimodal Large Language Model Is a Human-Aligned Annotator for Text-to-Image Generation [[Paper]](https://arxiv.org/abs/2404.15100) <sub>![arXiv 2024](https://img.shields.io/badge/arXiv-2024-lightgrey) Reward Evaluator · Human Preference · Reward Model · Image</sub>
- **SpatialScore**: Enhancing Spatial Understanding in Image Generation via Reward Modeling [[Paper]](https://arxiv.org/abs/2601.08126) <sub>![CVPR 2026](https://img.shields.io/badge/CVPR-2026-blue) Reward Evaluator · Spatial Preference · Reward Model · Image</sub>
- **MPS**: Learning Multi-Dimensional Human Preference for Text-to-Image Generation [[Paper]](https://openaccess.thecvf.com/content/CVPR2024/html/Zhang_Learning_Multi-dimensional_Human_Preference_for_Text-to-Image_Generation_CVPR_2024_paper.html) [[Code]](https://github.com/Kwai-Kolors/MPS) <sub>![CVPR 2024](https://img.shields.io/badge/CVPR-2024-blue) Reward Evaluator · Multi-Dimensional Human Preference · Reward Model · Image</sub>
- **ICT Score**: Enhancing Reward Models for High-Quality Image Generation: Beyond Text-Image Alignment [[Paper]](https://arxiv.org/abs/2504.08732) <sub>![ICCV 2025](https://img.shields.io/badge/ICCV-2025-blue) Reward Evaluator · Text-Image Alignment · Reward Model · Image</sub>
- **Social Reward**: Social Reward: Evaluating and Enhancing Generative AI through Million-User Feedback from an Online Creative Community [[Paper]](https://openreview.net/forum?id=0fh2aK8L8y) [[Code]](https://github.com/google-research/google-research/tree/master/social_rl) <sub>![ICLR 2024](https://img.shields.io/badge/ICLR-2024-blue) Reward Evaluator · Social Preference · Reward Model · Image</sub>

## VLM / MLLM-Based Reward Judges

- **VisionReward**: Fine-Grained Multi-Dimensional Human Preference Learning for Image and Video Generation [[Paper]](https://arxiv.org/abs/2412.21059) <sub>![AAAI 2026](https://img.shields.io/badge/AAAI-2026-blue) Reward Evaluator · Human Preference · Reward Model · Image + Video</sub>
- **OneReward**: OneReward: Unified Mask-Guided Image Generation via Multi-Task Human Preference Learning [[Paper]](https://arxiv.org/abs/2508.21066) [[Code]](https://github.com/OneReward/OneReward) [[Project]](https://one-reward.github.io/) <sub>![arXiv 2025](https://img.shields.io/badge/arXiv-2025-lightgrey) Reward Evaluator · Task-Aware Preference · Reward Model · Image</sub>
- **EngageNet**: Measuring and Improving Engagement of Text-to-Image Generation Models [[Paper]](https://openreview.net/forum?id=tLo5UZW8Bt) <sub>![ICLR 2025](https://img.shields.io/badge/ICLR-2025-blue) Reward Evaluator · Engagement · Reward Model · Image</sub>
- **RewardDance**: RewardDance: Reward Scaling in Visual Generation [[Paper]](https://arxiv.org/abs/2509.08826) [[Code]](https://github.com/SenseThink/RewardDance) <sub>![arXiv 2025](https://img.shields.io/badge/arXiv-2025-lightgrey) Reward Evaluator · Human Preference · Reward Model · Token</sub>
- **VideoReward**: Improving Video Generation with Human Feedback [[Paper]](https://arxiv.org/abs/2501.13918) [[Project]](https://gongyeliu.github.io/videoalign) <sub>![NeurIPS 2025](https://img.shields.io/badge/NeurIPS-2025-blue) Reward Evaluator · Human Preference · Reward Model · Video</sub>
- **LiFT**: LiFT: Leveraging Human Feedback for Text-to-Video Model Alignment [[Paper]](https://arxiv.org/abs/2412.04814) <sub>![arXiv 2024](https://img.shields.io/badge/arXiv-2024-lightgrey) Reward Evaluator · Video Quality · Reward Model · Video</sub>
- **UnifiedReward**: Unified Reward Model for Multimodal Understanding and Generation [[Paper]](https://arxiv.org/abs/2503.05236) [[Code]](https://github.com/CodeGoat24/UnifiedReward) <sub>![arXiv 2025](https://img.shields.io/badge/arXiv-2025-lightgrey) Reward Evaluator · Unified Evaluation · Reward Model · Image + Video</sub>
- **UnifiedReward-Flex**: Unified Personalized Reward Model for Vision Generation [[Paper]](https://arxiv.org/abs/2602.02380) <sub>![arXiv 2026](https://img.shields.io/badge/arXiv-2026-lightgrey) Reward Evaluator · Human Preference · Reward Model · Image + Video</sub>

VLM/MLLM-based judges are treated as an evaluator family rather than standalone paper entries. Concrete reward models are listed above when they have a public paper, model, codebase, or project page.

## Selection Notes

| Goal | Useful Reward Family | Caution |
| --- | --- | --- |
| Broad human preference | PickScore, HPSv2, ImageReward | Use held-out judges and qualitative audits. |
| Compositional correctness | GenEval, T2I-CompBench, DSG-style evaluators | Global embedding similarity is often insufficient. |
| Video quality | VideoReward, LiFT, VBench, VLM video judges | Check temporal consistency separately from aesthetics. |
| Multimodal generation | UnifiedReward, VisionReward, VLM/MLLM judges | Ensure understanding behavior does not regress. |
| Fast training loops | CLIPScore, aesthetic predictors, task recognizers | Cheap proxy rewards are easier to exploit. |
