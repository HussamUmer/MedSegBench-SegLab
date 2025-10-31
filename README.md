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

> ⚙️ **Note:**  
> I’ve run **each dataset notebook for 1 epoch** 🧪 — just to confirm that all components (dataset paths, file structures, augmentations, and DataLoaders) work correctly and the pipelines execute without errors.  
> The only exception is the **Covid19Radio project**, which I haven’t executed yet but am confident will work flawlessly given its identical structure.  
>  
> This limited run was purely for **functional validation** and not full model training. You can perform full training yourself directly in **Google Colab** or **Jupyter Notebook** by simply running all cells end-to-end.  
>  

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
- **[BUSI — Breast Ultrasound Lesion Segmentation (256×256) with TransUNet 🩺](https://github.com/HussamUmer/MedSegBench-SegLab/tree/main/BUSI_Binary_TransUNet256)**  
  <sub>Folder: `BUSI_Binary_TransUNet256`</sub>

> (Binary segmentation notebooks coming soon... stay tuned 🧩)

---

# 🩺 Multi-Class Segmentation Projects

Multi-class segmentation deals with **organ-level** or **region-level** predictions, where multiple anatomical structures are labeled simultaneously.  
The same 13-step framework extends naturally to multi-class datasets with per-class metrics, confusion matrices, and class-wise calibration.

> (Coming soon in v2 release — support for AbdomenUSMSBench, Polyp, and OrganSeg datasets 🧬)

---

## 🧠 Step-6 Plug-and-Play Segmentation Models  

This folder contains ready-to-use **model blocks** for **Step 6 — MODEL BLOCK** of the Seg-Lab pipeline 🧩.  
Each notebook is a *plug-and-play* segment that can be inserted directly into any dataset notebook (ISIC, Kvasir, BUSI …).  

> ⚠️ **Important:** These model notebooks **will not run independently**.  
> They depend on the Seg-Lab pipeline (Steps 0–5 & 7–13).  
> Always **copy the cells into Step 6** of a dataset notebook before execution.

---

### 🔧 Standard Copy-Paste Flow (for all models)

Each model has **4 cells** that you must copy in order:

1️⃣ **Cell 1/4 — Imports & Wrapper**  
   - Copy imports and the `SMPWrap` (or equivalent).  
   - Ensures `forward(x) → {"logits": (B, C, H, W)}` for pipeline compatibility.  

2️⃣ **Cell 2/4 — Builder Function**  
   - Copy the `build_*()` definition.  
   - Confirm:  
     - `in_channels = 3`  
     - `classes = C` (→ `1` for binary, `>1` for multiclass)  
     - `activation = None` (loss handles activation).  

3️⃣ **Cell 3/4 — Instantiate & Shape Check**  
   - Paste the model-creation snippet, e.g.:  
     ```python
     model = build_unet_r34_binary()
     xb, yb = next(iter(train_loader))
     out = model(xb)
     print("logits:", tuple(out["logits"].shape))
     ```  
   - (Optional) set a tag for checkpoints/logs:  
     ```python
     MODEL_TAG = "UNet-R34"
     ```  

4️⃣ **Cell 4/4 — Parameter Count (Optional)**  
   - Paste the parameter summary:  
     ```python
     num_params = sum(p.numel() for p in model.parameters() if p.requires_grad)
     print(f"[PARAMS] {MODEL_TAG}: {num_params/1e6:.2f} M")
     ```  

> ✅ Once inserted, no edits are needed — the pipeline automatically manages training, metrics, visualization, calibration, and speed/VRAM benchmarking.

---

## 📚 Available Models

### 1️⃣ TransUNet (Default)
Already included in every dataset notebook as the **default baseline**.  
*No copy required — use as is.*

---

### 2️⃣ U-Net (R34 Encoder)
<a href="https://colab.research.google.com/github/HussamUmer/MedSegBench-SegLab/blob/main/Segmentation%20Models/U_Net.ipynb" target="_blank">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open U-Net in Colab"/>
</a>  
- Copy **Cells 1/4 – 4/4** into Step 6 of your dataset notebook.

---

### 3️⃣ U-Net++ (Dense Skip Connections)
<a href="https://colab.research.google.com/github/HussamUmer/MedSegBench-SegLab/blob/main/Segmentation%20Models/U_Net_PlusPlus.ipynb" target="_blank">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open U-Net++ in Colab"/>
</a>  
- Copy **Cells 1/4 – 4/4** into Step 6 of your dataset notebook.

---

### 4️⃣ DeepLabV3+ (ResNet-50 Backbone)
<a href="https://colab.research.google.com/github/HussamUmer/MedSegBench-SegLab/blob/main/Segmentation%20Models/DeepLabV3%2B.ipynb" target="_blank">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open DeepLabV3+ in Colab"/>
</a>  
- Copy **Cells 1/4 – 4/4** into Step 6 of your dataset notebook.

---

### ✅ Before Running
- [ ] Correct `C` value (Binary → 1; Multiclass → #classes).  
- [ ] `forward(x)` returns `{"logits": B × C × H × W}`.  
- [ ] `IMAGE_SIZE` matches dataset (128 / 256 / 512).  
- [ ] `AMP_ON` (mixed precision) can remain True.  

> 🔧 More Step-6 plug-and-play models are coming soon! If you want a specific architecture, open a PR or request it — I’ll add it to the collection ✨


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
