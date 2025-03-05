# Awesome-Offline-Model-Based-Optimization

📰 Must-Read Papers on Offline Model-Based Optimization 🔥

This repository collects important papers for our new survey: **"Offline Model-Based Optimization: Comprehensive Review"** (will release soon).

[![Awesome](https://awesome.re/badge.svg)](https://github.com/StevenYuan666/Awesome-Offline-Model-Based-Optimization)
![](https://img.shields.io/github/last-commit/StevenYuan666/Awesome-Offline-Model-Based-Optimization?color=green)
![](https://img.shields.io/badge/PRs-Welcome-red)
![Stars](https://img.shields.io/github/stars/mila-iqia/Awesome-Offline-Model-Based-Optimization?color=yellow&label=Stars) ![Forks](https://img.shields.io/github/forks/mila-iqia/Awesome-Offline-Model-Based-Optimization?color=green&label=Forks)

+ 💻: `Code`
+ 📖: `bibtex`


## Latest Updates
+ [2025/03/04] First Release of Awesome-Offline-Model-Based Optimization

## 🔍 Table of Contents

- [🌟 What is Offline Model-Based Optimization?](#-definition)
- [🔗 Benchmarks](#-Benchmarks)
- [🎯 Surrogate Models-Based Methods](#-Surrogate-Models-Based-Methods)
- [🤔 Generative Models-Based Methods](#-Generative-Models-Based-Methods)
- [🤗 Contribution](#-contribution)
  - [Contributors](#contributors)
  - [Acknowledgement](#acknowledgement)

## 🌟 What is Offline Model-Based Optimization?

In offline optimization, the goal is to discover a new design, denoted by $\boldsymbol{x}^*$, that maximizes the objective(s) $\boldsymbol{f}(\boldsymbol{x})$. This is achieved using an offline dataset $\mathcal{D}$, which consists of $N$ designs paired with their property labels. In particular, the dataset is given by ![Offline Dataset](https://quicklatex.com/cache3/e5/ql_1122a332dc128c100abf9c546c902be5_l3.png) where each design vector $\boldsymbol{x}_i$ belongs to a design space $\mathcal{X} \subseteq \mathbb{R}^d$, and each property label $\boldsymbol{y}_i \in \mathbb{R}^m$ contains the corresponding $m$ objective values for that design. The function $\boldsymbol{f}: \mathcal{X} \rightarrow \mathbb{R}^m$ maps a design to its $m$-dimensional objective value vector.



In offline single-objective optimization (SOO), only one objective is considered (i.e., $m=1$). For instance, the design $\boldsymbol{x}$ might represent a neural network architecture, with $f(\boldsymbol{x})$ denoting the network's accuracy on a given dataset.



Offline multi-objective optimization (MOO) extends the framework to simultaneously address multiple objectives using the dataset $\mathcal{D}$. In this setting, the goal is to find solutions that balance competing objectives effectively. For instance, when designing a neural architecture, one might seek to achieve both high accuracy and high efficiency.

## 🔗 Benchmarks

### Tasks

#### Synthetic Functions

- [**Virtual Library of Simulation Experiments: Test Functions and Datasets**](https://www.sfu.ca/~ssurjano/optimization.html) (Sonja Surjanovic & Derek Bingham, 2013) [💻](https://www.sfu.ca/~ssurjano/optimization.html) [📖](https://github.com/mila-iqia/Awesome-Offline-Model-Based-Optimization/blob/main/bibtex/simulationlib.txt)

- [**BayesO Benchmarks: Benchmark Functions for Bayesian Optimization**](https://github.com/jungtaekkim/bayeso-benchmarks) (Jungtaek Kim, 2023) [💻](https://github.com/jungtaekkim/bayeso-benchmarks) [📖](https://github.com/mila-iqia/Awesome-Offline-Model-Based-Optimization/blob/main/bibtex/bayeso.txt)

- [**Pymoo: Multi-Objective Optimization in Python**](https://ieeexplore.ieee.org/document/9078759) (Julian Blank & Kalyanmoy Ded, IEEE Access 2020) [💻](https://github.com/anyoptimization/pymoo) [📖](https://github.com/mila-iqia/Awesome-Offline-Model-Based-Optimization/blob/main/bibtex/pymoo.txt)
- [**Offline Multi-Objective Optimization**](https://arxiv.org/abs/2406.03722) (Ke Xue & Rong-Xi Tan et al., ICML 2024) [💻](https://github.com/lamda-bbo/offline-moo) [📖](https://github.com/mila-iqia/Awesome-Offline-Model-Based-Optimization/blob/main/bibtex/offline_moo.txt)

#### Real-World System

- [**An Easy-to-Use Real-World Multi-Objective Optimization Problem Suite**](https://www.sciencedirect.com/science/article/abs/pii/S1568494620300181) (Ryoji Tanabe et al., Applied Soft Computing 2020) [💻](https://github.com/ryojitanabe/reproblems) [📖](https://github.com/mila-iqia/Awesome-Offline-Model-Based-Optimization/blob/main/bibtex/re_suite.txt)

- [**GTOPX Space Mission Benchmarks**](https://www.sciencedirect.com/science/article/pii/S235271102100011X) (Martin Schlueter et al., SoftwareX 2021) [💻](https://www.midaco-solver.com/index.php/about/benchmarks/gtopx) [📖](https://github.com/mila-iqia/Awesome-Offline-Model-Based-Optimization/blob/main/bibtex/gtopx.txt)

- [**SOO-Bench: Benchmarks for Evaluating the Stability of Offline Black-Box Optimization**](https://openreview.net/forum?id=bqf0aCF3Dd) (Hong Qian et al., ICLR 2025) [💻](https://github.com/zhuyiyi-123/SOO-Bench) [📖](https://github.com/mila-iqia/Awesome-Offline-Model-Based-Optimization/blob/main/bibtex/soo.txt)

- [**Offline Multi-Objective Optimization**](https://arxiv.org/abs/2406.03722) (Ke Xue & Rong-Xi Tan et al., ICML 2024) [💻](https://github.com/lamda-bbo/offline-moo) [📖](https://github.com/mila-iqia/Awesome-Offline-Model-Based-Optimization/blob/main/bibtex/offline_moo.txt)

- [**Design-Bench: Benchmarks for Data-Driven Offline Model-Based Optimization**](https://proceedings.mlr.press/v162/trabucco22a.html) (Brandon Trabucco & Xinyang Geng et al., ICML 2022) [💻](https://github.com/brandontrabucco/design-bench) [📖](https://github.com/mila-iqia/Awesome-Offline-Model-Based-Optimization/blob/main/bibtex/design_bench.txt)

- [**Data-Driven Offline Optimization for Architecting Hardware Accelerators**](https://openreview.net/forum?id=GsH-K1VIyy) (Aviral Kumar & Amir Yazdanbakhsh et al., ICLR 2022) [💻](https://github.com/google-research/google-research/tree/master/prime) [📖](https://github.com/mila-iqia/Awesome-Offline-Model-Based-Optimization/blob/main/bibtex/hardware.txt)

#### Scientific Design

- [**ViennaRNA Package 2.0**](https://almob.biomedcentral.com/articles/10.1186/1748-7188-6-26) (Ronny Lorenz et al., Algorithms for Molecular Biology 2011) [💻](https://www.tbi.univie.ac.at/RNA/) [📖](https://github.com/mila-iqia/Awesome-Offline-Model-Based-Optimization/blob/main/bibtex/vienna_rna.txt)
- [**Conservative Objective Models for Effective Offline Model-Based Optimization**](https://arxiv.org/abs/2107.06882) (Brandon Trabucco & Aviral Kumar et al., ICML 2021) [💻](https://github.com/brandontrabucco/design-baselines) [📖](https://github.com/mila-iqia/Awesome-Offline-Model-Based-Optimization/blob/main/bibtex/coms.txt)

- [**Design-Bench: Benchmarks for Data-Driven Offline Model-Based Optimization**](https://proceedings.mlr.press/v162/trabucco22a.html) (Brandon Trabucco & Xinyang Geng et al., ICML 2022) [💻](https://github.com/brandontrabucco/design-bench) [📖](https://github.com/mila-iqia/Awesome-Offline-Model-Based-Optimization/blob/main/bibtex/design_bench.txt)
- [**Proximal Exploration for Model-Guided Protein Sequence Design**](https://proceedings.mlr.press/v162/ren22a.html) (Zhizhou Ren & Jiahan Li et al., ICML 2022) [💻](https://github.com/HeliXonProtein/proximal-exploration) [📖](https://github.com/mila-iqia/Awesome-Offline-Model-Based-Optimization/blob/main/bibtex/proximal.txt)
- [**Antigen-Specific Antibody Design and Optimization with Diffusion-Based Generative Models for Protein Structures**](https://proceedings.neurips.cc/paper_files/paper/2022/hash/3fa7d76a0dc1179f1e98d1bc62403756-Abstract-Conference.html) (Shitong Luo & Yufeng Su et al., NeurIPS 2022) [💻](https://github.com/luost26/diffab) [📖](https://github.com/mila-iqia/Awesome-Offline-Model-Based-Optimization/blob/main/bibtex/antigen.txt)
- [**Offline Multi-Objective Optimization**](https://arxiv.org/abs/2406.03722) (Ke Xue & Rong-Xi Tan et al., ICML 2024) [💻](https://github.com/lamda-bbo/offline-moo) [📖](https://github.com/mila-iqia/Awesome-Offline-Model-Based-Optimization/blob/main/bibtex/offline_moo.txt)

- [**Latent Conservative Objective Models for Offline Data-Driven Crystal Structure Prediction**](https://openreview.net/forum?id=rAGYFtTQ-Zz) (Han Qi & Xinyang Geng et al., ICLR ML4Materials 2023) [📖](https://github.com/mila-iqia/Awesome-Offline-Model-Based-Optimization/blob/main/bibtex/latent_crystal.txt)
- [**Bayesian Optimization of Active Materials for Lithium-Ion Batteries**](https://saemobilus.sae.org/papers/bayesian-optimization-active-materials-lithium-ion-batteries-2021-01-0765) (Homero Valladares et al., IEEE IECON 2021) [📖](https://github.com/mila-iqia/Awesome-Offline-Model-Based-Optimization/blob/main/bibtex/battery.txt)

#### Machine Learning Model

- [**Design-Bench: Benchmarks for Data-Driven Offline Model-Based Optimization**](https://proceedings.mlr.press/v162/trabucco22a.html) (Brandon Trabucco & Xinyang Geng et al., ICML 2022) [💻](https://github.com/brandontrabucco/design-bench) [📖](https://github.com/mila-iqia/Awesome-Offline-Model-Based-Optimization/blob/main/bibtex/design_bench.txt)
- [**Offline Multi-Objective Optimization**](https://arxiv.org/abs/2406.03722) (Ke Xue & Rong-Xi Tan et al., ICML 2024) [💻](https://github.com/lamda-bbo/offline-moo) [📖](https://github.com/mila-iqia/Awesome-Offline-Model-Based-Optimization/blob/main/bibtex/offline_moo.txt)
- [**HPOBench: A Collection of Reproducible Multi-Fidelity Benchmark Problems for HPO**](https://openreview.net/forum?id=1k4rJYEwda-) (Katharina Eggensperger et al., NeurIPS Datasets and Benchmarks Track 2021) [💻](https://github.com/automl/HPOBench) [📖](https://github.com/mila-iqia/Awesome-Offline-Model-Based-Optimization/blob/main/bibtex/hpobench.txt)

### Evaluations

#### Usefulness

- [**Design-Bench: Benchmarks for Data-Driven Offline Model-Based Optimization**](https://proceedings.mlr.press/v162/trabucco22a.html) (Brandon Trabucco & Xinyang Geng et al., ICML 2022) [💻](https://github.com/brandontrabucco/design-bench) [📖](https://github.com/mila-iqia/Awesome-Offline-Model-Based-Optimization/blob/main/bibtex/design_bench.txt)
- [**Biological Sequence Design with GFlowNets**](https://proceedings.mlr.press/v162/jain22a.html) (Moksh Jain et al., ICML 2022) [💻](https://github.com/MJ10/BioSeq-GFN-AL) [📖](https://github.com/mila-iqia/Awesome-Offline-Model-Based-Optimization/blob/main/bibtex/biosequence_gflownet.txt)
- [**Offline Multi-Objective Optimization**](https://arxiv.org/abs/2406.03722) (Ke Xue & Rong-Xi Tan et al., ICML 2024) [💻](https://github.com/lamda-bbo/offline-moo) [📖](https://github.com/mila-iqia/Awesome-Offline-Model-Based-Optimization/blob/main/bibtex/offline_moo.txt)
- [**ParetoFlow: Guided Flows in Multi-Objective Optimization**](https://openreview.net/forum?id=mLyyB4le5u) (Ye Yuan & Can Chen et al., ICLR 2025) [💻](https://github.com/mila-iqia/ParetoFlow) [📖](https://github.com/mila-iqia/Awesome-Offline-Model-Based-Optimization/blob/main/bibtex/paretoflow.txt)

#### Diversity

- [**Biological Sequence Design with GFlowNets**](https://proceedings.mlr.press/v162/jain22a.html) (Moksh Jain et al., ICML 2022) [💻](https://github.com/MJ10/BioSeq-GFN-AL) [📖](https://github.com/mila-iqia/Awesome-Offline-Model-Based-Optimization/blob/main/bibtex/biosequence_gflownet.txt)
- [**Bootstrapped Training of Score-Conditioned Generator for Offline Design of Biological Sequences**](https://proceedings.neurips.cc/paper_files/paper/2023/hash/d601a9b708cacfad167f6c6c45647a18-Abstract-Conference.html) (Minsu Kim et al., NeurIPS 2023) [💻](https://github.com/kaist-silab/bootgen) [📖](https://github.com/mila-iqia/Awesome-Offline-Model-Based-Optimization/blob/main/bibtex/bootgen.txt)
- [**Improving Protein Optimization with Smoothed Fitness Landscapes**](https://openreview.net/forum?id=rxlF2Zv8x0) (Andrew Kirjner & Jason Yim et al., ICLR 2024) [💻](https://github.com/kirjner/GGS) [📖](https://github.com/mila-iqia/Awesome-Offline-Model-Based-Optimization/blob/main/bibtex/ggs.txt)
- [**Diversity By Design: Leveraging Distribution Matching for Offline Model-Based Optimization**](https://arxiv.org/abs/2501.18768) (Michael S. Yao et al., 2025) [💻](https://github.com/michael-s-yao/DynAMO) [📖](https://github.com/mila-iqia/Awesome-Offline-Model-Based-Optimization/blob/main/bibtex/diversitybydesign.txt)

#### Novelty

- [**Biological Sequence Design with GFlowNets**](https://proceedings.mlr.press/v162/jain22a.html) (Moksh Jain et al., ICML 2022) [💻](https://github.com/MJ10/BioSeq-GFN-AL) [📖](https://github.com/mila-iqia/Awesome-Offline-Model-Based-Optimization/blob/main/bibtex/biosequence_gflownet.txt)
- [**Bootstrapped Training of Score-Conditioned Generator for Offline Design of Biological Sequences**](https://proceedings.neurips.cc/paper_files/paper/2023/hash/d601a9b708cacfad167f6c6c45647a18-Abstract-Conference.html) (Minsu Kim et al., NeurIPS 2023) [💻](https://github.com/kaist-silab/bootgen) [📖](https://github.com/mila-iqia/Awesome-Offline-Model-Based-Optimization/blob/main/bibtex/bootgen.txt)
- [**Improving Protein Optimization with Smoothed Fitness Landscapes**](https://openreview.net/forum?id=rxlF2Zv8x0) (Andrew Kirjner & Jason Yim et al., ICLR 2024) [💻](https://github.com/kirjner/GGS) [📖](https://github.com/mila-iqia/Awesome-Offline-Model-Based-Optimization/blob/main/bibtex/ggs.txt)

#### Stability

- [**SOO-Bench: Benchmarks for Evaluating the Stability of Offline Black-Box Optimization**](https://openreview.net/forum?id=bqf0aCF3Dd) (Hong Qian et al., ICLR 2025) [💻](https://github.com/zhuyiyi-123/SOO-Bench) [📖](https://github.com/mila-iqia/Awesome-Offline-Model-Based-Optimization/blob/main/bibtex/soo.txt)



## 🎯 Surrogate Models-Based Methods

#### Auxiliary Loss

- [**Conservative Objective Models for Effective Offline Model-Based Optimization**](https://arxiv.org/abs/2107.06882) (Brandon Trabucco & Aviral Kumar et al., ICML 2021) [💻](https://github.com/brandontrabucco/design-baselines) [📖](https://github.com/mila-iqia/Awesome-Offline-Model-Based-Optimization/blob/main/bibtex/coms.txt)
- [**RoMA: Robust Model Adaptation for Offline Model-Based Optimization**](https://proceedings.neurips.cc/paper_files/paper/2021/hash/24b43fb034a10d78bec71274033b4096-Abstract.html) (Sihyun Yu et al., NeurIPS 2021) [💻](https://github.com/sihyun-yu/RoMA) [📖](https://github.com/mila-iqia/Awesome-Offline-Model-Based-Optimization/blob/main/bibtex/roma.txt)
- [**Bidirectional Learning for Offline Infinite-Width Model-Based Optimization**](https://proceedings.neurips.cc/paper_files/paper/2022/hash/bd391cf5bdc4b63674d6da3edc1bde0d-Abstract-Conference.html) (Can Chen et al., NeurIPS 2022) [💻](https://github.com/GGchen1997/BDI) [📖](https://github.com/mila-iqia/Awesome-Offline-Model-Based-Optimization/blob/main/bibtex/bdi.txt)
- [**Data-Driven Offline Decision-Making via Invariant Representation Learning**](https://arxiv.org/abs/2211.11349) (Han Qi & Yi Su & Aviral Kumar et al., NeurIPS 2022) [💻](https://sites.google.com/view/iom-neurips) [📖](https://github.com/mila-iqia/Awesome-Offline-Model-Based-Optimization/blob/main/bibtex/iom.txt)
- [**Bidirectional Learning for Offline Model-Based Biological Sequence Design**](https://proceedings.mlr.press/v202/chen23ao.html) (Can Chen et al., ICML 2023) [💻](https://github.com/GGchen1997/BIB-ICML2023-Submission) [📖](https://github.com/mila-iqia/Awesome-Offline-Model-Based-Optimization/blob/main/bibtex/bib.txt)
- [**Parallel-Mentoring for Offline Model-Based Optimization**](https://proceedings.neurips.cc/paper_files/paper/2023/hash/f189e7580acad0fc7fd45405817ddee3-Abstract-Conference.html) (Can Chen et al., NeurIPS 2023) [💻](https://github.com/GGchen1997/parallel_mentoring) [📖](https://github.com/mila-iqia/Awesome-Offline-Model-Based-Optimization/blob/main/bibtex/parallel_mentor.txt)
- [**Learning Surrogates for Offline Black-Box Optimization via Gradient Matching**](https://openreview.net/forum?id=mv9beA1wDF) (Minh Hoang et al., ICML 2024) [💻](https://github.com/azzafadhel/MatchOpt) [📖](https://github.com/mila-iqia/Awesome-Offline-Model-Based-Optimization/blob/main/bibtex/matchopt.txt)
- [**Boosting Offline Optimizers with Surrogate Sensitivity**](https://openreview.net/forum?id=aLSA3JH08h&referrer=%5Bthe%20profile%20of%20Manh%20Cuong%20Dao%5D(%2Fprofile%3Fid%3D~Manh_Cuong_Dao1)) (Manh Cuong Dao et al., ICML 2024)  [💻](https://github.com/cuong-dm/BOSS) [📖](https://github.com/mila-iqia/Awesome-Offline-Model-Based-Optimization/blob/main/bibtex/boss.txt)
- [**Incorporating Surrogate Gradient Norm to Improve Offline Optimization Techniques**](https://proceedings.neurips.cc/paper_files/paper/2024/hash/0f588c9d9fa34762362697c1dd463294-Abstract-Conference.html) (Manh Cuong Dao et al., NeurIPS 2024) [💻](https://github.com/cuong-dm/IGNITE) [📖](https://github.com/mila-iqia/Awesome-Offline-Model-Based-Optimization/blob/main/bibtex/ignite.txt)
- [**Offline Model-Based Optimization by Learning to Rank**](https://openreview.net/forum?id=sb1HgVDLjN) (Rong-Xi Tan et al., ICLR 2025) [💻](https://github.com/lamda-bbo/Offline-RaM) [📖](https://github.com/mila-iqia/Awesome-Offline-Model-Based-Optimization/blob/main/bibtex/learning2rank.txt)

#### Data-Drive Adaptation

- [**Autofocused Oracles for Model-Based Design**](https://proceedings.neurips.cc/paper/2020/hash/972cda1e62b72640cb7ac702714a115f-Abstract.html) (Clara Fannjiang et al., NeurIPS 2020) [💻](https://github.com/clarafy/autofocused-oracles) [📖](https://github.com/mila-iqia/Awesome-Offline-Model-Based-Optimization/blob/main/bibtex/autofocused.txt)
- [**Conservative Objective Models for Effective Offline Model-Based Optimization**](https://arxiv.org/abs/2107.06882) (Brandon Trabucco & Aviral Kumar et al., ICML 2021) [💻](https://github.com/brandontrabucco/design-baselines) [📖](https://github.com/mila-iqia/Awesome-Offline-Model-Based-Optimization/blob/main/bibtex/coms.txt)
- [**Bidirectional Learning for Offline Model-Based Biological Sequence Design**](https://proceedings.mlr.press/v202/chen23ao.html) (Can Chen et al., ICML 2023) [💻](https://github.com/GGchen1997/BIB-ICML2023-Submission) [📖](https://github.com/mila-iqia/Awesome-Offline-Model-Based-Optimization/blob/main/bibtex/bib.txt)
- [**Parallel-Mentoring for Offline Model-Based Optimization**](https://proceedings.neurips.cc/paper_files/paper/2023/hash/f189e7580acad0fc7fd45405817ddee3-Abstract-Conference.html) (Can Chen et al., NeurIPS 2023) [💻](https://github.com/GGchen1997/parallel_mentoring) [📖](https://github.com/mila-iqia/Awesome-Offline-Model-Based-Optimization/blob/main/bibtex/parallel_mentor.txt)
- [**Importance-Aware Co-Teaching for Offline Model-Based Optimization**](https://proceedings.neurips.cc/paper_files/paper/2023/hash/ae8b0b5838ba510daff1198474e7b984-Abstract-Conference.html) (Ye Yuan & Can Chen et al., NeurIPS 2023) [💻](https://github.com/mila-iqia/Importance-aware-Co-teaching) [📖](https://github.com/mila-iqia/Awesome-Offline-Model-Based-Optimization/blob/main/bibtex/ict.txt)
- [**Functional Graphical Models: Structure Enables Offline Data-Driven Optimization**](https://arxiv.org/abs/2401.05442) (Jakub Grudzien Kuba et al., AISTATS 2024) [📖](https://github.com/mila-iqia/Awesome-Offline-Model-Based-Optimization/blob/main/bibtex/fgm.txt)

#### Collaborative Ensembling

- [**Offline Model-Based Optimization via Normalized Maximum Likelihood Estimation**](https://arxiv.org/abs/2102.07970) (Justin Fu et al., ICLR 2021) [💻](https://sites.google.com/view/nemo-anonymous) [📖](https://github.com/mila-iqia/Awesome-Offline-Model-Based-Optimization/blob/main/bibtex/nemo.txt)
- [**Conflict-Averse Gradient Optimization of Ensembles for Effective Offline Model-Based Optimization**](https://arxiv.org/abs/2303.17934) (Sathvik Kolli, 2023) [📖](https://github.com/mila-iqia/Awesome-Offline-Model-Based-Optimization/blob/main/bibtex/conflictaverse.txt)
- [**Parallel-Mentoring for Offline Model-Based Optimization**](https://proceedings.neurips.cc/paper_files/paper/2023/hash/f189e7580acad0fc7fd45405817ddee3-Abstract-Conference.html) (Can Chen et al., NeurIPS 2023) [💻](https://github.com/GGchen1997/parallel_mentoring) [📖](https://github.com/mila-iqia/Awesome-Offline-Model-Based-Optimization/blob/main/bibtex/parallel_mentor.txt)
- [**Importance-Aware Co-Teaching for Offline Model-Based Optimization**](https://proceedings.neurips.cc/paper_files/paper/2023/hash/ae8b0b5838ba510daff1198474e7b984-Abstract-Conference.html) (Ye Yuan & Can Chen et al., NeurIPS 2023) [💻](https://github.com/mila-iqia/Importance-aware-Co-teaching) [📖](https://github.com/mila-iqia/Awesome-Offline-Model-Based-Optimization/blob/main/bibtex/ict.txt)

#### Generative Model Integration

- [**Autofocused Oracles for Model-Based Design**](https://proceedings.neurips.cc/paper/2020/hash/972cda1e62b72640cb7ac702714a115f-Abstract.html) (Clara Fannjiang et al., NeurIPS 2020) [💻](https://github.com/clarafy/autofocused-oracles) [📖](https://github.com/mila-iqia/Awesome-Offline-Model-Based-Optimization/blob/main/bibtex/autofocused.txt)
- [**Data-Driven Offline Decision-Making via Invariant Representation Learning**](https://arxiv.org/abs/2211.11349) (Han Qi & Yi Su & Aviral Kumar et al., NeurIPS 2022) [💻](https://sites.google.com/view/iom-neurips) [📖](https://github.com/mila-iqia/Awesome-Offline-Model-Based-Optimization/blob/main/bibtex/iom.txt)
- [**Robust Guided Diffusion for Offline Black-Box Optimization**](https://arxiv.org/abs/2410.00983) (Can Chen et al., TMLR 2024) [💻](https://github.com/GGchen1997/RGD) [📖](https://github.com/mila-iqia/Awesome-Offline-Model-Based-Optimization/blob/main/bibtex/rgd.txt)

## 🤔 Generative Models-Based Methods

#### Variational Autoencoders (VAE)

- [**Automatic Chemical Design using a Data-Driven Continuous Representation of Molecules**](https://arxiv.org/abs/1610.02415) **_ACS central science_** 2018 [💻]() [📖]()
- [**Conditioning by Adaptive Sampling for Robust Design**](https://proceedings.mlr.press/v97/brookes19a.html) **_ICML_** 2019 [💻]() [📖]()
- [**RoMA: Robust Model Adaptation for Offline Model-Based Optimization**](https://proceedings.neurips.cc/paper_files/paper/2021/hash/24b43fb034a10d78bec71274033b4096-Abstract.html) (Sihyun Yu et al., NeurIPS 2021) [💻](https://github.com/sihyun-yu/RoMA) [📖](https://github.com/mila-iqia/Awesome-Offline-Model-Based-Optimization/blob/main/bibtex/roma.txt)
- [**Latent Bayesian Optimization via Autoregressive Normalizing Flows**](https://openreview.net/forum?id=ZCOwwRAaEl) **_ICLR_** 2025 [💻]() [📖]()

#### Generative Adversarial Networks (GAN)

- [**Model Inversion Networks for Model-Based Optimization**](https://proceedings.neurips.cc/paper/2020/hash/373e4c5d8edfa8b74fd4b6791d0cf6dc-Abstract.html) **_NeurIPS_** 2019 [💻]() [📖]()
- [**Data-Driven Offline Decision-Making via Invariant Representation Learning**](https://arxiv.org/abs/2211.11349) (Han Qi & Yi Su & Aviral Kumar et al., NeurIPS 2022) [💻](https://sites.google.com/view/iom-neurips) [📖](https://github.com/mila-iqia/Awesome-Offline-Model-Based-Optimization/blob/main/bibtex/iom.txt)
- [**Generative Adversarial Model-Based Optimization via Source Critic Regularization**](https://proceedings.neurips.cc/paper_files/paper/2024/hash/4dd0a016d7d253d02473e4778414ab0b-Abstract-Conference.html) **_NeurIPS_** 2024 [💻]() [📖]()

#### Autoregressive Models

- [**Plug and Play Language Models: A Simple Approach to Controlled Text Generation**](https://openreview.net/forum?id=H1edEyBKDS) **_ICLR_** 2020 [💻]() [📖]()
- [**Model-Based Reinforcement Learning for Biological Sequence Design**](https://openreview.net/forum?id=HklxbgBKvr) **_ICLR_** 2020 [💻]() [📖]()
- [**Generative Pretraining for Black-Box Optimization**](https://arxiv.org/abs/2206.10786) **_ICML_** 2022 [💻]() [📖]()
- [**Bootstrapped Training of Score-Conditioned Generator for Offline Design of Biological Sequences**](https://proceedings.neurips.cc/paper_files/paper/2023/hash/d601a9b708cacfad167f6c6c45647a18-Abstract-Conference.html) **_NeurIPS_** 2023 [💻]() [📖]()
- [**ExPT: Synthetic Pretraining for Few-Shot Experimental Design**](https://proceedings.neurips.cc/paper_files/paper/2023/hash/8fab4407e1fe9006b39180525c0d323c-Abstract-Conference.html) **_NeurIPS_** 2023 [💻]() [📖]()

#### Diffusion Models

- [**Diffusion Models for Black-Box Optimization**](https://arxiv.org/abs/2306.07180) **_ICML_** 2023 [💻]() [📖]()
- [**Exploring Chemical Space with Score-Based Out-of-Distribution Generation**](https://arxiv.org/abs/2206.07632) **_ICML_** 2023 [💻]() [📖]()
- [**Robust Guided Diffusion for Offline Black-Box Optimization**](https://arxiv.org/abs/2410.00983) **_TMLR_** 2024 [💻]() [📖]()
- [**Guided Trajectory Generation with Diffusion Models for Offline Model-Based Optimization**](https://proceedings.neurips.cc/paper_files/paper/2024/hash/98904db124b2a2463e8c59ec33fc7150-Abstract-Conference.html) **_NeurIPS_** 2024 [💻]() [📖]()
- [**Design Editing for Offline Model-Based Optimization**](https://arxiv.org/abs/2405.13964) **_Public Online_** 2024 [💻]() [📖]()
- [**Low To High-Value Designs: Offline Optimization via Generalized Diffusion**](https://openreview.net/forum?id=K9Elg2JrvY) **_Public Online_** 2025 [💻]() [📖]()

#### Flow Matching

- [**Dirichlet Flow Matching with Applications to DNA Sequence Design**](https://proceedings.mlr.press/v235/stark24b.html) **_ICML_** 2024 [💻]() [📖]()

- [**ParetoFlow: Guided Flows in Multi-Objective Optimization**](https://openreview.net/forum?id=mLyyB4le5u) **_ICLR_** 2025 [💻]() [📖]()
- [**Flow Q-Learning**](https://arxiv.org/abs/2502.02538) **_Public Online_** 2025 [💻]() [📖]()
- [**AffinityFlow: Guided Flows for Antibody Affinity Maturation**](https://arxiv.org/abs/2502.10365) **_Public Online_** 2025 [💻]() [📖]()

#### Energy-based Models

- [**Conservative Objective Models Are a Special Kind of Contrastive Divergence-Based Energy Model**](https://arxiv.org/abs/2304.03866) **_Public Online_** 2023 [💻]() [📖]()

- [**Protein Discovery with Discrete Walk-Jump Sampling**](https://openreview.net/forum?id=zMPHKOmQNb) **_ICLR_** 2024 [💻]() [📖]()
- [**Latent Energy-Based Odyssey: Black-Box Optimization via Expanded Exploration in the Energy-Based Latent Space**](https://arxiv.org/abs/2405.16730) **_Public Online_** 2024 [💻]() [📖]()

#### Control by Generative Flow Networks (GFlowNet)

- [**Biological Sequence Design with GFlowNets**](https://proceedings.mlr.press/v162/jain22a.html) (Moksh Jain et al., ICML 2022) [💻](https://github.com/MJ10/BioSeq-GFN-AL) [📖](https://github.com/mila-iqia/Awesome-Offline-Model-Based-Optimization/blob/main/bibtex/biosequence_gflownet.txt)
- [**Multi-Objective GFlowNets**](https://proceedings.mlr.press/v202/jain23a.html) **_ICML_** 2023 [💻]() [📖]()
- [**Generative Flow Networks Assisted Biological Sequence Editing**](https://openreview.net/forum?id=9BQ3l8OVru) **_NeurIPS GenBio_** 2023 [💻]() [📖]()
- [**Improved Off-Policy Reinforcement Learning in Biological Sequence Design**](https://arxiv.org/abs/2410.04461) **_NeurIPS AI for New Drug Modalities_** 2024 [💻]() [📖]()
- [**Learning to Scale Logits for Temperature-Conditional GFlowNets**](https://arxiv.org/abs/2310.02823) **_ICML_** 2024 [💻]() [📖]()
- [**Posterior Inference with Diffusion Models for High-Dimensional Black-box Optimization**](https://arxiv.org/abs/2502.16824) **_Public Online_** 2025 [💻]() [📖]()


## Star History
[![Star History Chart](https://api.star-history.com/svg?repos=mila-iqia/Awesome-Offline-Model-Based-Optimization&type=Date)](https://star-history.com/#mila-iqia/Awesome-Offline-Model-Based-Optimization&Date)



## 🤗 Contribution

### Contributors

[Ye Yuan](https://mila.quebec/en/directory/ye-yuan)

### Contributing to this project

Please feel free to file a PR for contributing to this project! Thanks so much for your help!

### Acknowledgement

TBD
