---
title: "BengaliAddressNet: A Weighted Soft-Voting
 Ensemble for Bengali Handwritten Upazila–District
 Pair Name Recognition"
collection: publications
category: conferences
 
excerpt: 'BengaliAddressNet: A Weighted Soft-Voting
  Ensemble for Bengali Handwritten Upazila–District
  Pair Name Recognition.'
 
paperurl: '/files/thesis_in_paper (1).pdf'
---
 ** Problem it solves**

Prior Bengali handwriting recognition focuses on single characters or words, leaving **multi-word administrative fields unexplored** due to a lack of datasets. Handwritten address pairs in Bangladesh pose severe challenges due to cursive script complexities, varying writing styles, and **high visual similarities across locations**. Manual processing of postal mail and official forms creates a major bottleneck for administrative document digitization. This paper solves these challenges by enabling **automated end-to-end recognition of combined upazila-district name pairs**.

### Contributions Made
The study introduces **BNHW-UDPNR**, a novel dataset of **9,808 handwritten upazila-district pair images** covering all **496 administrative locations** in Bangladesh. It presents an **unsupervised text segmentation pipeline** combining MSER and Canny edge detection, removing the need for manual text bounding-box annotations. Additionally, it proposes **BengaliAddressNet**, a novel deep learning ensemble framework designed specifically for complex multi-word address recognition. Finally, it establishes empirical benchmarks evaluating the impact of dual-branch architectures, GELU activation functions, and data balancing strategies.

### Methods Used
The segmentation pipeline detects text regions via **MSER and Canny edge algorithms**, using Connected Component Analysis and column splitting to crop target lines. The proposed **BengaliAddressNet** uses a dual-branch architecture pairing a **Vision Transformer (ViT-Base)** for global context with a **ConvNeXt-Tiny** network for local feature extraction. Both branches feed feature vectors into a custom multi-layer perceptron head equipped with **GELU activations**. Final predictions are produced through a **weighted soft-voting ensemble strategy** ($w=0.18$ for ViT, $0.82$ for ConvNeXt) combining pre-softmax logits from both backbones.

### Results
The proposed **BengaliAddressNet** ensemble achieved a peak **test accuracy of 94.65%**, outperforming individual ViT-Base (91.12%) and ConvNeXt-Tiny (94.17%) models. The model attained a **macro-F1 score of 0.94** and a **ROC-AUC of 99.99%** across all 496 administrative classes. Experiments demonstrated that GELU activations outperformed standard ReLU, while **data augmentations boosted ensemble accuracy by +3.44%**. The unsupervised segmentation pipeline successfully extracted **90% of text line images automatically** without manual adjustments.

[Draft of the paper]({{ page.paperurl }})
