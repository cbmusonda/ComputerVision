# Semi-Supervised Learning Comparison for Medical Image Segmentation

## Using LA and ACDC Datasets (10% & 20% Labeled Data)

This repository contains a comprehensive evaluation of four state-of-the-art semi-supervised learning (SSL) methods applied to medical image segmentation.
We benchmarked each method on two widely used medical datasets—LA (Left Atrium MRI) and ACDC (Cardiac MRI)—under challenging 10% and 20% labeled training conditions.

All experiments were executed inside Google Colab, and each method’s official repository was either cloned or imported following the instructions below.

## ⭐Methods Evaluated
1. FixMatch
   - Paper: https://arxiv.org/pdf/2109.09960
   - Consistency regularization + confidence thresholding.
2. Meta Pseudo-Labels (MPL)
   - Paper: https://arxiv.org/pdf/2109.09960
   - Learning teacher predictions using meta-gradients.
3. ST++ (Student–Teacher Plus-Plus)
   - Paper: https://arxiv.org/pdf/2208.06449
   - Progressive student-teacher refinement across training stages.
4. RCPS (Rectified Contrastive Pseudo Supervision)
   - Paper: https://arxiv.org/pdf/2301.05500
   - Contrastive pseudo-labeling with rectification to improve SSL robustness.

## 📦Dataset Overview
### 🏥 LA Dataset (Left Atrium)
- 3D MRI volumes
- Binary segmentation task
- Requires 2D slice extraction + intensity normalization
  
### ❤️ ACDC Dataset
- 3-class segmentation: LV cavity, RV cavity, myocardium
- End-diastole and end-systole phases
- Different preprocessing pipeline from LA dataset.
  
Both datasets were adapted so each SSL method could train consistently across both domains.
   
