# Single Layer Perceptron for Binary Classification

## Overview

This project implements a **Single Layer Perceptron** from scratch for binary classification using the **Banknote Authentication Dataset**. The implementation demonstrates the fundamentals of artificial neural networks, including the perceptron learning algorithm, weight updates, bias optimization, and performance evaluation.

The project was completed as part of the **CS3807 – Deep Learning Laboratory** 

---

## Objectives

- Understand the architecture of a single artificial neuron.
- Implement the Perceptron Learning Algorithm from scratch.
- Perform Exploratory Data Analysis (EDA).
- Preprocess the dataset.
- Train and evaluate the perceptron model.
- Analyze the effect of different learning rates.
- Compare results with Scikit-learn's implementation 

---

## Dataset

**Dataset:** Banknote Authentication Dataset

- **Instances:** 1372
- **Features:** 4 numerical features
- **Classes:** 2
- **Task:** Binary Classification

### Features

- Variance
- Skewness
- Curtosis
- Entropy

### Target

- **0** → Authentic Banknote
- **1** → Forged Banknote 

---

## Project Workflow

1. Load the dataset
2. Perform Exploratory Data Analysis
3. Normalize features
4. Split data into training and testing sets
5. Implement Single Layer Perceptron from scratch
6. Train using the Perceptron Learning Rule
7. Evaluate model performance
8. Compare different learning rates 

---

## Exploratory Data Analysis

The following visualizations were generated:

- Feature Histograms
- Correlation Heatmap
- Scatter Plot
- Boxplots

These plots help understand feature distributions, identify correlations, detect outliers, and visualize class separability. 

---

## Model Implementation

The perceptron was implemented without using machine learning libraries for training.

Implementation includes:

- Weight Initialization
- Bias Initialization
- Step Activation Function
- Forward Propagation
- Perceptron Learning Rule 

---

## Evaluation Metrics

The model is evaluated using:

- Accuracy
- Precision
- Recall
- F1-Score
- Confusion Matrix 

---

## Learning Rate Analysis

The perceptron was trained using multiple learning rates:

- 0.001
- 0.01
- 0.1
- 0.5
- 1.0

The convergence behaviour and model performance were compared across different learning rates. 

---

## Requirements

Install the required packages using:

```bash
pip install -r requirements.txt
```

---

## Results

The project includes:

- Dataset exploration
- Data preprocessing
- Perceptron implementation from scratch
- Performance evaluation
- Training error visualization
- Weight and bias evolution
- Learning rate comparison
- Confusion matrix

---

## Key Concepts Covered

- Artificial Neuron
- Perceptron Learning Algorithm
- Binary Classification
- Step Activation Function
- Gradient-Free Learning
- Feature Normalization
- Model Evaluation
- Hyperparameter Analysis

---

## References

1. F. Rosenblatt, *The Perceptron*, 1958.
2. Ian Goodfellow, Yoshua Bengio, Aaron Courville – *Deep Learning*
3. Christopher Bishop – *Pattern Recognition and Machine Learning*
4. Simon Haykin – *Neural Networks and Learning Machines*
5. UCI Machine Learning Repository – Banknote Authentication Dataset
6. Scikit-learn Documentation 

