# 🔬 Kvasir — Endoscopy Polyp Segmentation (256×256) with TransUNet

This project adapts the MedSegBench-SegLab pipeline for the **Kvasir Endoscopy Dataset**, performing **binary polyp segmentation** using the **TransUNet** architecture.

## 🩺 Dataset Details
- **Dataset:** Kvasir (256×256)
- **Task:** Binary Segmentation *(Polyp vs. Background)*
- **Modality:** Endoscopy (Gastrointestinal)
- **Download Link:** [Download from Zenodo](https://zenodo.org/records/13358372/files/kvasir_256.npz?download=1)
- **MD5 Checksum:** `4ce7118decc9973a252e9a9dd6c1e47e`

✅ The notebook follows the same standardized 13-step MedSegBench pipeline as previous projects, with only the dataset and MD5 checksum updated for the **Kvasir** dataset.

## 🚀 Open Notebook in Colab

To directly explore and run this project on Google Colab, click below 👇  

<p align="center">
  <a href="https://colab.research.google.com/github/HussamUmer/MedSegBench-SegLab/blob/main/Kvasir_Binary_TransUNet256/notebook/Kvasir_Binary_TransUNet256.ipynb" target="_blank">
    <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open in Colab"/>
  </a>
</p>

*(Runs end-to-end — just update **Step 6 (MODEL BLOCK)** with your model 💡)*
