# 🧪 Visual Anomaly Detection for Packaging Lines

This project implements a patch-based visual anomaly detection system using the MVTec AD Carpet dataset. It uses a ResNet50 feature extractor and unsupervised memory bank approach to identify surface defects in carpet samples, commonly seen in packaging lines of FMCG manufacturing.

---

## 📌 Project Overview

- **Dataset**: MVTec AD (Carpet subset)
- **Approach**: Memory-based anomaly detection using patch-wise feature comparison
- **Model**: ResNet50 feature extractor (torchvision pretrained)
- **Goal**: Identify defective vs. non-defective carpet images using unsupervised learning

---

## 🚀 How It Works

1. **Mounts Google Drive** and reads dataset folders
2. **Builds a ResNet50-based feature extractor** (hooked layers)
3. **Creates a memory bank** from 10% of `train/good` images
4. **Calculates anomaly scores** for each test image based on distance to memory bank
5. **Finds optimal threshold** using F1-score
6. **Evaluates performance** with Accuracy, AUC-ROC, IoU, Dice
7. **Generates heatmaps** for visual inspection
8. **Exports results** to Excel and PDF

---

## 📁 Files Included

| File                                | Description                                         |
|-------------------------------------|-----------------------------------------------------|
| `Carpet_Anomaly_Detection.ipynb`    | Main Colab notebook (end-to-end pipeline)           |
| `carpet_anomaly_full_results.xlsx`  | Per-image predictions and anomaly scores            |
| `carpet_heatmap_report.pdf`         | Visual anomaly heatmaps with IoU & Dice scores      |

---

## 📊 Model Performance

| Metric        | Value     |
|---------------|-----------|
| Accuracy      | 95.58%    |
| AUC-ROC       | 0.97      |
| Mean IoU      | > 0.85    |
| Mean Dice     | > 0.90    |

---

## 🔧 Tech Stack

- Python (Google Colab)
- PyTorch & torchvision
- scikit-learn
- matplotlib, seaborn
- pandas, openpyxl
- PIL, skimage

---

## 📂 Dataset Used

- [MVTec Anomaly Detection – Carpet Class](https://www.mvtec.com/company/research/datasets/mvtec-ad)

---

## 🧠 Author

**Jinal Ahir**  
Intel AI for Manufacturing Certificate Program

---

## 📎 Report Files

- 📊 [Excel Results](carpet_anomaly_full_results.xlsx)
- 📄 [Heatmap PDF Report](carpet_heatmap_report.pdf)
