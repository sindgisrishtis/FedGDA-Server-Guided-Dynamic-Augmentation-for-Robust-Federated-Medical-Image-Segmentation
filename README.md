# FedGIN-Multimodal-Segmentation
Federated Learning Framework using Dynamic Global Non-linear Augmentation for Multi-modal Organ Segmentation

# FedGIN Multi-modal Organ Segmentation

## 📌 Project Overview
This project focuses on **multi-organ segmentation using Federated Learning concepts**, inspired by the FedGIN framework.

The goal is to handle **data heterogeneity across medical datasets** and improve generalization using advanced augmentation strategies.

---

## 🎯 Current Progress (Completed)

### ✅ 1. Dataset Selection
- Dataset: **TotalSegmentator (Small Subset)**
- ~102 CT scans
- Real-world clinical data

---

### ✅ 2. Organ Selection
We selected **5 important abdominal organs**:

- Liver  
- Spleen  
- Pancreas  
- Kidneys (Left + Right combined)  
- Gallbladder  

---

### ✅ 3. Preprocessing Pipeline

Steps performed:

1. Loaded CT scans (`.nii.gz`)
2. Extracted selected organ masks
3. Combined left & right kidneys
4. Normalized CT images
5. Saved processed data as:
*_ct.npy
*_mask.npy

---

### ✅ 4. 3D → 2D Slicing

To enable efficient training:

- Converted 3D volumes into 2D slices
- Removed empty slices (no organs)
- Final dataset contains **~21,000+ slices**

---

### 📂 Final Data Format

Each sample:

- **CT slice:** `(H, W)`
- **Mask:** `(5, H, W)`

---

### 📊 Example

- CT Shape: `(207, 207)`
- Mask Shape: `(5, 207, 207)`
- Mask Values: `{0, 1}`

---
