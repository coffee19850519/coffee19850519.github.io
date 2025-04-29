---
title: "scPEFT: Parameter Efficient Fine-Tuning single-cell Large Language Models"
excerpt: "A framework that efficiently calibrates general scLLMs for out-of-context use cases <br/><img src='/images/scPEFT.jpg'>"
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

![scPEFT: Parameter Efficient Fine-Tuning single-cell Large Language Models](/images/scPEFT.jpg)


Computational demands reduction for adaptation of scLLMs
======
By constraining domain adaptation to a separate lower dimensional subspace, scPEFT reduces parameter tuning by at least 96% and lowers Graphics Processing Unit (GPU) memory costs by more than 50%, making scLLMs significantly accessible for research groups operating on limited resources.

![Efficiency Analysis of scPEFT](/images/scPEFT_efficiency.jpg)

Mitigating catastrophic forgetting
======
scPEFT re-parameterizes original scLLM model parameters with low-dimensional proxies, fundamentally differing from traditional fine-tuning. The plug-in adapters enable efficient customization of scLLMs without overwriting the original scLLM model parameters, reducing the risk of overfitting to noisy or biased task-specific data while mitigating catastrophic forgetting of pre-learned knowledge. This approach improves performance by 5-15% across diverse out-of-context scenarios, including disease-specific datasets, cross-species comparisons, and under-characterized cell groups
![Mitigating catastrophic forgetting by scPEFT](/images/scPEFT_catastrophic.jpg)

Biomarker insights
======
scPEFT provides unique insights for biomedical research by ensuring that the model's attention scores align closely with pre-learned general gene activities and condition-specific requirements. This delivers COVID-infection-specific cell-state-associated genes and distinguishing phenotypical subpopulations from CD34+ enriched and bone marrow samples that other tools fail to discern. 
![Biomarker insights provided by scPEFT](/images/scPEFT_biomarker.jpg)

Cross-species Transfer
======
scPEFT enables the effective transfer of scLLMs, initially trained on human data, to other animal species beyond their pretrained corpus. This approach bridges the species divide by capturing a shared embedding subspace between pre-trained human data and various animal species, facilitating integrated analyses across diverse organisms. 
![cross-species transfer by scPEFT](/images/scPEFT_cross_species.jpg)

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