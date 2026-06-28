# Diabetic Retinopathy Detection using MobileNet

A lightweight deep learning model for automated multi-class detection of Diabetic Retinopathy (DR) from retinal fundus images, optimized for deployment on smartphones without internet dependency.

---

## Overview

Diabetic Retinopathy is a leading cause of blindness worldwide. This project implements a MobileNet-based CNN classifier that detects and grades DR severity 
from retinal fundus images into five classes.

**Key features:**
- Lightweight MobileNet architecture using depthwise separable convolutions
- Designed to run locally on smartphones without internet dependency
- Multi-class severity classification across 5 DR grades

---

## Pipeline

The training pipeline follows these steps:
1. Retinal fundus images loaded from directory structure, filepaths and labels extracted into a DataFrame
2. Sample images displayed per severity class
3. Dataset split using `train_test_split`
4. Images fed through Keras `ImageDataGenerator` with augmentation and rescaling
5. CNN model trained on the 5-class DR severity labels
6. Model evaluated using accuracy metrics and confusion matrix
7. Severity level predicted and mapped to DR class label

---

## Dataset

**Diabetic Retinopathy 224x224 (Gaussian Filtered)**  
Source: [Kaggle](https://www.kaggle.com/datasets/sovitrath/diabetic-retinopathy-224x224-gaussian-filtered) 

| Class | Severity Level |
|-------|---------------|
| 0 | No DR |
| 1 | Mild |
| 2 | Moderate |
| 3 | Severe |
| 4 | Proliferative DR |

Images are Gaussian filtered and resized to 224×224 pixels.

---

## Model

- **Architecture:** MobileNet (depthwise separable convolutions)
- **Task:** Multi-class classification (5 severity levels)
- **Optimized for:** Edge deployment / smartphone inference

---
