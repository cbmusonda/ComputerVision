# Semi-Supervised Learning Comparison for Medical Image Segmentation

## Using LA and ACDC Datasets (10% & 20% Labeled Data)

This repository contains a comprehensive evaluation of four state-of-the-art semi-supervised learning (SSL) methods applied to medical image segmentation.
We benchmarked each method on two widely used medical datasets—LA (Left Atrium MRI) and ACDC (Cardiac MRI)—under challenging 10% and 20% labeled training conditions.

All experiments were executed inside Google Colab, and each method’s official repository was either cloned or imported following the instructions below.

## ⭐Methods Evaluated

### 1. MC-Net+ (Mutual Consistency Learning)
**Paper:** “Mutual Consistency Learning for Semi-Supervised Medical Image Segmentation”  
**Link:** https://arxiv.org/pdf/2109.09960  
We implement MC-Net+, which uses a shared encoder and multiple decoders with a mutual consistency constraint to focus supervision on hard, uncertain regions and better exploit unlabeled data.

### 2. RCPS (Rectified Contrastive Pseudo Supervision)
**Paper:** “RCPS: Rectified Contrastive Pseudo Supervision for Semi-Supervised Medical Image Segmentation”  
**Link:** https://arxiv.org/pdf/2301.05500  
We use RCPS to combine rectified pseudo supervision (with uncertainty-aware correction) and voxel-level contrastive learning to improve class separability in the feature space.

> **Implementation note:**  
> The official RCPS code was provided as a ZIP archive rather than a public Git repo.  
> For this project, the **RCPS ZIP file was manually uploaded directly into the Google Colab environment** and extracted there for training.  
> A copy of that original archive is stored in this repository under:
> `external_code/RCPS_original.zip`.

### 3. S4CVNet (When CNN Meet with ViT)
**Paper:** “When CNN Meet with ViT: Towards Semi-Supervised Learning for Multi-Class Medical Image Semantic Segmentation”  
**Link:** https://arxiv.org/pdf/2208.06449  
S4CVNet is a semi-supervised framework that combines CNN and ViT in a dual-view feature-learning module with a ViT-based guidance module, using pseudo-label supervision and consistency constraints.

### 4. Cross-View Mutual Learning (CVML)
**Paper:** “Cross-View Mutual Learning for Semi-Supervised Medical Image Segmentation”  
**Link:** https://doi.org/10.1145/3664647.3680699  
CVML introduces a cross-view mutual learning scheme where multiple views/branches exchange pseudo-labels and consistency constraints to better leverage unlabeled data for segmentation.

## 📦Dataset Overview

### 🏥LA Dataset (Left Atrium)
- 3D MRI volumes
- Binary segmentation (left atrium vs background)
- We sample 2D slices and apply intensity normalization and cropping.

### ❤️ACDC Dataset
- Cine-MRI cardiac dataset with **4 segmentation classes**:
  1. Background  
  2. Right ventricle (RV) endocardium  
  3. Myocardium  
  4. Left ventricle (LV) endocardium  
- Patients are also grouped into 5 diagnosis categories (NOR, MINF, DCM, HCM, RV), but in this project we focus on the **4-class segmentation task**.

