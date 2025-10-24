# 🧬 Chromosome Identification using Computer Vision

This repository contains a complete pipeline for **automatic chromosome identification/karyotyping** using Classical Computer Vision + Deep Learning. The goal is to classify and arrange human chromosomes (1–22 + X, Y) from metaphase spreads.

---

## 🧠 Problem Overview

Karyotyping is the process of analyzing chromosomes to detect:

* Trisomies (e.g., Down Syndrome – Trisomy 21)
* Monosomies / deletions
* Structural abnormalities (translocation, inversion, duplication)

Traditionally done **manually** by cytogenetic experts → slow + error-prone.
This project automates the identification step using Computer Vision.

---

## 🔬 Pipeline

```
Microscope Image → Preprocessing → Segmentation → Cropping Individual Chromosomes →
Feature Extraction → Classification (DL) → Output Karyotype
```

---

## 📂 Folder Structure

```
chromosome-cv/
│
├── data/
│   ├── raw/
│   ├── processed/
│   └── annotations/
│
├── src/
│   ├── preprocessing.py        # noise removal, contrast, CLAHE
│   ├── segmentation.py         # threshold/mask R-CNN/UNet
│   ├── cropping.py             # bounding box extraction
│   ├── feature_extraction.py   # shapes, centromere index, CNN features
│   ├── classification.py       # EfficientNet / ResNet
│   └── evaluation.py
│
├── notebooks/
│   ├── 01_data_visualization.ipynb
│   ├── 02_segmentation_training.ipynb
│   └── 03_chromosome_classifier.ipynb
│
└── models/
    ├── segmentation_model.h5
    └── classifier_model.h5
```

---

## 🛠️ Technologies Used

| Step           | Method                                |
| -------------- | ------------------------------------- |
| Preprocessing  | OpenCV (CLAHE, adaptive thresholding) |
| Segmentation   | UNet / Mask-RCNN                      |
| Classification | EfficientNet / ResNet                 |
| Deployment     | ONNX / Flask                          |

---

## ✅ Features

✔️ Fully automated segmentation of chromosomes
✔️ Deep learning-based chromosome classification (1–22, X, Y)
✔️ Optionally includes centromere position estimation
✔️ Easily extensible to abnormality detection

---

## 📊 Dataset

You can use:

* **ICS Karyotyping Dataset**
* **Bioimage Chromosome Dataset**
* **Allen Institute datasets**

(Links can be added later)

---

## 👩‍🔬 Use Cases

| Application        | Field                 |
| ------------------ | --------------------- |
| Prenatal Diagnosis | Medical Genetics      |
| Research           | Cytogenetics          |
| Labs/Automation    | AI-assisted pathology |
| Teaching/Training  | Bioinformatics & ML   |

---

## 🚀 Getting Started

```bash
pip install opencv-python numpy torch torchvision matplotlib
```

---

## 🧩 Future Improvements

* Detect structural abnormalities (translocation, inversion)
* Multi-instance segmentation improvements
* Real-time microscope integration

---
