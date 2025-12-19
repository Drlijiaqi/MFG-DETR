# MFG-DETR: Real-time Safety Helmet Detection via a Multi-scale Feature-Gated Fusion Framework

[![PyTorch](https://img.shields.io/badge/PyTorch-v2.2.2-red.svg)](https://pytorch.org/)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)

This repository contains the official implementation of **MFG-DETR**, a lightweight and real-time object detection framework tailored for intelligent safety helmet monitoring in complex construction environments.

## 🚀 Abstract

Ensuring workers' compliance with safety helmet regulations is critical for occupational safety. However, existing methods often struggle with small-object recognition, environmental complexity, and deployment constraints on edge devices. 

To address these challenges, we propose **MFG-DETR**. Built upon the RT-DETR architecture, MFG-DETR integrates three novel modules:

1.  **Multi-scale Lightweight Edge Detector (MLE):** Combines adaptive pooling and frequency-based edge enhancement to improve small-object localization.
2.  **Synergistic Dual-Stage Attention Fusion (SDSA-Fusion):** Employes global-local attention and content-guided pixel-level gating to enhance feature fusion under occlusion.
3.  **Synergistic Gated Residual gConvC3 (SGR-gConvC3):** Incorporates gated convolution and learnable residual scaling to selectively suppress noise while enhancing semantic representations.

## 🏆 Performance

Extensive experiments on **GDUT-HWD + AIGC-HWD**, **SHWD**, and **SHEL5K** datasets demonstrate that MFG-DETR achieves state-of-the-art accuracy with minimal computational overhead.

**Comparison on GDUT+AIGC Dataset:**

| Model | mAP@0.5 (%) | mAP@0.75 (%) | Params (MB) | FLOPs (G) | FPS |
| :--- | :---: | :---: | :---: | :---: | :---: |
| YOLOv8-l | 87.69 | 74.80 | 43.61 | 164.80 | 97.81 |
| RT-DETR-r18 | 86.57 | 73.75 | 19.87 | 57.00 | 298.91 |
| RT-DETR-r50 | 87.96 | 75.70 | 41.96 | 129.60 | 153.07 |
| **MFG-DETR (Ours)** | **90.67** | **76.81** | **14.87** | **51.20** | **312.34** |

> **Highlights:**
> * **High Accuracy:** 90.67% mAP@0.5.
> * **Lightweight:** Only 14.87 MB parameters (approx. 25% reduction compared to RT-DETR-r18).
> * **Real-time:** >300 FPS on RTX 4090.

## 📂 Code Download

**The full code will be released after the paper is accepted.**

We are currently finalizing the code organization. Once the paper is accepted, we will upload the following:
* Complete source code for MFG-DETR.
* Training and inference scripts.

## 🛠️ Environment

[cite_start]The model was developed and tested under the following environment:

* **OS:** Windows 11
* **Python:** 3.10.16
* **PyTorch:** 2.2.2
* **CUDA:** 12.1
* **GPU:** NVIDIA GeForce RTX 4090 (24GB)
* **CPU:** Intel Core i9-13900k

## 📝 Citation

If you find this work helpful for your research, please consider citing:

```bibtex
@article{mfg_detr_2025,
  title={MFG-DETR: Real-time Safety Helmet Detection via a Multi-scale Feature-Gated Fusion Framework},
  author={Hao Zhang; Jiaqi Li; Zhaobo Li; Lingjie Kong; Xuefeng Zhao},
  journal={Automation in Construction},
  year={2025}
}
