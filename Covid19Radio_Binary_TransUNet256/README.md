# 🫁 Covid19RadioMSBench — Chest X-Ray Lung Segmentation (256×256) with TransUNet

This project applies the MedSegBench-SegLab pipeline to the **Covid19RadioMSBench** dataset for **binary lung segmentation** on chest X-ray images.

## 🩺 Dataset Details
- **Dataset:** Covid19RadioMSBench (256×256)
- **Task:** Binary Segmentation *(Lung vs. Background)*
- **Download Link:** [Download from Zenodo](https://zenodo.org/records/13358372/files/covid19radio_256.npz?download=1)
- **MD5 Checksum:** `f1b1de2f1a22d163f553d9b554c742ec`

✅ The only change from previous notebooks is the dataset (Covid19RadioMSBench) and its corresponding resolution and MD5 checksum; all other 13 steps in the pipeline remain identical.

## 🚀 Open Notebook in Colab

To directly explore and run this project on Google Colab, click below 👇  

<p align="center">
  <a href="https://colab.research.google.com/github/HussamUmer/MedSegBench-SegLab/blob/main/Covid19Radio_Binary_TransUNet256/note book/Covid19Radio_Binary_TransUNet256.ipynb" target="_blank">
    <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open in Colab"/>
  </a>
</p>

*(Runs end-to-end — just update **Step 6 (MODEL BLOCK)** with your model 💡)*
