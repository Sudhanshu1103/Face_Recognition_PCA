# Face Recognition using PCA with AT&T Dataset

## Description

This project implements a **face recognition system** using Principal Component Analysis (PCA) combined with Support Vector Machines (SVM) classification. The system is trained and tested on the AT&T (ORL) face database, which contains grayscale images of 40 individuals with 10 images per person.

## Key Features

- **PCA Implementation**: Two methods for dimensionality reduction
  - Eigenvalue Decomposition (EVD)
  - Singular Value Decomposition (SVD)
  
- **Face Recognition Pipeline**:
  - Dataset loading and preprocessing (grayscale conversion)
  - Mean face computation and visualization
  - Face projection onto PCA eigenface space
  - Face reconstruction from reduced dimensions
  
- **Classification**: SVM classifier with linear kernel for face recognition

- **Performance Analysis**:
  - Accuracy evaluation across different numbers of PCA components
  - Runtime comparison between EVD and SVD methods
  - Visualization of accuracy vs. component count

## Dataset

The AT&T (Olivetti Faces) Database contains:
- **40 unique individuals**
- **10 images per person**
- **Image size**: 112 × 92 pixels (grayscale)
- **Total images**: 400

## How It Works

1. **Load Dataset**: Images are loaded from the AT&T dataset and converted to grayscale
2. **Train-Test Split**: 70% training, 30% testing
3. **PCA Computation**: Calculate eigenfaces from training data
4. **Projection**: Project both training and testing images onto the eigenface space
5. **Classification**: Train SVM classifier on projected training data
6. **Evaluation**: Test accuracy on projected test data with varying PCA components
7. **Visualization**: Display mean face, reconstructed faces, and accuracy plots

## Dependencies

- NumPy
- Scikit-learn
- Matplotlib
- Pillow (PIL)

## Usage

Run the Jupyter notebook `FACE_RECOGNITION_PROJECT2(1)(1).ipynb` to execute the complete pipeline. The notebook includes visualization of:
- Mean face across all training images
- Reconstructed faces with varying numbers of PCA components
- Accuracy metrics for different component counts
- Runtime comparison between PCA methods
