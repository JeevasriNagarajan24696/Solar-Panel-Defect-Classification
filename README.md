# Solar Panel Defect Classification Using Deep Learning

**Course:** ENGR 501 – Deep and Reinforcement Learning for Engineers  
**Institution:** University of British Columbia, Okanagan Campus  
**Project:** Deep Learning-Based Solar Panel Defect Classification Using Convolutional Neural Networks

## 1. Project Overview

Solar panels are exposed to environmental conditions such as dust, snow, and bird droppings, as well as physical and electrical damage. These conditions can affect solar-panel performance and create maintenance challenges.

This project investigates the use of Convolutional Neural Networks (CNNs) to classify solar-panel images into six categories. The objective is to develop a baseline CNN, evaluate its performance, and investigate techniques for improving classification accuracy.

## 2. Project Objectives

- Develop a CNN-based solar-panel image classification system.
- Prepare and clean an existing publicly available dataset.
- Train and evaluate a baseline CNN.
- Analyze training and validation accuracy and loss.
- Investigate improvements through data augmentation and training optimization.
- Compare the baseline CNN with a transfer-learning approach.

## 3. Dataset

**Source:** [Solar Panel Images – Kaggle](https://www.kaggle.com/datasets/pythonafroz/solar-panel-images)

The dataset contains six image categories:

1. Clean
2. Dusty
3. Bird-drop
4. Electrical-damage
5. Physical-Damage
6. Snow-Covered

### Dataset Preparation

The original dataset contained 885 readable images.

During preprocessing:

- Exact duplicate images were identified using SHA-256 hashing.
- 91 extra duplicate copies were detected.
- Two groups containing conflicting class labels were excluded.
- The final cleaned dataset contained 792 images.

### Dataset Split

| Dataset | Number of Images |
|---|---:|
| Training | 554 |
| Validation | 119 |
| Testing | 119 |
| **Total** | **792** |

A stratified 70/15/15 split was used to maintain approximately similar class proportions across the datasets.

Images were resized to 224 × 224 pixels using aspect-ratio-preserving padding and normalized to the range 0–1.

## 4. Tools and Technologies

- Python
- TensorFlow
- Keras
- Google Colab
- NumPy
- Pandas
- Matplotlib
- Scikit-learn
- GitHub

## 5. Baseline CNN Architecture

The baseline model uses:

- Three convolutional layers with ReLU activation
- Three max-pooling layers
- Global average pooling
- A fully connected layer with 64 neurons
- A softmax output layer for six-class classification

**Total trainable parameters:** 101,894

### Training Configuration

| Parameter | Value |
|---|---|
| Optimizer | Adam |
| Learning rate | 0.001 |
| Loss function | Sparse Categorical Cross-Entropy |
| Batch size | 32 |
| Epochs | 15 |
| Input image size | 224 × 224 × 3 |

## 6. Baseline CNN Results

The baseline CNN was trained for 15 epochs.

| Evaluation Metric | Result |
|---|---:|
| Final training accuracy | 45.85% |
| Final validation accuracy | 42.86% |
| Highest validation accuracy | 49.58% |
| Final training loss | 1.3986 |
| Final validation loss | 1.3930 |

### Observations

- Training accuracy generally increased during the 15 epochs.
- Training loss decreased overall.
- Validation accuracy and loss fluctuated.
- The baseline model demonstrated some learning capability, but classification accuracy remained limited.
- The results suggest possible underfitting rather than clear, sustained overfitting.

These results establish a reference for evaluating subsequent improvements.

## 7. Planned Experiments

The following experiments will be investigated:

| Experiment | Approach | Status |
|---|---|---|
| 1 | Baseline CNN | Completed |
| 2 | CNN with Data Augmentation | Planned |
| 3 | CNN with Training Optimization | Planned |
| 4 | MobileNetV2 Transfer Learning | Planned |

The experiments will be compared using classification metrics and learning curves.

## 8. Project Files

**Solar_Panel_Defect_Classification.ipynb**

The Google Colab notebook contains the dataset preparation, preprocessing, baseline CNN implementation, training, and learning-curve visualizations.

## 9. Future Work

- Implement data augmentation.
- Investigate learning-rate and training improvements.
- Train and evaluate MobileNetV2.
- Compare model performance using accuracy, precision, recall, F1-score, and confusion matrices.
- Evaluate the selected final model using the held-out test dataset.

## 10. Project Status

**Current stage:** Baseline CNN training and validation analysis completed.

Further experiments and final evaluation are in progress.
