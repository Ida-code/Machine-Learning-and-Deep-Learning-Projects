Skin Cancer Classification using MobileNetV2
Project Overview
This project focuses on binary classification of skin lesion images into two categories:
1.)Benign
2.)Malignant

Model Architecture

The model is based on MobileNetV2, a lightweight convolutional neural network pretrained on ImageNet.

Key modifications:
*Loaded pretrained ImageNet weights
*Removed the original classification head
*Added a custom fully connected layer
*Modified the final output layer to predict 2 classes (benign and malignant)

Data Split
80% Training
20% Testing

Training Strategy
*Optimizer: Adam
*Loss Function: Sparse Categorical Crossentropy
*Early Stopping was used to prevent overfitting



Evaluation performed using accuracy and confusion matrix

Early Stopping
->Early stopping was implemented to stop training when validation performance stopped improving, preventing unnecessary epochs and reducing overfitting.


Accuracy:
Train Acc: 0.8173 | Val Acc: 0.7991
Train Loss: 0.3904 | Val Loss: 0.4173

Rationale for Using MobileNetV2
->MobileNetV2 was selected because:
->It is computationally efficient
->It performs well on smaller datasets
->It provides strong feature extraction through pretrained weights
->It reduces training time compared to training a CNN from scratch
