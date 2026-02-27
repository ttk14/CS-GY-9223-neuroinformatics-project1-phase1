# CS-GY 9223 Neuroinformatics — Project 1, Phase 1

## 3D ResNet MRI Super-Resolution with 6-Fold Cross-Validation

This project trains a 3D residual convolutional network to enhance low-field (64mT) MRI volumes to approximate high-field (3T) quality.

### Approach
- **Model:** 3D ResNet with residual blocks operating on volumetric patches (64x64x32)
- **Training:** 6-fold cross-validation, 25 epochs per fold, L1 loss
- **Optimizer:** AdamW (lr=2e-4, weight_decay=1e-4)
- **Data:** 18 paired low-field / high-field MRI volumes

### Files
| File | Description |
|------|-------------|
| `resnet3d_mri_enhancement.ipynb` | Full training, validation, and submission pipeline |
| `extract_slices.py` | Helper functions for data loading and submission creation |
| `metric.py` | MS-SSIM evaluation metric |

### Large Files (Google Drive)
Model weights and dataset are too large for GitHub. Download from:

**[Google Drive — Phase 1](https://drive.google.com/drive/folders/15mE3FY_U85mlthVcbQIvYU8Dhh6UMCCq?usp=share_link)**

Contents:
- `dataset.zip` — Training and test MRI volumes
- `best_fold_1.pt` through `best_fold_6.pt` — Trained model weights for each fold

### How to Run
1. Clone this repo
2. Download files from Google Drive and place them in the repo root
3. Unzip `dataset.zip` (creates `train/` and `test/` folders)
4. Run `resnet3d_mri_enhancement.ipynb`

### Authors
- Nibish Tamrakar (nt2920@nyu.edu)
- Tarik Kassa (tk2766@nyu.edu)
