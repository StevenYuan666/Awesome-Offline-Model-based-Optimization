# Awesome-Offline-Model-Based-Optimization

📰 Must-read papers on Offline Model-Based Optimization 🔥

This repository collects important papers for our new survey (will release soon).

[![Awesome](https://awesome.re/badge.svg)](https://github.com/StevenYuan666/Awesome-Offline-Model-Based-Optimization)
![](https://img.shields.io/github/last-commit/StevenYuan666/Awesome-Offline-Model-Based-Optimization?color=green)
![](https://img.shields.io/badge/PRs-Welcome-red)

## 🔍 Table of Contents

- [🌟 What is Offline Model-Based Optimization?](#-definition)
- [🔗 Benchmarks](#-Benchmarks)
- [🎯 Surrogate Models-based Methods](#-Surrogate-Models-based-Methods)
- [🤔 Generative Models-based Methods](#-Generative-Models-based-Methods)
- [🤗 Contribution](#-contribution)
  - [Contributors](#contributors)
  - [Acknowledgement](#acknowledgement)

## 🌟 What is Offline Model-Based Optimization?

In offline optimization, the goal is to discover a new design, denoted by $\boldsymbol{x}^*$, that maximizes the objective(s) $\boldsymbol{f}(\boldsymbol{x})$. This is achieved using an offline dataset $\mathcal{D}$, which consists of $N$ designs paired with their property labels. In particular, the dataset is given by $\mathcal{D} = \{(\boldsymbol{x}_i, \boldsymbol{y}_i)\}\_{i=1}^{N}\,$ where each design vector $\boldsymbol{x}_i$ belongs to a design space $\mathcal{X} \subseteq \mathbb{R}^d$, and each property label $\boldsymbol{y}_i \in \mathbb{R}^m$ contains the corresponding $m$ objective values for that design. The function $\boldsymbol{f}: \mathcal{X} \rightarrow \mathbb{R}^m$ maps a design to its $m$-dimensional objective value vector.



In offline single-objective optimization (SOO), only one objective is considered (i.e., $m=1$). For instance, the design $\boldsymbol{x}$ might represent a neural network architecture, with $f(\boldsymbol{x})$ denoting the network's accuracy on a given dataset.



Offline multi-objective optimization (MOO) extends the framework to simultaneously address multiple objectives using the dataset $\mathcal{D}$. In this setting, the goal is to find solutions that balance competing objectives effectively. For instance, when designing a neural architecture, one might seek to achieve both high accuracy and high efficiency.

## 🔗 Benchmarks

### Tasks

#### Synthetic Functions

- [**Virtual Library of Simulation Experiments: Test Functions and Datasets**](https://www.sfu.ca/~ssurjano/optimization.html) **_Public Online_** 2013

- [**BayesO Benchmarks: Benchmark Functions for Bayesian Optimization**](https://github.com/jungtaekkim/bayeso-benchmarks) **_Public Online_** 2023

- [**Pymoo: Multi-Objective Optimization in Python**](https://ieeexplore.ieee.org/document/9078759) **_IEEE Access_** 2020
- [**Offline Multi-Objective Optimization**](https://arxiv.org/abs/2406.03722) **_ICML_** 2024

#### Real-World System

- [**An easy-to-use real-world multi-objective optimization problem suite**](https://www.sciencedirect.com/science/article/abs/pii/S1568494620300181) **_Applied Soft Computing_** 2020

- [**GTOPX space mission benchmarks**](https://www.sciencedirect.com/science/article/pii/S235271102100011X) **_SoftwareX_** 2021

- [**SOO-Bench: Benchmarks for Evaluating the Stability of Offline Black-Box Optimization**](https://openreview.net/forum?id=bqf0aCF3Dd) **_ICLR_** 2025

- [**Offline Multi-Objective Optimization**](https://arxiv.org/abs/2406.03722) **_ICML_** 2024

- [**Design-Bench: Benchmarks for Data-Driven Offline Model-Based Optimization**](https://proceedings.mlr.press/v162/trabucco22a.html) **_ICML_** 2022

- [**Data-Driven Offline Optimization for Architecting Hardware Accelerators**](https://openreview.net/forum?id=GsH-K1VIyy) **_ICLR_** 2022

#### Scientific Design

- [**ViennaRNA Package 2.0**](https://almob.biomedcentral.com/articles/10.1186/1748-7188-6-26) **_Algorithms for Molecular Biology_** 2011
- [**Conservative Objective Models for Effective Offline Model-Based Optimization**](https://arxiv.org/abs/2107.06882) **_ICML_** 2021

- [**Design-Bench: Benchmarks for Data-Driven Offline Model-Based Optimization**](https://proceedings.mlr.press/v162/trabucco22a.html) **_ICML_** 2022
- [**Proximal Exploration for Model-guided Protein Sequence Design**](https://proceedings.mlr.press/v162/ren22a.html) **_ICML_** 2022
- [**Antigen-Specific Antibody Design and Optimization with Diffusion-Based Generative Models for Protein Structures**](https://proceedings.neurips.cc/paper_files/paper/2022/hash/3fa7d76a0dc1179f1e98d1bc62403756-Abstract-Conference.html) **_NeurIPS_** 2022
- [**Offline Multi-Objective Optimization**](https://arxiv.org/abs/2406.03722) **_ICML_** 2024

- [**Latent Conservative Objective Models for Offline Data-Driven Crystal Structure Prediction**](https://openreview.net/forum?id=rAGYFtTQ-Zz) **_ICLR ml4materials_** 2023
- [**Bayesian Optimization of Active Materials for Lithium-Ion Batteries**](https://saemobilus.sae.org/papers/bayesian-optimization-active-materials-lithium-ion-batteries-2021-01-0765) **_IEEE IECON_** 2021

#### Machine Learning Model

- [**Design-Bench: Benchmarks for Data-Driven Offline Model-Based Optimization**](https://proceedings.mlr.press/v162/trabucco22a.html) **_ICML_** 2022
- [**Offline Multi-Objective Optimization**](https://arxiv.org/abs/2406.03722) **_ICML_** 2024
- [**HPOBench: A Collection of Reproducible Multi-Fidelity Benchmark Problems for HPO**](https://openreview.net/forum?id=1k4rJYEwda-) **_NeurIPS Datasets and Benchmarks Track_** 2021

### Evaluations

#### Usefulness

- [**Design-Bench: Benchmarks for Data-Driven Offline Model-Based Optimization**](https://proceedings.mlr.press/v162/trabucco22a.html) **_ICML_** 2022
- [**Biological Sequence Design with GFlowNets**](https://proceedings.mlr.press/v162/jain22a.html) **_ICML_** 2022
- [**Offline Multi-Objective Optimization**](https://arxiv.org/abs/2406.03722) **_ICML_** 2024
- [**ParetoFlow: Guided Flows in Multi-Objective Optimization**](https://openreview.net/forum?id=mLyyB4le5u) **_ICLR_** 2025

#### Diversity

- [**Biological Sequence Design with GFlowNets**](https://proceedings.mlr.press/v162/jain22a.html) **_ICML_** 2022
- [**Bootstrapped Training of Score-Conditioned Generator for Offline Design of Biological Sequences**](https://proceedings.neurips.cc/paper_files/paper/2023/hash/d601a9b708cacfad167f6c6c45647a18-Abstract-Conference.html) **_NeurIPS_** 2023
- [**Improving protein optimization with smoothed fitness landscapes**](https://openreview.net/forum?id=rxlF2Zv8x0) **_ICLR_** 2024
- [**Diversity By Design: Leveraging Distribution Matching for Offline Model-Based Optimization**](https://arxiv.org/abs/2501.18768) **_Public Online_** 2025

#### Novelty

- [**Biological Sequence Design with GFlowNets**](https://proceedings.mlr.press/v162/jain22a.html) **_ICML_** 2022
- [**Bootstrapped Training of Score-Conditioned Generator for Offline Design of Biological Sequences**](https://proceedings.neurips.cc/paper_files/paper/2023/hash/d601a9b708cacfad167f6c6c45647a18-Abstract-Conference.html) **_NeurIPS_** 2023
- [**Improving protein optimization with smoothed fitness landscapes**](https://openreview.net/forum?id=rxlF2Zv8x0) **_ICLR_** 2024

#### Stability

- [**SOO-Bench: Benchmarks for Evaluating the Stability of Offline Black-Box Optimization**](https://openreview.net/forum?id=bqf0aCF3Dd) **_ICLR_** 2025



## 🎯 Surrogate Models-based Methods

#### Auxiliary Loss

- [**Conservative Objective Models for Effective Offline Model-Based Optimization**](https://arxiv.org/abs/2107.06882) **_ICML_** 2021
- [**RoMA: Robust Model Adaptation for Offline Model-Based Optimization**](https://proceedings.neurips.cc/paper_files/paper/2021/hash/24b43fb034a10d78bec71274033b4096-Abstract.html) **_NeurIPS_** 2021
- [**Bidirectional Learning for Offline Infinite-width Model-Based Optimization**](https://proceedings.neurips.cc/paper_files/paper/2022/hash/bd391cf5bdc4b63674d6da3edc1bde0d-Abstract-Conference.html) **_NeurIPS_** 2022
- [**Data-Driven Offline Decision-Making via Invariant Representation Learning**](https://arxiv.org/abs/2211.11349) **_NeurIPS_** 2022
- [**Bidirectional Learning for Offline Model-Based Biological Sequence Design**](https://proceedings.mlr.press/v202/chen23ao.html) **_ICML_** 2023
- [**Parallel-mentoring for Offline Model-Based Optimization**](https://proceedings.neurips.cc/paper_files/paper/2023/hash/f189e7580acad0fc7fd45405817ddee3-Abstract-Conference.html) **_NeurIPS_** 2023
- [**Learning Surrogates for Offline Black-Box Optimization via Gradient Matching**](https://openreview.net/forum?id=mv9beA1wDF) **_ICML_** 2024
- [**Boosting Offline Optimizers with Surrogate Sensitivity**](https://openreview.net/forum?id=aLSA3JH08h&referrer=%5Bthe%20profile%20of%20Manh%20Cuong%20Dao%5D(%2Fprofile%3Fid%3D~Manh_Cuong_Dao1)) **_ICML_** 2024 
- [**Incorporating Surrogate Gradient Norm to Improve Offline Optimization Techniques**](https://proceedings.neurips.cc/paper_files/paper/2024/hash/0f588c9d9fa34762362697c1dd463294-Abstract-Conference.html) **_NeurIPS_** 2024
- [**Offline Model-Based Optimization by Learning to Rank**](https://openreview.net/forum?id=sb1HgVDLjN) **_ICLR_** 2025

#### Data-Drive Adaptation

- [**Autofocused oracles for Model-Based design**](https://proceedings.neurips.cc/paper/2020/hash/972cda1e62b72640cb7ac702714a115f-Abstract.html) **_NeurIPS_** 2020
- [**Conservative Objective Models for Effective Offline Model-Based Optimization**](https://arxiv.org/abs/2107.06882) **_ICML_** 2021
- [**Bidirectional Learning for Offline Model-Based Biological Sequence Design**](https://proceedings.mlr.press/v202/chen23ao.html) **_ICML_** 2023
- [**Parallel-mentoring for Offline Model-Based Optimization**](https://proceedings.neurips.cc/paper_files/paper/2023/hash/f189e7580acad0fc7fd45405817ddee3-Abstract-Conference.html) **_NeurIPS_** 2023
- [**Importance-aware Co-teaching for Offline Model-Based Optimization**](https://proceedings.neurips.cc/paper_files/paper/2023/hash/ae8b0b5838ba510daff1198474e7b984-Abstract-Conference.html) **_NeurIPS_** 2023
- [**Functional Graphical Models: Structure Enables Offline Data-Driven Optimization**](https://arxiv.org/abs/2401.05442) **_AISTATS_** 2024

#### Collaborative Ensembling

- [**Offline Model-Based Optimization via Normalized Maximum Likelihood Estimation**](https://arxiv.org/abs/2102.07970) **_ICLR_** 2021
- [**Conflict-Averse Gradient Optimization of Ensembles for Effective Offline Model-Based Optimization**](https://arxiv.org/abs/2303.17934) **_Public Online_** 2023
- [**Parallel-mentoring for Offline Model-Based Optimization**](https://proceedings.neurips.cc/paper_files/paper/2023/hash/f189e7580acad0fc7fd45405817ddee3-Abstract-Conference.html) **_NeurIPS_** 2023
- [**Importance-aware Co-teaching for Offline Model-Based Optimization**](https://proceedings.neurips.cc/paper_files/paper/2023/hash/ae8b0b5838ba510daff1198474e7b984-Abstract-Conference.html) **_NeurIPS_** 2023

#### Generative Model Integration

- [**Autofocused oracles for Model-Based design**](https://proceedings.neurips.cc/paper/2020/hash/972cda1e62b72640cb7ac702714a115f-Abstract.html) **_NeurIPS_** 2020
- [**Data-Driven Offline Decision-Making via Invariant Representation Learning**](https://arxiv.org/abs/2211.11349) **_NeurIPS_** 2022
- [**Robust Guided Diffusion for Offline Black-Box Optimization**](https://arxiv.org/abs/2410.00983) **_TMLR_** 2024

## 🤔 Generative Models-based Methods

#### Variational Autoencoders (VAE)

- [**Automatic chemical design using a data-driven continuous representation of molecules**](https://arxiv.org/abs/1610.02415) **_ACS central science_** 2018
- [**Conditioning by adaptive sampling for robust design**](https://proceedings.mlr.press/v97/brookes19a.html) **_ICML_** 2019
- [**RoMA: Robust Model Adaptation for Offline Model-Based Optimization**](https://proceedings.neurips.cc/paper_files/paper/2021/hash/24b43fb034a10d78bec71274033b4096-Abstract.html) **_NeurIPS_** 2021
- [**Latent Bayesian Optimization via Autoregressive Normalizing Flows**](https://openreview.net/forum?id=ZCOwwRAaEl) **_ICLR_** 2025

#### Generative Adversarial Networks (GAN)

- [**Model Inversion Networks for Model-Based Optimization**](https://proceedings.neurips.cc/paper/2020/hash/373e4c5d8edfa8b74fd4b6791d0cf6dc-Abstract.html) **_NeurIPS_** 2019
- [**Data-Driven Offline Decision-Making via Invariant Representation Learning**](https://arxiv.org/abs/2211.11349) **_NeurIPS_** 2022
- [**Generative Adversarial Model-Based Optimization via Source Critic Regularization**](https://proceedings.neurips.cc/paper_files/paper/2024/hash/4dd0a016d7d253d02473e4778414ab0b-Abstract-Conference.html) **_NeurIPS_** 2024

#### Autoregressive Models

- [**Plug and Play Language Models: A Simple Approach to Controlled Text Generation**](https://openreview.net/forum?id=H1edEyBKDS) **_ICLR_** 2020
- [**Model-Based reinforcement learning for biological sequence design**](https://openreview.net/forum?id=HklxbgBKvr) **_ICLR_** 2020
- [**Generative Pretraining for Black-Box Optimization**](https://arxiv.org/abs/2206.10786) **_ICML_** 2022
- [**Bootstrapped Training of Score-Conditioned Generator for Offline Design of Biological Sequences**](https://proceedings.neurips.cc/paper_files/paper/2023/hash/d601a9b708cacfad167f6c6c45647a18-Abstract-Conference.html) **_NeurIPS_** 2023
- [**ExPT: Synthetic Pretraining for Few-Shot Experimental Design**](https://proceedings.neurips.cc/paper_files/paper/2023/hash/8fab4407e1fe9006b39180525c0d323c-Abstract-Conference.html) **_NeurIPS_** 2023

#### Diffusion Models

- [**Diffusion Models for Black-Box Optimization**](https://arxiv.org/abs/2306.07180) **_ICML_** 2023
- [**Exploring Chemical Space with Score-based Out-of-distribution Generation**](https://arxiv.org/abs/2206.07632) **_ICML_** 2023
- [**Robust Guided Diffusion for Offline Black-Box Optimization**](https://arxiv.org/abs/2410.00983) **_TMLR_** 2024
- [**Guided Trajectory Generation with Diffusion Models for Offline Model-Based Optimization**](https://proceedings.neurips.cc/paper_files/paper/2024/hash/98904db124b2a2463e8c59ec33fc7150-Abstract-Conference.html) **_NeurIPS_** 2024
- [**Design Editing for Offline Model-Based Optimization**](https://arxiv.org/abs/2405.13964) **_Public Online_** 2024
- [**Low To High-value Designs: Offline Optimization Via Generalized Diffusion**](https://openreview.net/forum?id=K9Elg2JrvY) **_Public Online_** 2025

#### Flow Matching

- [**Dirichlet Flow Matching with Applications to DNA Sequence Design**](https://proceedings.mlr.press/v235/stark24b.html) **_ICML_** 2024

- [**ParetoFlow: Guided Flows in Multi-Objective Optimization**](https://openreview.net/forum?id=mLyyB4le5u) **_ICLR_** 2025
- [**Flow Q-Learning**](https://arxiv.org/abs/2502.02538) **_Public Online_** 2025
- [**AffinityFlow: Guided Flows for Antibody Affinity Maturation**](https://arxiv.org/abs/2502.10365) **_Public Online_** 2025

#### Energy-based Models

- [**Conservative objective models are a special kind of contrastive divergence-based energy model**](https://arxiv.org/abs/2304.03866) **_Public Online_** 2023

- [**Protein Discovery with Discrete Walk-Jump Sampling**](https://openreview.net/forum?id=zMPHKOmQNb) **_ICLR_** 2024
- [**Latent Energy-Based Odyssey: Black-Box Optimization via Expanded Exploration in the Energy-Based Latent Space**](https://arxiv.org/abs/2405.16730) **_Public Online_** 2024

#### Control by Generative Flow Networks (GFlowNet)

- [**Biological Sequence Design with GFlowNets**](https://proceedings.mlr.press/v162/jain22a.html) **_ICML_** 2022
- [**Multi-Objective GFlowNets**](https://proceedings.mlr.press/v202/jain23a.html) **_ICML_** 2023
- [**Generative Flow Networks Assisted Biological Sequence Editing**](https://openreview.net/forum?id=9BQ3l8OVru) **_NeurIPS GenBio_** 2023
- [**Improved Off-policy Reinforcement Learning in Biological Sequence Design**](https://arxiv.org/abs/2410.04461) **_NeurIPS AI for New Drug Modalities_** 2024
- [**Learning to Scale Logits for Temperature-Conditional GFlowNets**](https://arxiv.org/abs/2310.02823) **_ICML_** 2024
- [**Posterior Inference with Diffusion Models for High-dimensional Black-box Optimization**](https://arxiv.org/abs/2502.16824) **_Public Online_** 2025




## 🤗 Contribution

### Contributors

[Ye Yuan](https://mila.quebec/en/directory/ye-yuan)

### Contributing to this project

Please feel free to file a PR for contributing to this project! Thanks so much for your help!

### Acknowledgement

TBD
