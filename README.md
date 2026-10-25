# Explainable Deep Learning for Multiclass Skin Lesion Classification

**Research Internship | Project ID: 1157**

## Overview

This study compares three ImageNet-pretrained CNN architectures—ResNet50, MobileNetV2, and EfficientNetB0—for seven-class skin lesion classification using the HAM10000 dataset. Grad-CAM is used for qualitative explainability analysis.

## Dataset

HAM10000 contains 10,015 dermoscopic images across seven classes: `akiec`, `bcc`, `bkl`, `df`, `mel`, `nv`, and `vasc`.

**Dataset:** https://www.kaggle.com/datasets/kmader/skin-cancer-mnist-ham10000

The dataset was partitioned at lesion level:

- Training: 7,002 images
- Validation: 1,519 images
- Testing: 1,494 images

## Model Performance

| Model | Test Accuracy | Macro F1-score | Melanoma Recall |
|---|---:|---:|---:|
| ResNet50 | 77.51% | 44.18% | 45.99% |
| MobileNetV2 | 74.10% | 42.30% | 26.20% |
| EfficientNetB0 | 71.95% | 27.79% | 18.18% |

## Explainability

Grad-CAM was applied to selected ResNet50 predictions to visualize image regions influencing the model's decisions. This analysis is qualitative and has not been clinically validated.

## Limitations

The dataset is class-imbalanced. Class weights were calculated but not used during model training. ResNet50 preprocessing was applied before geometric augmentation, which is a methodological limitation. Results are not clinically validated.

## How to Run

1. Download the HAM10000 dataset from the link above.
2. Open the research notebook(s) in Google Colab.
3. Update dataset and output paths to match your environment.
4. Install any missing dependencies and run the notebook cells in order.

## Disclaimer

This project is for academic research only and is not intended for clinical diagnosis.
