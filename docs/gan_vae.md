# GANs and VAEs

GANs and VAEs provide important precedents for generator-as-policy learning, adversarial reward design, and latent-action control.

## GANs: RL beyond Standard Adversarial Gradients

- **PolicyGAN**: Training Generative Adversarial Networks Using Policy Gradient [[Paper]](https://arxiv.org/abs/1708.05717) <sub>![ICAPR 2017](https://img.shields.io/badge/ICAPR-2017-blue) GAN/VAE · Scalar Reward · Policy Gradient · Generator</sub>
- **TD3-GAN**: Controlling the Latent Space of GANs through Reinforcement Learning: A Case Study on Task-Based Image-to-Image Translation [[Paper]](https://arxiv.org/abs/2302.04888) <sub>![SAC 2024](https://img.shields.io/badge/SAC-2024-blue) GAN/VAE · Scalar Reward · TD3 · Latent</sub>
- **RL-GAN-Net**: A Reinforcement Learning Agent Controlled GAN Network for Real-Time Point Cloud Shape Completion [[Paper]](https://openaccess.thecvf.com/content_CVPR_2019/html/Sarmad_RL-GAN-Net_A_Reinforcement_Learning_Agent_Controlled_GAN_Network_for_Real-Time_Point_CVPR_2019_paper.html) <sub>![CVPR 2019](https://img.shields.io/badge/CVPR-2019-blue) GAN/VAE · Scalar Reward · RL Agent · Generator</sub>
- **PbIG**: Preference-Based Image Generation [[Paper]](https://openaccess.thecvf.com/content_WACV_2020/html/Kazemi_Preference-Based_Image_Generation_WACV_2020_paper.html) <sub>![WACV 2020](https://img.shields.io/badge/WACV-2020-blue) GAN/VAE · Pairwise Preference · Preference-Based Generation · Latent</sub>
- **SeqGAN**: Sequence Generative Adversarial Nets with Policy Gradient [[Paper]](https://arxiv.org/abs/1609.05473) <sub>![AAAI 2017](https://img.shields.io/badge/AAAI-2017-blue) GAN/VAE · Scalar Reward · Policy Gradient · Generator</sub>
- **RL-V2V-GAN**: Video to Video Generative Adversarial Network for Few-Shot Learning Based on Policy Gradient [[Paper]](https://ieeexplore.ieee.org/document/10467045) <sub>![TNNLS 2025](https://img.shields.io/badge/TNNLS-2025-blue) GAN/VAE · Scalar Reward · DDPG · Generator</sub>
- **SAEC**: Stochastic Actor-Executor-Critic for Image-to-Image Translation [[Paper]](https://www.ijcai.org/proceedings/2021/144) <sub>![IJCAI 2021](https://img.shields.io/badge/IJCAI-2021-blue) GAN/VAE · Scalar Reward · Maximum-Entropy RL · Latent</sub>
- **RL-I2IT**: Image-to-Image Translation with Deep Reinforcement Learning [[Paper]](https://arxiv.org/abs/2309.13672) <sub>![arXiv 2024](https://img.shields.io/badge/arXiv-2024-lightgrey) GAN/VAE · Scalar Reward · Actor-Critic · Generator</sub>
- **AGAN**: Towards Automated Design of Generative Adversarial Networks [[Paper]](https://arxiv.org/abs/1906.11080) <sub>![arXiv 2019](https://img.shields.io/badge/arXiv-2019-lightgrey) GAN/VAE · Scalar Reward · Policy Gradient · Architecture</sub>

## VAEs: RL on Latent Interfaces

- **HVAE**: Improving Unsupervised Hierarchical Representation with Reinforcement Learning [[Paper]](https://arxiv.org/abs/2402.11170) <sub>![CVPR 2024](https://img.shields.io/badge/CVPR-2024-blue) GAN/VAE · Scalar Reward · Policy Gradient · Latent</sub>
- **RIG**: Visual Reinforcement Learning with Imagined Goals [[Paper]](https://arxiv.org/abs/1807.04742) <sub>![NeurIPS 2018](https://img.shields.io/badge/NeurIPS-2018-blue) GAN/VAE · Scalar Reward · TD3 · Latent</sub>

## Practical Notes

| Issue | Recommendation |
| --- | --- |
| Native adversarial objectives | State clearly when RL adds value beyond discriminator gradients. |
| Latent optimization | Track diversity and controllability under reward pressure. |
| Generator control | Identify whether the action is a token, latent vector, architecture choice, or generator update. |
