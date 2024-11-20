# 3D Semantic Segmentation of Brain Metastases

## Overview
This repository contains a project focused on **3D semantic segmentation of brain metastases** using the BraTS 2024 and NYUMets datasets. The goal is to segment tumor regions from multi-modal MRI scans (T1, T1 contrast-enhanced, T2, FLAIR), aiding in the detection and diagnosis of brain metastases. The project leverages advanced deep learning techniques, including **3D U-Net**, **Attention U-Net**, and **3D ResUNet** models, alongside custom loss functions to optimize performance.

## Datasets Used
- **BraTS 2024 Metastasis Dataset**: Multi-modal MRI images (T1, T1c, T2, FLAIR) along with segmentation masks that mark tumor regions.
- **NYUMets Dataset**: Similar MRI images and corresponding tumor masks, used to supplement training data.

## Installation

### Prerequisites
- Python 3.x
- TensorFlow/Keras
- Numpy
- Nibabel
- Tifffile
- Matplotlib (optional for visualizations)

### Install Dependencies
Clone the repository and install the required dependencies:
## Models
This project utilizes three different models for segmentation:
1. **3D U-Net**: Standard architecture for medical image segmentation, adapted for 3D volumetric data.
2. **Attention U-Net**: U-Net enhanced with attention mechanisms to focus on relevant regions for improved segmentation performance.
3. **3D ResUNet**: A variant of 3D U-Net that includes residual connections to help improve gradient flow and model performance.

## Methodology
- **Preprocessing**:
  - **Normalization**: Standardized image intensity values.
  - **Cropping & Resizing**: Ensured consistent input dimensions.
  - **Random Slice Selection**: Data augmentation to prevent overfitting.
  - **One-Hot Encoding**: For segmentation masks to represent each class distinctly.

- **Loss Functions**:
  - **Weighted Dice Loss**: Addresses class imbalances.
  - **Categorical Focal Loss**: Focuses on difficult-to-classify regions.

- **Metrics**:
  - **Accuracy**: Measures the percentage of correctly predicted voxels.
  - **IoU (Intersection over Union)**: Evaluates the overlap between predicted and actual tumor regions.


