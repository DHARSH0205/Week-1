# Waste Classification using CNN

## 🎯 Problem Statement

The growing problem of improper waste management stems from inadequate collection, segregation, and recycling systems. This leads to environmental pollution, health hazards, and inefficient resource utilization. Manual waste segregation is labor-intensive, time-consuming, and often inaccurate.

To address this, the project aims to develop a **Convolutional Neural Network (CNN)** based image classification system capable of automatically categorizing solid waste into four major types — **Plastic, Paper, Metal, and Organic**.

This **AI-powered solution** supports sustainable waste management practices by enabling faster and more accurate segregation for recycling and disposal.

---

## 📊 Dataset Overview

**Source:** [Kaggle - Waste Classification Dataset by Adithya Challa](https://www.kaggle.com/datasets/adithyachalla/waste-classification)

**Total Images:** ~4,000  
**Image Format:** JPG(RGB)  
**Structure:** Each folder represents a unique waste class.

---

### 🗂 Selected Categories for This Project

| Category | Folder Name | Description |
|----------------|-----------------|--------------|
| **Plastic** | `1-Plastic` | Plastic bottles, containers, bags, and packaging |
| **Paper** | `2-Paper` | Newspapers, sheets, books, and paper items |
| **Metal** | `3-Metal` | Aluminum cans, foils, and metal scraps |
| **Organic** | `4-Food Organics` | Food waste, fruits, and vegetables |

---

### 🖼️ Image Usage

Images are directly used from the Kaggle dataset **without modification** to maintain authenticity and ensure reliable CNN training.

---

📘 *This project contributes to advancing automated waste segregation and supports environmental sustainability through intelligent waste management.*

## Model Architecture
- **Base Model:** MobileNetV2 (pretrained on ImageNet)  
- **Input Shape:** 224×224×3  
- **Top Layers Added:**
  - GlobalAveragePooling2D
  - Dense layer(s) for classification
- **Optimizer:** Adam  
- **Loss Function:** Sparse Categorical Crossentropy  
- **Metrics:** Accuracy  

**Notes:** Using a pretrained base model helps achieve high accuracy with limited data by leveraging **transfer learning**.

---

## Training
- **Platform:** Kaggle Notebook with GPU  
- **Batch Size:** 32  
- **Validation Split:** 20%  
- **Data Preprocessing:** Images resized to 224×224 and normalized  
- **GPU Optimization:** Datasets cached and prefetched  

**Training Results:**
- Training Accuracy: 0.927  
- Validation Accuracy: ~0.92  

---

