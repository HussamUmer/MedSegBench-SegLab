# 🧬 Promise12 — Prostate MRI Segmentation (256×256) with TransUNet

This project adapts the MedSegBench-SegLab pipeline for the **Promise12 Prostate MRI Dataset**, performing **binary segmentation** of the prostate gland using the **TransUNet** model.

## 🩺 Dataset Details
- **Dataset:** Promise12 (256×256)
- **Task:** Binary Segmentation *(Prostate vs. Background)*
- **Modality:** MRI
- **Download Link:** [Download from Zenodo](https://zenodo.org/records/13358372/files/promise12_256.npz?download=1)
- **MD5 Checksum:** `f5dbdbfe05b80808c4d541a63f64521c`

✅ This notebook follows the standard 13-step MedSegBench-SegLab pipeline, with the dataset, modality, and MD5 checksum updated specifically for the **Promise12 (Prostate MRI)** dataset.

## 🚀 Open Notebook in Colab

To directly explore and run this project on Google Colab, click below 👇  

<p align="center">
  <a href="https://colab.research.google.com/github/HussamUmer/MedSegBench-SegLab/blob/main/Promise12_Binary_TransUNet256/notebook/Promise12_Binary_TransUNet256.ipynb" target="_blank">
    <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open in Colab"/>
  </a>
</p>

*(Runs end-to-end — just update **Step 6 (MODEL BLOCK)** with your model 💡)*
