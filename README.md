# 🚀 MedSegBench-SegLab — Plug-and-Play Binary & Multi-Class 🧠🩺 Segmentation 
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
![Python](https://img.shields.io/badge/Python-3.8+-yellow)
![PyTorch](https://img.shields.io/badge/PyTorch-🧩-red)
![Reproducible](https://img.shields.io/badge/Reproducible-Seeds%20%26%20Splits-green)
![Colab Ready](https://img.shields.io/badge/Open%20in-Colab-orange)
![MedSegBench Ready](https://img.shields.io/badge/MedSegBench-Ready-purple)

---

## 🌟 Why This Repo?

Medical image segmentation research often struggles with **non-reproducible experiments** — different splits, preprocessing, and logging styles make fair comparison impossible.  
**MedSegBench-SegLab** solves this by providing a **unified, reproducible, and Colab-friendly lab** 🧠 where every dataset follows an identical **13-step benchmark pipeline**, letting researchers simply plug in their models and compare fairly.

You focus on your model 🧩 — we handle the rest.

> 💡 While conducting my research on developing a **TransUNet-Lite**, I originally built this notebook to **train and evaluate my own models**.  
It has since been tested on **three architectures** — one standard **TransUNet** and **two novel lightweight variants** that I designed during my experiments.


---

## 📦 What’s Inside

This repository includes complete **segmentation benchmark notebooks** built over the **MedSegBench datasets** (35+ datasets, 60,000+ medical images 🏥), covering both:

- 🩸 **Binary Segmentation** — single foreground class (e.g., tumor vs. non-tumor)
- 🩺 **Multi-Class Segmentation** — multiple organs, lesions, or tissue regions *(coming soon...)*

Each notebook is **Colab-ready**, self-contained, and follows the exact same structure for **fair apples-to-apples model comparison** 🍎🍏.

---

> > ⚙️ **Note:**  
> For each dataset notebook, I’m currently running up to **Step 5️⃣** — mainly to update dataset paths, verify file structures, and ensure that all **DataLoaders** function correctly.  
> Full end-to-end runs (training → evaluation → visualization) will be completed later or integrated into the **Vision4Healthcare** repository.  
>  
> This phase focuses purely on the **dataset preparation and validation** 🧩, while new and optimized models for **Step 6 — MODEL BLOCK** 🧠 will be introduced in a dedicated upcoming repository.

---

## 🧩 What Does Each Notebook Include?

Each notebook follows a **13-step universal pipeline**:

1. **Environment & Libraries** — Import and setup GPU, print versions  
2. **Dataset Download** — Fetch MedSegBench NPZ and verify MD5  
3. **Config & Reproducibility** — Fixed seed, configs, and environment dump  
4. **Predefined Splits** — Load dataset splits (no re-splitting)  
5. **Preprocessing & Augmentations** — Normalize and augment  
6. **🧠 MODEL BLOCK** — ✨ *Your playground!* Paste your custom model here  
7. **Losses & Metrics** — Dice, IoU, BCE, CrossEntropy  
8. **Training & Logging** — AdamW, CosineLR, mixed precision, CSV logs  
9. **Plotly Curves** — Interactive training/validation curves  
10. **Test Evaluation** — Frozen checkpoint, compute metrics  
11. **Inference Speed Test** — Measure latency & VRAM  
12. **Threshold & Calibration** — PR/ROC, AUPRC, AUROC, ECE  
13. **Qualitative Visuals** — Image overlays, boundaries, grid outputs  

Everything—training logs, checkpoints, figures, summaries—is saved automatically.  
Just modify Step 6 and re-run the notebook end-to-end!

---

## ⚙️ How to Run

1. Open any notebook in **Google Colab** or **Jupyter**.  
2. Set your `MEDSEGBENCH_DIR` (where datasets are cached).  
3. Go to **Step 6 — MODEL BLOCK** and paste your model (e.g., U-Net, TransUNet, SwinUNet).  
4. Run all cells — that’s it! 🚀  

Each notebook runs completely standalone.  
For demonstration, we’ve used **TransUNet 🧬** as an example model.

---

## 🧠 Dataset Overview

**MedSegBench** is a large-scale collection of **35+ medical image segmentation datasets** standardized for fair benchmarking.  
It includes over **60,000+ images** from modalities like:

- 🩺 **Dermoscopic (ISIC 2016/2018)**
- 🫁 **CT / MRI (Brain, Liver, Heart)**
- 🩻 **X-ray & Ultrasound (Chest, Abdomen, Musculoskeletal)**  

Each dataset is provided in `.npz` format with **predefined splits**, **unified resolution (128/256/512)**, and **MD5 verification** for reproducibility.

---

# 🩸 Binary Segmentation Projects

Binary segmentation focuses on separating **foreground (e.g., lesion/tumor)** from **background**, perfect for lightweight and diagnostic models.  
Each notebook here follows the 13-step standard pipeline and only changes **dataset name** and **Step 6 model**.

You can plug in **your custom architecture**, evaluate it under **identical conditions**, and visualize results with live **Plotly curves**, **Dice/IoU comparisons**, and **qualitative overlays**.  
All metrics, speed, and calibration plots are generated automatically — so benchmarking becomes effortless! ⚡

---

## 📘 Projects

- **[ISIC 2016 — Skin Lesion Segmentation (256×256) with TransUNet 🔬](https://github.com/HussamUmer/MedSegBench-SegLab/blob/main/ISIC2016_Binary_TransUNet256/README.md)**  
  <sub>Folder: `ISIC2016_Binary_TransUNet256`</sub>
- **[ISIC 2016 — Skin Lesion Segmentation (512×512) with TransUNet 🔬](https://github.com/HussamUmer/MedSegBench-SegLab/blob/main/ISIC2016_Binary_TransUNet512/README.md)**  
  <sub>Folder: `ISIC2016_Binary_TransUNet512`</sub>
- **[Covid19RadioMSBench — Chest X-Ray Lung Segmentation (256×256) with TransUNet 🫁](https://github.com/HussamUmer/MedSegBench-SegLab/tree/main/Covid19Radio_Binary_TransUNet256)**  
  <sub>Folder: `Covid19Radio_Binary_TransUNet256`</sub>
- **[Kvasir — Endoscopy Polyp Segmentation (256×256) with TransUNet 🔬](https://github.com/HussamUmer/MedSegBench-SegLab/tree/main/Kvasir_Binary_TransUNet256)**  
  <sub>Folder: `Kvasir_Binary_TransUNet256`</sub>
- **[RoboTool — Endoscopic Surgical Tool Segmentation (256×256) with TransUNet ⚙️](https://github.com/HussamUmer/MedSegBench-SegLab/tree/main/RoboTool_Binary_TransUNet256)**  
  <sub>Folder: `RoboTool_Binary_TransUNet256`</sub>
- **[Promise12 — Prostate MRI Segmentation (256×256) with TransUNet 🧬](https://github.com/HussamUmer/MedSegBench-SegLab/tree/main/Promise12_Binary_TransUNet256)**  
  <sub>Folder: `Promise12_Binary_TransUNet256`</sub>


> (Binary segmentation notebooks coming soon... stay tuned 🧩)

---

# 🩺 Multi-Class Segmentation Projects

Multi-class segmentation deals with **organ-level** or **region-level** predictions, where multiple anatomical structures are labeled simultaneously.  
The same 13-step framework extends naturally to multi-class datasets with per-class metrics, confusion matrices, and class-wise calibration.

> (Coming soon in v2 release — support for AbdomenUSMSBench, Polyp, and OrganSeg datasets 🧬)

---

## 🧾 Citation

If you use this repository or MedSegBench datasets, please cite:

> **MedSegBench: A Comprehensive Benchmark for Medical Image Segmentation Across Modalities**  
> *Zenodo DOI: [10.5281/zenodo.12662149](https://zenodo.org/records/12662149)*

---

## 💡 Final Words

✨ This project is **open for Colab**, **open for collaboration**, and **open for discovery**.  
🌍 Star ⭐ the repo, fork it, and bring your segmentation model to life with fair benchmarking!  

> “One pipeline, many datasets — infinite innovation.” 💫  
— *Team Vision4Healthcare*
