---
title: "TrustAI Lab - Projects"
layout: textlay
excerpt: "projects"
sitemap: false
permalink: /projects
---

My research mission is to build **Trustworthy AI for Scientific Discovery**, empowering domain scientists with explainable intelligence they can use and trust. My work is organized around a virtuous cycle of developing novel **Methods**, grounding them in rigorous **Theory**, validating them with robust **Evaluations**, and driving discovery through real-world **Applications**.

---
## 1. Methods: From Optimization to Learning
We design novel explanation architectures that are not only accurate but also practical for real-world deployment. Our key innovation is shifting from slow, per-instance optimization to fast, generalizable learning-based approaches.

* **PGExplainer**: The first generative explainer for graph neural networks, offering a 100x speedup over previous methods by training a global explanation model once and deploying it for many instances.
    * [[NeurIPS 20 Paper]](https://arxiv.org/abs/2011.04573) [[900+ Citations]](https://scholar.google.com/scholar?cites=11306913385781387258) [[PyG Integration]](https://pytorch-geometric.readthedocs.io/en/latest/generated/torch_geometric.explain.algorithm.PGExplainer.html)

* **Proxy Graphs**: A solution to the critical Out-of-Distribution (OOD) problem, where explanations create inputs the model has never seen. By evaluating on in-distribution "proxy graphs", we generate more reliable and robust explanations.
    * **MixupExplainer**: A non-parametric approach for proxy construction. [[SIGKDD 23 Paper]](https://arxiv.org/abs/2307.07832)
    * **ProxyExplainer**: A learnable, parametric model for generating optimal proxies. [[ICML 24 Paper]](https://arxiv.org/abs/2402.02036)

---
## 2. Theory: From Model Artifacts to Scientific Truth
We build the theoretical foundations required to trust AI explanations as a source of genuine scientific insight, moving beyond explanations that are mere artifacts of a specific model architecture.

* **Information-Theoretic Foundation for XAI**: We formally define a "good" explanation using the principles of **sufficiency** (it contains all critical information) and **minimality** (it contains no redundant information). Our core theorem proves that a **highly accurate model's explanation is a bridge to the ground-truth scientific mechanism**. This provides the first formal justification for using benchmark datasets to evaluate XAI methods.
    * [[ICLR 24 Paper]](https://openreview.net/pdf?id=up6hr4hIQH)

---
## 3. Evaluations: Creating Metrics We Can Trust
When ground truth is unavailable, we need evaluation metrics that are reliable. We've identified critical flaws in existing fidelity metrics due to OOD issues and have developed new, robust alternatives.

* **Robust Fidelity (for Graphs)**: A new class of fidelity measures resilient to the distribution shifts that plague traditional metrics. It correctly identifies superior explanations where previous metrics fail, especially against adversarial attacks.
    * [[Project Page]](https://trustai4s-lab.github.io/fidelity.html) [[ICLR 24 Paper]](https://openreview.net/pdf?id=up6hr4hIQH) [[Code]](https://github.com/AslanDing/Fidelity)

* **F-Fidelity (for Time Series, Images, NLP)**: A robust and highly efficient framework that solves the flaws in the standard ROAR evaluation protocol. By fine-tuning a model once on random masks, we can fairly and robustly evaluate any number of explainers without costly retraining or information leakage.
    * [[Project Page]](https://trustai4s-lab.github.io/ffidelity.html) [[ICLR 25 Paper]](https://openreview.net/pdf?id=X0r4BN50Dv) [[Code]](https://github.com/AslanDing/Finetune-Fidelity)

---
## 4. Applications: Driving Scientific Discovery
We apply our trustworthy AI framework to help domain scientists solve critical challenges across various scientific frontiers.

* **Environmental Science**: Identifying critical historical patterns in climate data to explain and predict events like compound flooding.
    * **TimeX++**: [[ICML 24 Paper]](https://arxiv.org/abs/2405.09308)
    * [[Climate Tech @ FIU Project]](https://climate-tech.cs.fiu.edu/research/)

* **Bioinformatics**: Pinpointing the crucial 3D motifs and their spatial arrangements that determine a molecule's function, providing chemically plausible explanations.
    * **3DGraphX**: [[SIGKDD 25 Paper]](https://trustai4s-lab.github.io/)

* **Neuroscience**: Uncovering how dynamic changes in brain connectivity patterns over time can predict cognitive behaviors.
    * **DyExplainer**: [[TKDD 25 Paper]](https://trustai4s-lab.github.io/)
