# Point-Based Crowd Counting

This project implements the research paper:
**"Rethinking Counting and Localization in Crowds: A Purely Point-Based Framework"**  
*Qingyu Song, Changan Wang, Zhengkai Jiang, Yabiao Wang, Ying Tai, Chengjie Wang, Jilin Li, Feiyue Huang, Yang Wu*

The goal of this repository is to replicate and extend the ideas presented in the paper, which proposes a purely point-based framework for crowd counting and individual localization.
Localizing individuals in a crowd is more aligned with real-world applications of high-level crowd analysis compared to just counting the total number of people. This repository focuses on implementing the *Point to Point Network (P2PNet)*, a novel approach that avoids intermediate representations like density maps or pseudo boxes, which can be error-prone. P2PNet directly predicts point proposals corresponding to heads in an image, consistent with human annotation.

Key contributions of the original paper include:

- A **density Normalized Average Precision (nAP)** metric for comprehensive performance evaluation.
- A **one-to-one matching mechanism** for optimal association of predictions using the Hungarian algorithm.
- **Significant improvements** over state-of-the-art methods on popular crowd counting benchmarks, both in counting accuracy and localization precision.

<img src="img/net.png" width="1000"/>   

---

## **Features**

- **Point-Based Counting:** A framework that directly predicts a set of point proposals representing individual heads in a crowd.
- **No Density Maps:** Avoids intermediate steps like density map generation, simplifying the process and reducing errors.
- **nAP Metric:** A novel metric for evaluating counting performance based on density normalization.
- **Hungarian Algorithm:** Utilized for one-to-one matching between predicted points and ground truth annotations.
