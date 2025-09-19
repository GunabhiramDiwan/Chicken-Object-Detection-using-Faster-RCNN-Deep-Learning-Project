# 🐔 Chicken Object Detection Using Faster R-CNN

This repository contains the implementation of **Chicken Object Detection** using **Faster Region-Based Convolutional Neural Networks (Faster R-CNN)** with different backbone architectures (**ResNet-50, ResNet-101, ResNeXt-101**). The project demonstrates a practical approach to automating chicken counting and monitoring in poultry farms, reducing manual labor and improving efficiency.

---

## 📌 Overview
- Automates **chicken detection and counting** in images and videos.
- Uses **Faster R-CNN with Detectron2** for real-time object detection.
- Evaluates three backbones: **ResNet-50, ResNet-101, and ResNeXt-101**.
- Achieves **97.25% mAP@0.5 (ResNet-50)**, proving its suitability for **real-time monitoring**.
- Supports data augmentation for robustness under different conditions.

---

## 📂 Dataset
- **Source**: Hayriyigit Kaggle Chicken Object Detection dataset.  
- **Original Images**: 376  
- **Augmented Images**: 605 → expanded to 752 using **Albumentations** (contrast adjustment, flipping, rotation).  
- **Annotations**: Created using **LabelImg (XML)** and converted into **COCO format** for Detectron2 compatibility.  
- **Split**: Train (80%), Test (20%).  

---

## 🛠️ Tech Stack
- **Frameworks**: PyTorch, Detectron2  
- **Deep Learning Models**: Faster R-CNN (ResNet-50, ResNet-101, ResNeXt-101)  
- **Annotation Tool**: LabelImg  
- **Data Augmentation**: Albumentations  
- **Formats**: VOC XML → COCO JSON  

---

## 📊 Results

| Backbone     | mAP@0.5 | mAP@0.75 | Model Size | Training Time |
|--------------|---------|----------|------------|---------------|
| ResNet-50    | **97.25%** | 62.07%   | 314 MB     | 24 min        |
| ResNet-101   | 96.08%   | 62.65%   | 460 MB     | 34 min        |
| ResNeXt-101  | 96.26%   | 61.79%   | 796 MB     | 85 min        |

✅ **ResNet-50** achieved the best trade-off between accuracy and computational efficiency, making it the most suitable for **real-time poultry monitoring**.

---

## 🚀 How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/GunabhiramDiwan/Chicken-Object-Detection.git
   cd Chicken-Object-Detection
