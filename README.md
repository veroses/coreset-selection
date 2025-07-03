# Coreset Selection for Neural Network Training

This project is a short educational experiment designed to help me explore coreset selection and neural network training using PyTorch. The goal was to benchmark k-means clustering-based subset selection against random sampling and observe their effects on training efficiency and generalization.


## Project Summary
- **Dataset:** MNIST
- **Model:** Convolutional Neural Network (CNN) built using PyTorch
- **Subset Selection:** K-means clustering vs. random sampling

## Notebook Sections

### 1. Setup
This section imports all required libraries, sets random seeds for reproducibility, and configures the device (CPU or GPU). Seeding ensures that results can be consistently replicated.

### 2. Data Preparation
Loads the MNIST dataset and defines DataLoaders for both training and testing. DataLoaders handle batching and shuffling to efficiently pass data to the model during training.

### 3. Model Definition
Defines the convolutional neural network (CNN) architecture using PyTorch’s `nn.Module`. The model consists of convolutional layers, activation functions, dropout, and fully connected layers for classification.

### 4. Training & Evaluation Utilities
Provides reusable functions for training the model, evaluating its performance, and tracking accuracy and loss over time. These utilities work for both the baseline and coreset-selected training.

### 5. Subset Selection Utilities
Implements k-means clustering for coreset selection and random sampling as a baseline method. These functions control which training points are selected during each subset update.

### 6. Experiment
This is the main experiment block where all hyperparameters are defined. Training loops are run for both the baseline (random sampling) and coreset (k-means) models. Model performance is logged and compared.

### 7. Visualization
Plots training and test accuracy and loss for both models to visually compare their learning dynamics. Graphs help illustrate the trade-offs between k-means selection and random sampling.
