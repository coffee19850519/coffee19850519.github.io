---
title: "scPEFT: Parameter Efficient Fine-Tuning single-cell Large Language Models"
excerpt: "A framework that efficiently calibrates general scLLMs for out-of-context use cases <br/><img src='/images/scPEFT_thumbnail.jpg'>"
collection: portfolio
---
![scPEFT: Parameter Efficient Fine-Tuning single-cell Large Language Models](images/scPEFT.jpg)

Description
======
Recent advancements in single-cell Large Language Models (scLLMs) show promise in a variety of tasks within familiar cellular contexts and many scLLMs have been released. 
However, in out-of-context scenarios, such as unseen diseases, treatments, uncharacterized cell populations, or across species, scLLMs often perform unreliably, leading to misinterpretations.
Current strategies to address this challenge primarily focus on scaling up pretraining data and model parameters, which demand significant computational resources and extensive data collection, restricting accessibility for most users of scLLMs with limited resources. 
Here, we introduce scPEFT (single-cell Parameter-Efficient Fine-Tuning), a novel framework that efficiently calibrates general scLLMs for out-of-context use cases by integrating low-dimensional, learnable, and pluggable adapters. 
scPEFT democratizes scLLMs, making them accessible to a broader research community, including those with limited resources. 
It enables context-specific single-cell analyses without requiring prohibitively expensive computational power while maintaining generalizable performance and interpretable insights. 
Additionally, by analyzing its attention mechanism, scPEFT facilitates disease-specific biomarker detection for particular cell types and states, enhancing the clinical applications of scLLMs. 
This novel utility paradigm can also be extended to other biological and biomedical foundation models. 

GitHub link
======
https://github.com/coffee19850519/scPEFT

Related Publications
======
Harnessing the Power of Single-Cell Large Language Models with Parameter Efficient Fine-Tuning using scPEFT
Fei He, Ruixin Fei, Jordan E. Krull, Xinyu Zhang, Mingyue Gao, Li Su, Yibo Chen, Yang Yu, Jinpu Li, Baichuan Jin, Yuzhou Chang, Anjun Ma, Qin Ma, Dong Xu
bioRxiv 2025.04.21.649754; doi: https://doi.org/10.1101/2025.04.21.649754
