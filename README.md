# Deep-Learning-Based-Pizza-Image-Classification-System

## Overview

This project presents a comprehensive comparative study of modern Deep Learning techniques for binary image classification (Pizza vs. Not Pizza).

The objective was to design, train, evaluate, and compare multiple computer vision architectures ranging from traditional machine learning approaches to advanced deep learning models, transfer learning techniques, knowledge distillation, attention mechanisms, and explainable AI methods.

The project was developed using TensorFlow, Keras, and PyTorch.

---

## Dataset
https://www.kaggle.com/datasets/carlosrunner/pizza-not-pizza 
The dataset consists of two image categories:

- Pizza
- Not Pizza

Images were resized to **224 × 224 pixels** and divided into:

- Training Set (80%)
- Validation Set (10%)
- Test Set (10%)

Data augmentation techniques were applied to improve model generalization:

- Random Horizontal Flip
- Random Rotation
- Random Zoom

---

## Implemented Approaches

### 1. Custom CNN Architecture

A Convolutional Neural Network developed from scratch using TensorFlow/Keras.

Features:

- Multiple Conv2D layers
- MaxPooling layers
- Data augmentation
- Softmax classification layer

Evaluation Metrics:

- Accuracy
- F1-Score
- Matthews Correlation Coefficient (MCC)
- Confusion Matrix
- ROC Curve

---

### 2. Traditional Machine Learning Baselines

To provide a comparison with deep learning approaches, the following classifiers were implemented:

#### Random Forest

- 100 estimators
- Image flattening preprocessing

#### Support Vector Machine (SVM)

- Linear Kernel
- High-dimensional image feature representation

---

### 3. Transfer Learning

A pretrained ResNet50 architecture was used as a feature extractor.

Characteristics:

- ImageNet pretrained weights
- Frozen backbone
- Custom classification head
- Faster convergence
- Improved classification performance

---

### 4. Knowledge Distillation

A Teacher-Student framework was implemented.

Teacher Model:

- MobileNetV2

Student Model:

- Lightweight custom CNN

Benefits:

- Reduced computational complexity
- Smaller deployment model
- Knowledge transfer from a larger network

---

### 5. Advanced Dual-Branch Attention Architecture

A custom architecture was developed using PyTorch.

Components:

#### Branch 1

- EfficientNet-B0
- CBAM Attention Module

#### Branch 2

- EfficientNet-B3
- ECA Attention Module

#### Feature Fusion

Features extracted from both branches are fused and passed through fully connected layers for final classification.

Advantages:

- Multi-scale feature extraction
- Attention-enhanced learning
- Improved robustness

---

### 6. Explainable Artificial Intelligence (XAI)

Grad-CAM was implemented to visualize model decision-making.

This allows:

- Understanding model predictions
- Identifying important image regions
- Improving model interpretability

---

## Technologies Used

### Programming Languages

- Python

### Deep Learning Frameworks

- TensorFlow
- Keras
- PyTorch

### Machine Learning

- Scikit-Learn

### Data Processing

- NumPy
- Pandas

### Visualization

- Matplotlib
- Seaborn

### Computer Vision

- OpenCV
- PIL

---

## Model Evaluation

The models were evaluated using:

- Accuracy
- F1-Score
- Matthews Correlation Coefficient (MCC)
- ROC-AUC
- Confusion Matrix
- 5-Fold Cross Validation

---

## Results

The experimental results demonstrated that advanced deep learning architectures incorporating:

- Transfer Learning
- Attention Mechanisms
- Knowledge Distillation

significantly outperform traditional machine learning approaches for image classification tasks.

The best performing architecture achieved over **92% classification accuracy** while maintaining strong generalization capabilities.

---

## Explainability

Grad-CAM visualizations were generated to highlight the image regions that influenced model predictions.

These visual explanations improve transparency and trustworthiness of the classification process.

---

## Project Structure

```text
├── dataset/
│   ├── pizza/
│   └── not_pizza/
│
├── models/
│   ├── Custom CNN
│   ├── ResNet50 Transfer Learning
│   ├── Knowledge Distillation
│   └── Dual Branch Attention Network
│
├── evaluation/
│   ├── ROC Curves
│   ├── Confusion Matrices
│   └── Performance Metrics
│
└── notebooks/
```

---

## Future Improvements

- Multi-class food classification
- Vision Transformers (ViT)
- EfficientNetV2
- Ensemble Learning
- Deployment as a Web Application
- Real-time inference on mobile devices

---

## Author

**Elena Parteni**

M.Sc. Student – Advanced Information Technologies  
Faculty of Automation, Computers, Electrical and Electronics Engineering  
"Dunărea de Jos" University of Galați

GitHub: https://github.com/elenaaep
LinkedIn: https://linkedin.com/in/parteni-elena
