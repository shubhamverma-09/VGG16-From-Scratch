# VGG16 From Scratch on CIFAR-10

## Overview

This project implements the VGG16 Convolutional Neural Network architecture from scratch using TensorFlow/Keras and trains it on the CIFAR-10 dataset.
The model is enhanced with Batch Normalization layers to improve training stability, accelerate convergence, and achieve better performance.
The objective of this project is to understand the internal architecture of VGG16, implement it manually without using pretrained weights, and evaluate its performance on a real-world image classification dataset.

---

## Dataset

Dataset: CIFAR-10

CIFAR-10 contains 60,000 RGB images belonging to 10 classes:

- Airplane
- Automobile
- Bird
- Cat
- Deer
- Dog
- Frog
- Horse
- Ship
- Truck

Dataset Split:

- Training Images: 50,000
- Test Images: 10,000
- Image Size: 32 × 32 × 3

---

## VGG16 Architecture

VGG16 consists of:

### Block 1
- Conv3×3 (64)
- Conv3×3 (64)
- MaxPooling

### Block 2
- Conv3×3 (128)
- Conv3×3 (128)
- MaxPooling

### Block 3
- Conv3×3 (256)
- Conv3×3 (256)
- Conv3×3 (256)
- MaxPooling

### Block 4
- Conv3×3 (512)
- Conv3×3 (512)
- Conv3×3 (512)
- MaxPooling

### Block 5
- Conv3×3 (512)
- Conv3×3 (512)
- Conv3×3 (512)
- MaxPooling

### Fully Connected Layers
- Dense(4096)
- Dense(4096)
- Dense(10)

---

## Project Structure

```text
VGG16-From-Scratch/
│
├── vgg16_experiment.ipynb
|
├── accuracy_curve.png
|
├── loss_curve.png
|
├── README.md

```

---

## Data Preprocessing

The following preprocessing steps were applied:

- Pixel normalization (0–255 → 0–1)
- One-hot encoding of labels
- Data augmentation:
  - Random Horizontal Flip
  - Random Rotation
  - Random Zoom

---

## Training Configuration

| Parameter | Value |
|------------|--------|
| Optimizer | Adam |
| Loss Function | Categorical Crossentropy |
| Batch Size | 128 |
| Epochs | 40 |
| Learning Rate | 0.001 |

---

## Results

| Metric | Value |
|----------|----------|
| Training Accuracy |94.36 % |
| Validation Accuracy | 88.87% |
| Test Accuracy | 88.97% |

### Training Accuracy Curve

<img width="566" height="372" alt="Training - Validation Accuracy Graph" src="https://github.com/user-attachments/assets/3a203d1d-063d-421f-8685-4b31b4afc0dd" />


### Training Loss Curve

<img width="567" height="371" alt="Training - Validation Loss Graph" src="https://github.com/user-attachments/assets/67d9f31d-cc40-4dd8-805f-692b6053e991" />


## Technologies Used

- Python
- TensorFlow
- Keras
- NumPy
- Matplotlib
- Scikit-learn

---

## Key Learnings

Through this project I gained hands-on experience with:

- CNN Architecture Design
- VGG16 Implementation
- Image Classification
- Data Augmentation
- Model Evaluation
- Hyperparameter Tuning
- Deep Learning Workflow

---

## Future Improvements

- Train on CIFAR-100
- Compare with ResNet and DenseNet
- Apply Transfer Learning
- Experiment with Vision Transformers

---

## Author

Shubham Verma

B.Tech Computer Science and Engineering

University College of Engineering and Technology, Bikaner

LinkedIn:
https://www.linkedin.com/in/shubham-verma-6277422b3

---
