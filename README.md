# Liver Tumor Segmentation using U-Net

## 📌 Overview
This project implements a deep learning–based approach for **binary liver tumor segmentation** from CT scans using the **U-Net architecture**.  
The goal is to automatically identify tumor regions at the pixel level, assisting medical image analysis and research.

---

## 🧠 Problem Type
- Image Segmentation
- Binary Segmentation (Tumor vs Background)

---

## 📊 Dataset
- **Dataset:** LiTS (Liver Tumor Segmentation Challenge)
- **Modality:** CT scans
- **Format:** NIfTI (.nii)

### Data Structure:
- `train_CT/` → CT scan volumes
- `train_mask/` → Ground truth masks
- `test_CT/` → Test CT scans
- `test_mask/` → Test masks

Mask labels:
- `0` → Background
- `1` → Liver
- `2` → Tumor  
➡️ Converted to **binary mask**:
- `1` → Tumor
- `0` → Non-tumor

---

## ⚙️ Preprocessing
- Slice extraction (middle slice of each volume)
- Image resizing to **128×128**
- Normalization to range [0, 1]
- Binary mask conversion

---

## 🏗️ Model Architecture
- U-Net–like CNN
- Encoder–Decoder structure
- Skip connections for spatial detail preservation
- Sigmoid activation for binary segmentation

---

## 📐 Loss & Metric
- **Loss Function:** Dice Loss  
- **Evaluation Metric:** Dice Coefficient

---

## 🚀 Training Details
- Optimizer: Adam
- Batch size: 4
- Image size: 128×128
- Epochs: 10

---

## 📈 Results
- **Test Dice Score:** **70.2%**

The model demonstrates effective localization of liver tumor regions in CT images.

---

## 🖼️ Sample Output
The model predicts tumor masks that closely match the ground truth annotations.

---

## 💾 Model Saving
The trained model is saved as:
