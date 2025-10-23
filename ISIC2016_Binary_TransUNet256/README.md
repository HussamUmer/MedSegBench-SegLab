# 🧠 ISIC 2016 — Skin Lesion Segmentation (256×256) with TransUNet 🔬

![Python](https://img.shields.io/badge/Python-3.8+-yellow)
![PyTorch](https://img.shields.io/badge/PyTorch-🧩-red)
![Colab Ready](https://img.shields.io/badge/Open%20in-Colab-orange)
![MedSegBench Ready](https://img.shields.io/badge/MedSegBench-Ready-purple)
![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)

---

## 🌟 Project Description

This project demonstrates **binary segmentation** on the **ISIC 2016 Skin Lesion Dataset (256×256)** using the **TransUNet** architecture as a sample model inside the **MedSegBench-SegLab** framework. 🧩  

It serves as a **reference project** — showing how every segmentation notebook in this repository operates from **dataset loading → model training → evaluation → visualization → calibration** under a single unified 13-step pipeline.  

Our goal is to provide a fully reproducible example so that researchers can easily plug in their own models into **Step 6️⃣ (Model Block)** and obtain standardized results, metrics, and visual reports effortlessly. 🚀  

---

## 🩺 Dataset Details

- **Dataset:** [ISIC 2016](https://challenge.isic-archive.com/data/#2016)  
- **Task:** Binary Segmentation *(Lesion vs. Non-Lesion)*  
- **Resolution:** 256×256  
- **Modality:** Dermoscopic Skin Images  
- **Splits:** Predefined (Train / Validation / Test)  
- **Format:** `.npz` archive standardized under MedSegBench  

This dataset is part of the **MedSegBench** benchmark collection — a unified suite of over **35 medical segmentation datasets** designed for consistent evaluation across modalities.

---

## 🧩 Visual Samples from Dataset

Here are a few visual examples showing **dermoscopic skin images and corresponding ground truth masks** from the ISIC 2016 dataset.  
Each sample contains the **original image**, **GT (Ground Truth) overlay**, and **GT boundary** for clear lesion localization visualization.  

<p align="center">
  <img src="https://github.com/HussamUmer/MedSegBench-SegLab/raw/main/ISIC2016_Binary_TransUNet256/outputs/image_1.png" width="48%" alt="ISIC2016 Sample 1"/>
  <br>
  <em>🖼️ Figure 1 — Input Image with GT Overlay & Boundary</em>
</p>

<p align="center">
  <img src="https://github.com/HussamUmer/MedSegBench-SegLab/raw/main/ISIC2016_Binary_TransUNet256/outputs/image_2.png" width="48%" alt="ISIC2016 Sample 2"/>
  <br>
  <em>🖼️ Figure 2 — Input Image with GT Overlay & Boundary</em>
</p>

🔗 [View All Sample Outputs →](https://github.com/HussamUmer/MedSegBench-SegLab/tree/main/ISIC2016_Binary_TransUNet256/outputs)  
*(These visuals are generated directly from the notebook — showing dataset-level consistency across MedSegBench pipelines.)*


---

## 🌐 Dataset Download — ISIC 2016 (256×256)

The **ISIC 2016 Skin Lesion Dataset** used in this notebook is part of the **MedSegBench v1** release hosted on **Zenodo**.  
Each dataset in MedSegBench comes as a preprocessed `.npz` archive with predefined splits (train/val/test), standardized resolutions, and verified MD5 checksums for full reproducibility.  

**Download Details:**
- **Dataset:** ISIC 2016 (256×256)
- **Direct Link:** [Download from Zenodo](https://zenodo.org/records/13358372/files/isic2016_256.npz?download=1)
- **MD5 Checksum:** `ee3fc6b5fffdc039e963ab21ff18e42e`
- **File Size:** ~121 MB
- **Format:** `isic2016_256.npz`
- **Zenodo Record:** [https://zenodo.org/records/13358372](https://zenodo.org/records/13358372)

✅ **Usage:**  
The notebook automatically downloads this dataset to your `MEDSEGBENCH_DIR` if it’s not already present and verifies its integrity using the MD5 checksum.  
If the checksum mismatches, the system re-downloads the file to ensure complete reproducibility.  



---

## ⚙️ Model Used — TransUNet 🧬

The notebook uses **TransUNet** as the sample model placed inside **Step 6 — MODEL BLOCK**, demonstrating how any architecture can seamlessly integrate into the MedSegBench-SegLab pipeline.

- **Model Type:** Vision Transformer (ViT) encoder + U-Net decoder  
- **Input Shape:** 3×256×256  
- **Output:** 1×256×256 binary mask  
- **Loss Functions:** Dice + BCE  
- **Metrics:** Dice, IoU, Precision, Recall  
- **Optimizer:** AdamW with Cosine LR scheduler  
- **Mixed Precision (AMP):** Enabled for faster training  

You can replace TransUNet with any segmentation architecture (U-Net, DeepLabV3+, SwinUNet, etc.) — the rest of the notebook remains unchanged!

---

## 📊 Experiment Outputs & Results

All training artifacts, logs, and figures were automatically saved during the notebook run.  
These include:
- 📈 Training & Validation Curves (Dice, IoU, Loss)
- 🩺 Qualitative Results (Input → GT → Prediction)
- ⚙️ Resource Metrics (Params, MACs, VRAM, Latency)
- 📁 Summary Reports (JSON/CSV)

You can explore all the results, plots, and checkpoint outputs here:

🔗 [📂 View Experiment Outputs on Google Drive](https://drive.google.com/drive/folders/1t40QUhLEmaqYYyyg8uuGAoXVgLP0b_n8?usp=sharing)

---

## 🧠 Purpose of This Project

This notebook acts as a **template and showcase** for all future segmentation projects within **MedSegBench-SegLab**.  
It represents how each dataset project will be structured — from reproducible setup to final evaluation — ensuring that every notebook remains consistent, transparent, and comparable.

By studying this project, contributors can easily understand:
- How to structure new dataset notebooks  
- Where to place models (Step 6)  
- How logs, plots, and results are automatically generated  

---

## ✨ Closing Note

> “Consistency creates comparability — and comparability creates progress.” 💫  

This ISIC 2016 example is the **front door** of MedSegBench-SegLab — showing how medical segmentation can be standardized, simplified, and shared.  

🧩 Feel free to explore, modify, and extend this notebook for your models.  
⭐ Star the main repository if you find it useful — and let’s keep open science reproducible! 🚀

