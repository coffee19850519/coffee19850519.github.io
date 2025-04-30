---
title: "pathCLIP: Detection of genes and gene relations from biological pathway figures through image-text contrastive learning"
excerpt: "A pathway figure curation system for identifying genes and gene relations from pathway figures. <br/><img src='/images/pathCLIP_overview.jpg'>"
collection: portfolio
---

Motivation
======

In biomedical literature, biological pathways are commonly described through a combination of images and text. These pathways contain valuable information, including genes and their relationships, which provide insight into biological mechanisms and precision medicine. Curating pathway information across the literature enables the integration of this information to build a comprehensive knowledge base. While some studies have extracted pathway information from images and text independently, they often overlook the correspondence between the two modalities. Here, we present a pathway figure curation system named pathCLIP for identifying genes and gene relations from pathway figures. Our key innovation is the use of an image-text contrastive learning model to learn coordinated embeddings of image snippets and text descriptions of genes and gene relations, thereby improving curation. 

![Overview of proposed pipeline](/images/pathCLIP_overview.jpg)

This figure presents an overview of our pipeline, consisting of three key modules. On the left, the image module extracts visual embeddings from pathway figures. On the right, the text module generates text embeddings from the article text. In the middle, our image-text contrastive learning module (pathCLIP) is shown, which facilitates gene entity recognition and relation extraction tasks.


Pathway Figure Identifier
======

![Technical details of pathCLIP. ](/images/pathCLIP_image_processing.jpg)

Technical details of pathCLIP. (a) Pathway identifier. It illustrates the figure retrieval steps and the architecture of the pathway identifier. The input image, extracted from the literature, is passed through the pathway identifier, comprising ResNet and a classification network. The output indicates whether the image belongs to the pathway or non-pathway category. (b) Pathway object detection. It illustrates the image data preprocessing steps and the architecture of the object detection model. The pathway image is input into the object detection model, which identifies text boxes, arrows, and T-bars. These elements are then organized into image data acceptable for CLIP.

![results of pathCLIP pathway identifier. ](/images/pathCLIP_gene_relation_text.jpg)
(a) Performance of the pathway identifier, measured in terms of MCC, specificity, and sensitivity. (b) Performance metrics for arrow and T-Bar detection. (c) Performance metrics for gene-interaction recognition detection. (d) Embedding distribution of BioBERT-NER model on gene entity detection texts. (d) Embedding distribution of BioBERT pretrained model on entity detection texts. (f) Embedding distribution of BioBERT-RE model on gene relation extraction texts. (g) Embedding distribution of BioBERT pretrained model on gene relation extraction texts.

Fine-Tuned BioBERT Leverage on Tasks of NER and RE
======

![Text BioBERT fine-Tuning details](/images/pathCLIP_text_processing.jpg)

Text BioBERT fine-Tuning details. (a) Structure of text data used for gene entity detection and relation extraction tasks, highlighting key information related to genes and relations. (b) The process of pre-training and fine-tuning the BioBERT models. These models are employed to extract text features from sentences describing genes and relations, respectively.


Contrastive Learning Training on Pathway Figures and Their Text Descriptions
======
![Training and inference processes of pathCLIP.](/images/pathCLIP_text_image_training.jpg)

Training and inference processes of pathCLIP. (a) pathCLIP for gene entity detection and its integration with CLIP. (b) pathCLIP for relation extraction and its integration with CLIP for relation extraction.


Gene Recognition By pathCLIP
======

![pathCLIP results for entity detection](/images/pathCLIP_gene_text_image.jpg)

pathCLIP results for entity detection. (a) Embedding distribution of ResNet50 on entity detection images. (b) Embedding distribution of pathCLIP-ResNet50 on entity detection images. (c) Embedding distributions of pathCLIP on entity detection images and text. (d) Confusion matrix for entity detection by pathCLIP. (e) ROC curve of pathCLIP on entity detection, including five gene types as examples.

Relation Extraction By pathCLIP
======
![pathCLIP results for relation extraction](/images/pathCLIP_gene_relation_text_image.jpg)

pathCLIP results for relation extraction. (a) Embedding distribution of ResNet50 on relation extraction images. (b) Embedding distribution of pathCLIP-ResNet50 on relation extraction images. (c) Embedding distributions of pathCLIP on relation extraction images and text. (h) Confusion matrix for relation extraction by pathCLIP. (e) ROC curve, including pathCLIP, original ResNet, and fine-tuned ResNet.

GitHub link
======
[https://github.com/yangyang-69/pathCLIP](https://github.com/yangyang-69/pathCLIP)

Related Publication
======
**F. He** et al., "pathCLIP: Detection of Genes and Gene Relations From Biological Pathway Figures Through Image-Text Contrastive Learning," in *IEEE Journal of Biomedical and Health Informatics*, vol. 28, no. 8, pp. 5007-5019; [Full text](https://www.biorxiv.org/content/10.1101/2023.10.31.564859v1.full.pdf)


Collaborators
======
* Yibo Chen, Richard D. Hammer, Mihail Popescu @ [MISL](https://medicine.missouri.edu/centers-institutes-labs/medical-intelligent-systems-lab)
* Others from [DBL](https://digbio.missouri.edu/our-team/)