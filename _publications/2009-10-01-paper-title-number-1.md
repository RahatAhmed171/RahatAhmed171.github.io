---
title: "A Lightweight Hybrid Deep Learning Framework for Image-Based Air Quality Index Classification"
collection: publications
category: conferences
permalink: /publication/2009-10-01-paper-title-number-1
excerpt: 'A study of image-based air quality index classification using computer vision and deep learning.'
 
paperurl: '/files/drafts/AQI_classification_paper_draft( math added, formatted).pdf'
---
 ** Problem it solves**
Traditional AQI monitoring relies on sensor stations that are expensive and spatially limited. Existing image-based deep learning alternatives are either computationally heavy or require extra multimodal sensor hardware, making them impractical for real-time edge/mobile deployment.

** Contribution**
The paper proposes a lightweight hybrid architecture (PatchCSPNet) that classifies AQI into six severity categories using only ground-level sky images, achieving high accuracy without sensor fusion or heavy backbones, while remaining efficient enough for edge deployment.

** Methods used**
A frozen pre-trained ResNet50 extracts features, reduced via 1×1 convolution and bilinear upsampled, then split into a 4×4 spatial patch grid. Each patch is processed by a shared Cross Stage Partial Block (CSPBlock), followed by Global Average Pooling, dropout, and a linear classification head trained with Cross-Entropy loss and Adam optimizer.

** Results**
Evaluated on 12,240 images (6 classes), the model achieved 96.73% accuracy, a macro F1-score of 0.9666, and 4.400 ms inference latency per image — outperforming VGG16/19, InceptionV3, and the ResNet50 baseline in accuracy while staying competitive in speed, with Moderate/Good classes showing the most confusion.

[Draft of the paper]({{ page.paperurl }})
