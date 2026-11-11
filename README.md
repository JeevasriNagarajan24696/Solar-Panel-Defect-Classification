# Solar Panel Defect Classification Using Deep Learning

**Course:** ENGR 501 – Deep and Reinforcement Learning for Engineers  
**Institution:** University of British Columbia, Okanagan Campus  
**Project:** Deep Learning-Based Solar Panel Defect Classification Using Convolutional Neural Networks

## 1. Project Overview

Solar panels are exposed to environmental conditions such as dust, snow, and bird droppings, as well as physical and electrical damage. These conditions can affect solar-panel performance and create maintenance challenges.

This project investigates Convolutional Neural Networks (CNNs) and transfer learning for classifying solar-panel images into six categories. Four deep learning models were developed and evaluated to compare their classification performance.

## 2. Project Objectives

- Develop a CNN-based solar-panel image classification system.
- Prepare and preprocess a publicly available image dataset.
- Train and evaluate a baseline CNN.
- Investigate data augmentation and training optimization.
- Apply transfer learning using MobileNetV2.
- Compare four models using validation and test performance.
- Analyze classification reports and confusion matrices.

## 3. Dataset

**Source:** [Solar Panel Images – Kaggle](https://www.kaggle.com/datasets/pythonafroz/solar-panel-images)

The dataset contains six image categories:

1. Clean
2. Dusty
3. Bird-drop
4. Electrical-damage
5. Physical-Damage
6. Snow-Covered

Images were resized to 224 × 224 pixels and prepared for CNN training, validation, and testing.

## 4. Technologies Used

- Python
- TensorFlow and Keras
- Google Colab
- NumPy
- Pandas
- Matplotlib
- Scikit-learn
- GitHub

## 5. Model Development

Four deep learning experiments were conducted.

### Experiment 1: Baseline CNN

A CNN model was developed using convolutional layers, max-pooling layers, global average pooling, and dense layers.

The baseline CNN served as the reference model for evaluating subsequent improvements.

**Test Accuracy:** 42.02%  
**Test Loss:** 1.4113

### Experiment 2: CNN with Data Augmentation

Data augmentation was incorporated into the CNN training pipeline to investigate whether image transformations could improve generalization.

**Test Accuracy:** 34.45%  
**Test Loss:** 1.7613

Data augmentation did not improve test accuracy compared with the baseline CNN in this experiment.

### Experiment 3: Optimized CNN

The third experiment incorporated dropout and training adjustments to investigate potential improvements in classification performance.

**Test Accuracy:** 35.29%  
**Test Loss:** 1.5899

The optimized CNN did not outperform the baseline CNN.

### Experiment 4: MobileNetV2 Transfer Learning

A transfer-learning model was developed using MobileNetV2 with pretrained ImageNet weights.

The pretrained feature-extraction layers were frozen, and new classification layers were added for the six solar-panel categories.

**Test Accuracy:** 67.23%  
**Test Loss:** 0.9064

MobileNetV2 achieved the highest test accuracy among the four models.

## 6. Final Model Comparison

| Model | Test Accuracy (%) | Test Loss |
|---|---:|---:|
| Baseline CNN | 42.02 | 1.4113 |
| Augmented CNN | 34.45 | 1.7613 |
| Optimized CNN | 35.29 | 1.5899 |
| **MobileNetV2** | **67.23** | **0.9064** |

**Best Performing Model: MobileNetV2**

MobileNetV2 improved test accuracy by approximately 25.21 percentage points compared with the baseline CNN.

## 7. Classification Performance

The classification performance of the models was evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion matrix

The MobileNetV2 model correctly classified 13 out of 14 Electrical-damage images, achieving 92.86% recall for that category.

Dusty and Physical-Damage images remained more challenging to classify.

## 8. Key Findings

1. The baseline CNN achieved 42.02% test accuracy.
2. Data augmentation did not improve test accuracy in the second experiment.
3. The optimized CNN achieved 35.29% test accuracy.
4. MobileNetV2 achieved the highest test accuracy of 67.23%.
5. Transfer learning substantially improved classification performance compared with the custom CNN models.
6. Some categories remained challenging because of classification errors between visually similar conditions.

## 9. Future Improvements

Potential future improvements include:

- Increasing the number of training images.
- Addressing class imbalance.
- Fine-tuning selected pretrained MobileNetV2 layers.
- Investigating additional image preprocessing methods.
- Evaluating other transfer-learning architectures.

## 10. Conclusion

This project investigated CNN-based solar-panel defect classification using four deep learning experiments.

The results demonstrated that MobileNetV2 outperformed the three custom CNN models, achieving 67.23% test accuracy and 0.9064 test loss.

Although the transfer-learning approach improved overall classification performance, challenges remained in identifying certain defect categories.

Overall, the project demonstrates the potential of transfer learning for automated solar-panel condition monitoring.
