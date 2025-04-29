---
title: "pathCLIP: Detection of genes and gene relations from biological pathway figures through image-text contrastive learning"
excerpt: "A pathway figure curation system for identifying genes and gene relations from pathway figures. <br/><img src='/images/pathCLIP_overview.pdf'>"
collection: portfolio
---

Motivation
======
Recent advancements in single-cell Large Language Models (scLLMs) show promise in a variety of tasks within familiar cellular contexts and many scLLMs have been released. 
However, in out-of-context scenarios, such as unseen diseases, treatments, uncharacterized cell populations, or across species, scLLMs often perform unreliably, leading to misinterpretations.
Current strategies to address this challenge primarily focus on scaling up pretraining data and model parameters, which demand significant computational resources and extensive data collection, restricting accessibility for most users of scLLMs with limited resources. 
Here, we introduce scPEFT (single-cell Parameter-Efficient Fine-Tuning), a novel framework that efficiently calibrates general scLLMs for out-of-context use cases by integrating low-dimensional, learnable, and pluggable adapters. 
scPEFT democratizes scLLMs, making them accessible to a broader research community, including those with limited resources. 
It enables context-specific single-cell analyses without requiring prohibitively expensive computational power while maintaining generalizable performance and interpretable insights. 
Additionally, by analyzing its attention mechanism, scPEFT facilitates disease-specific biomarker detection for particular cell types and states, enhancing the clinical applications of scLLMs. 
This novel utility paradigm can also be extended to other biological and biomedical foundation models. 

![pathCLIP overview](/images/pathCLIP_overview.pdf)


Computational demands reduction for adaptation of scLLMs
======


Mitigating catastrophic forgetting
======


Biomarker insights
======


Cross-species Transfer
======


Uncharacterized cell population detection
======


GitHub link
======
[https://github.com/coffee19850519/scPEFT](https://github.com/coffee19850519/scPEFT)

Related Publications
======
1. Harnessing the Power of Single-Cell Large Language Models with Parameter Efficient Fine-Tuning using scPEFT
Fei He, Ruixin Fei, Jordan E. Krull, Xinyu Zhang, Mingyue Gao, Li Su, Yibo Chen, Yang Yu, Jinpu Li, Baichuan Jin, Yuzhou Chang, Anjun Ma, Qin Ma, Dong Xu
bioRxiv 2025.04.21.649754; [Full text](https://www.biorxiv.org/content/10.1101/2025.04.21.649754v1.full.pdf)

2. Parameter-Efficient Fine-Tuning Enhances Adaptation of Single Cell Large Language Model for Cell Type Identification
Fei He, Ruixin Fei, Mingyue Gao, Li Su, Xinyu Zhang, Dong Xu
bioRxiv 2024.01.27.577455; [Full text](https://www.biorxiv.org/content/10.1101/2024.01.27.577455v1.full.pdf)

Collaborators
======
* Jordan E. Krull, Yuzhou Chang, Anjun Ma, Qin Ma @ [BMBL](https://u.osu.edu/bmbl/lab-members/current-people/)
* Others from [DBL](https://digbio.missouri.edu/our-team/)