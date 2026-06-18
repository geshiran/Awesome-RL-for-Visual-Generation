# Benchmarks and Evaluation

Evaluation for RL-based visual generation should be diagnostic. Reward gains can hide regressions in object binding, counting, spatial relations, temporal coherence, world knowledge, safety, or diversity.

## Benchmark Resources

- **GenEval**: An Object-Focused Framework for Evaluating Text-to-Image Alignment [[Paper]](https://arxiv.org/abs/2310.11513) [[Code]](https://github.com/djghosh13/geneval) <sub>![NeurIPS 2023](https://img.shields.io/badge/NeurIPS-2023-blue) Benchmark · Detector + Rules · Metric · Image</sub>
- **T2I-CompBench**: A Comprehensive Benchmark for Open-World Compositional Text-to-Image Generation [[Paper]](https://arxiv.org/abs/2307.06350) [[Project]](https://karine-h.github.io/T2I-CompBench/) <sub>![NeurIPS 2023](https://img.shields.io/badge/NeurIPS-2023-blue) Benchmark · Compositional Metrics · Metric · Image</sub>
- **DrawBench**: Prompt Suite from Imagen [[Paper]](https://arxiv.org/abs/2205.11487) <sub>![NeurIPS 2022](https://img.shields.io/badge/NeurIPS-2022-blue) Benchmark · Human Evaluation · Benchmark · Image</sub>
- **TIFA**: Accurate and Interpretable Text-to-Image Faithfulness Evaluation with Question Answering [[Paper]](https://arxiv.org/abs/2303.11897) [[Code]](https://github.com/Yushi-Hu/tifa) <sub>![ICCV 2023](https://img.shields.io/badge/ICCV-2023-blue) Benchmark · VQA · Benchmark · Image</sub>
- **VQAScore**: Evaluating Text-to-Visual Generation with Image-to-Text Generation [[Paper]](https://arxiv.org/abs/2404.01291) [[Code]](https://github.com/linzhiqiu/t2v_metrics) <sub>![arXiv 2024](https://img.shields.io/badge/arXiv-2024-lightgrey) Benchmark · VQA · Benchmark · Image + Video</sub>
- **DSG**: Evaluating Text-to-Image Generative Models with Decomposed Scene Graphs [[Paper]](https://arxiv.org/abs/2310.15025) <sub>![arXiv 2023](https://img.shields.io/badge/arXiv-2023-lightgrey) Benchmark · Scene Graph · Benchmark · Image</sub>
- **WISE**: World Knowledge-Informed Semantic Evaluation for Text-to-Image Generation [[Paper]](https://arxiv.org/abs/2503.07265) [[Code]](https://github.com/PKU-YuanGroup/WISE) <sub>![arXiv 2025](https://img.shields.io/badge/arXiv-2025-lightgrey) Benchmark · World Knowledge · Benchmark · Image</sub>
- **GenAI-Bench**: Evaluating and Improving Compositional Text-to-Visual Generation [[Paper]](https://arxiv.org/abs/2406.13743) [[Code]](https://github.com/linzhiqiu/t2v_metrics) [[Project]](https://linzhiqiu.github.io/papers/genai_bench/) <sub>![arXiv 2024](https://img.shields.io/badge/arXiv-2024-lightgrey) Benchmark · Human Ratings · Benchmark · Image + Video</sub>
- **VBench**: VBench: Comprehensive Benchmark Suite for Video Generative Models [[Paper]](https://arxiv.org/abs/2311.17982) [[Code]](https://github.com/Vchitect/VBench) [[Project]](https://vchitect.github.io/VBench-project/) <sub>![CVPR 2024](https://img.shields.io/badge/CVPR-2024-blue) Benchmark · Video Quality Metrics · Benchmark · Video</sub>

## Evaluation Matrix

| Capability | Useful Resources | Typical Failure After RL |
| --- | --- | --- |
| Human preference | Pick-a-Pic, HPSv2, ImageReward | Style bias or reward-model overfitting. |
| Object count and presence | GenEval, T2I-CompBench | Correct style with missing or extra objects. |
| Spatial and attribute binding | T2I-CompBench, DSG, VQAScore | Swapped relations or attributes despite high global alignment. |
| Faithfulness and world knowledge | TIFA, WISE, GenAI-Bench | Plausible images with wrong facts or relations. |
| Video temporal quality | VBench, GenAI-Bench, VideoReward | High aesthetic score with temporal inconsistency. |
