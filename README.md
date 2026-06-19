# CNN-Based Automated Surface Crack Detection for Tata Steel

## Project Overview

This project uses a Convolutional Neural Network (CNN) to automatically detect surface cracks in steel plates during manufacturing.

The objective is to replace slow and error-prone manual inspection with an AI-powered quality inspection system capable of real-time crack detection.

## Dataset

- 40,000 steel surface images
- 20,000 Crack images
- 20,000 Smooth images
- Balanced dataset

### Data Split

- Training: 32,000 images
- Testing: 8,000 images

## Model Architecture

Input: 128 × 128 × 3 RGB

CNN Architecture:

- Conv2D(32) + ReLU + BatchNorm + MaxPooling
- Conv2D(64) + ReLU + BatchNorm + MaxPooling
- Flatten
- Dense(128) + ReLU
- Dropout(0.6)
- Dense(1, Sigmoid)

## Data Augmentation

- Rotation
- Zoom
- Brightness variation
- Shear transformation
- Horizontal and vertical flips
- Width and height shifts

## Training Configuration

- Optimizer: Adam
- Loss Function: Binary Cross Entropy
- Epochs: 20
- Batch Size: 32
- EarlyStopping
- ModelCheckpoint

## Performance

- Training Accuracy: 98%
- Validation Accuracy: 94%
- ROC-AUC ≈ 1.00

## Explainable AI (XAI)

Grad-CAM was used to visualize the regions responsible for crack detection, improving model transparency and trustworthiness.

## Deployment Features

- Real-time crack detection
- Streamlit dashboard
- Image upload support
- Live camera support
- Grad-CAM visualization

## Technologies Used

- Python
- TensorFlow
- Keras
- OpenCV
- NumPy
- Matplotlib
- Streamlit

## Authors

- Sarthak Sharma
- Shalin Sawhney
- Vaibhav Sharma
- Aastha Gupta
- Harnoor