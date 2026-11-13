# CityCare Hospital — ResNet-18 CIFAR-10 Baseline

## Overview

This project implements a baseline image classification model using transfer learning with ResNet-18 and the CIFAR-10 dataset.

The purpose of this task is to establish a working deep-learning environment and baseline model before moving to the later stages of the CityCare Hospital Camouflaged Object Detection project.

## Project Structure

```text
citycare-cod-baseline/
├── models/
│   └── resnet18_cifar10.pth
├── notebooks/
│   └── task1_resnet18_cifar10.ipynb
├── outputs/
│   └── confusion_matrix.png
└── README.md
```

## Technologies

- Python
- PyTorch
- Torchvision
- Google Colab
- CUDA / GPU
- Matplotlib
- Scikit-learn
- CIFAR-10

## Model

The project uses a pretrained **ResNet-18** model with transfer learning.

The original final classification layer was replaced with a new layer containing **10 output classes** for CIFAR-10.

The model was trained using:

- Loss: Cross-Entropy Loss
- Optimizer: Adam
- Learning rate: 0.001
- Epochs: 5
- Batch size: 64
- Hardware: NVIDIA Tesla T4 GPU

## Dataset

The **CIFAR-10** dataset contains 10 image classes:

1. Airplane
2. Automobile
3. Bird
4. Cat
5. Deer
6. Dog
7. Frog
8. Horse
9. Ship
10. Truck

The training split contains 50,000 images and the test split contains 10,000 images.

## Results

After 5 epochs of training:

| Metric | Result |
|---|---:|
| Final Training Accuracy | 95.79% |
| Final Test Accuracy | 89.89% |

The required test accuracy for Task 1 was at least **70%**, and the achieved test accuracy was **89.89%**.

## Confusion Matrix

The generated 10×10 confusion matrix is available here:

`outputs/confusion_matrix.png`

## Notebook

The complete training and evaluation workflow is available in:

`notebooks/task1_resnet18_cifar10.ipynb`

The notebook includes:

- Environment/GPU verification
- CIFAR-10 data loading
- ResNet-18 transfer learning
- Model training
- Accuracy evaluation
- Confusion matrix generation

## Trained Weights

The trained ResNet-18 weights are available at:

`models/resnet18_cifar10.pth`

## How to Run

Open the notebook in Google Colab and enable a GPU runtime.

Then run the notebook cells from top to bottom.

The notebook automatically downloads the CIFAR-10 dataset and uses the configured PyTorch/torchvision environment.

## Task 1 Outcome

Task 1 successfully established the baseline training pipeline using CIFAR-10 and ResNet-18 transfer learning. The model achieved **89.89% test accuracy**, exceeding the required 70% threshold.