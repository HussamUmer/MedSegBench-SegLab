# ⚙️ RoboTool — Endoscopic Surgical Tool Segmentation (256×256) with TransUNet

This project applies the MedSegBench-SegLab framework to the **RoboTool Endoscopy Dataset** for **binary segmentation of surgical instruments** in endoscopic video frames.

## 🩺 Dataset Details
- **Dataset:** RoboTool (256×256)
- **Task:** Binary Segmentation *(Tool vs. Background)*
- **Modality:** Endoscopic Surgery
- **Download Link:** [Download from Zenodo](https://zenodo.org/records/13358372/files/robotool_256.npz?download=1)
- **MD5 Checksum:** `7e644bc28160db7e4af27b164844f136`

✅ The notebook follows the standard 13-step MedSegBench-SegLab pipeline — only the dataset, modality, and MD5 checksum have been updated for the RoboTool dataset.

## 🚀 Open Notebook in Colab

To directly explore and run this project on Google Colab, click below 👇  

<p align="center">
  <a href="https://colab.research.google.com/github/HussamUmer/MedSegBench-SegLab/blob/main/RoboTool_Binary_TransUNet256/notebook/RoboTool_Binary_TransUNet256.ipynb" target="_blank">
    <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open in Colab"/>
  </a>
</p>

*(Runs end-to-end — just update **Step 6 (MODEL BLOCK)** with your model 💡)*
