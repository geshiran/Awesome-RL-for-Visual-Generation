# Method Selection Guide

Choose alignment methods by the generative interface first, then by feedback type, optimization scope, and compute budget.

## Interface-to-Method Map

| Interface | Feedback | Good Starting Points | Watch For |
| --- | --- | --- | --- |
| Diffusion trajectory | Scalar reward | DDPO, DPOK, RLD, Large-RL, Parrot | High-variance credit assignment and reward hacking. |
| Diffusion trajectory | Pairwise preference | Diffusion-DPO, D3PO, DSPO, SPO, CaPO | Preference data quality and reference-model drift. |
| Diffusion distillation | Differentiable reward | DRaFT, ReFL, RG-LCD, T2V-Turbo | Reward smoothness and loss of diversity. |
| Flow matching | Offline preference | PFM, Flow-DPO, SkyReels-V2, RDPO | Deterministic path assumptions. |
| Flow matching | Online RL | Flow-GRPO, TempFlow-GRPO, MixGRPO, GRPO-Guard | Exploration, clipping, and over-optimization. |
| Autoregressive visual tokens | Outcome reward | SimpleAR, VAR-GRPO, DreamVAR, GCPO | Sparse final rewards over long sequences. |
| Multimodal AR systems | Process reward | GoT-R1, ReasonGen-R1, T2I-R1, Janus-Pro-R1 | Separating reasoning quality from visual quality. |
| Unified multimodal interfaces | Understanding/generation reward | HermesFlow, CoRL, SUDER, UniRL, X-Omni | Improving generation while degrading understanding. |
| GAN/VAE latent spaces | Scalar or preference reward | SeqGAN, RL-GAN-Net, RIG, RL-I2IT | Diversity collapse and latent drift. |

## Feedback Selection

| Feedback Type | Use When | Suggested Evaluators |
| --- | --- | --- |
| Scalar learned reward | Fast iteration over many samples is possible | ImageReward, HPSv2, PickScore, aesthetic score |
| Pairwise preference | Human or model preference pairs are available | Preference reward plus GenEval/T2I-CompBench |
| VLM/MLLM judge | Semantics, relations, or world knowledge matter | TIFA, VQAScore, DSG, WISE, UnifiedReward |
| Task recognizer | Target behavior is narrow and measurable | OCR, detector, classifier, safety recognizer |
| Multi-reward objective | Aesthetic, fidelity, and prompt constraints conflict | Parrot-style reward balancing, held-out diagnostics |

## Minimal Evaluation Bundle

| Component | Purpose |
| --- | --- |
| Human-preference reward | Measures broad preference alignment. |
| Semantic evaluator | Checks prompt-image or prompt-video fidelity. |
| Compositional benchmark | Detects binding, counting, and spatial failures. |
| Held-out evaluator | Reduces circular evaluation against the training reward. |
| Qualitative audit | Groups failures by prompt family and visual artifact type. |
