# Multi-Layer Perceptron for Multi-Class Image Classification

## Overview

This project implements a **Multi-Layer Perceptron (MLP)** using **TensorFlow/Keras** for multi-class image classification on the **Fashion-MNIST Dataset**. The implementation demonstrates the working of neural networks, including image preprocessing, model construction, training, evaluation, and automated hyperparameter optimization.

The project was completed as part of the **CS3807 – Deep Learning Laboratory**

---

## Objectives

- Understand the architecture of a Multi-Layer Perceptron.
- Perform image preprocessing for neural networks.
- Implement an MLP model using TensorFlow/Keras.
- Train and evaluate a multi-class classification model.
- Analyze model performance using evaluation metrics.
- Perform automated hyperparameter optimization.
- Compare baseline and optimized model performance.

---

## Dataset

**Dataset:** Fashion-MNIST Dataset

- **Training Images:** 60,000
- **Testing Images:** 10,000
- **Image Size:** 28 × 28 pixels
- **Input Features:** 784
- **Classes:** 10
- **Task:** Multi-Class Classification

### Classes

The dataset contains the following clothing categories:

- T-shirt / Top
- Trouser
- Pullover
- Dress
- Coat
- Sandal
- Shirt
- Sneaker
- Bag
- Ankle Boot

---

## Project Workflow

1. Load the Fashion-MNIST dataset.
2. Perform dataset exploration.
3. Visualize sample images and class distribution.
4. Flatten images from 28 × 28 to 784-dimensional vectors.
5. Normalize pixel values.
6. Convert labels into one-hot encoded vectors.
7. Construct the MLP architecture.
8. Train the baseline model.
9. Evaluate model performance.
10. Perform hyperparameter optimization.
11. Retrain the optimized model.
12. Compare baseline and optimized models.

---

## Exploratory Data Analysis

The following visualizations were generated:

- Sample Images
- Class Distribution Plot

These plots help understand the dataset structure, identify class balance, and visualize sample images from different categories.

---

## Data Preprocessing

The following preprocessing steps were performed:

- Flattening images:

```
28 × 28 → 784 features
```

- Normalizing pixel values:

```
Pixel range: 0-255
Converted range: 0-1
```

- One-hot encoding target labels.

---

## Model Architecture

The baseline MLP architecture consists of:

```
Input Layer (784)

        ↓

Dense Layer (128 neurons, ReLU)

        ↓

Dense Layer (64 neurons, ReLU)

        ↓

Output Layer (10 neurons, Softmax)
```

The output layer uses **Softmax activation** for multi-class classification.

---

## Model Training

The model was trained using:

- **Optimizer:** Adam
- **Loss Function:** Categorical Cross Entropy
- **Metric:** Accuracy
- **Epochs:** 20
- **Batch Size:** 32

---

## Model Evaluation

The model is evaluated using:

- Accuracy
- Precision
- Recall
- F1-Score
- Confusion Matrix
- Classification Report

---

## Hyperparameter Optimization

Automated hyperparameter optimization was performed using:

**RandomizedSearchCV with SciKeras Wrapper**

The following hyperparameters were optimized:

- Number of Hidden Layers
- Number of Hidden Neurons
- Learning Rate
- Batch Size
- Number of Epochs
- Optimizer
- Activation Function

### Search Space

| Hyperparameter | Values |
|---|---|
| Hidden Layers | 1, 2, 3 |
| Hidden Neurons | 32, 64, 128, 256 |
| Learning Rate | 0.1, 0.01, 0.001 |
| Batch Size | 16, 32, 64, 128 |
| Epochs | 10, 20, 30 |
| Optimizer | SGD, Adam, RMSProp |
| Activation | ReLU, Tanh, Sigmoid |

---

## Hyperparameter Optimization Workflow

1. Built the baseline MLP model.
2. Defined the hyperparameter search space.
3. Applied Randomized Search with 5-fold cross-validation.
4. Selected the best hyperparameter combination.
5. Retrained the model using optimized parameters.
6. Evaluated the optimized model.
7. Compared baseline and optimized performance.

---

## Training Analysis

The following plots were generated:

- Training Accuracy vs Epoch
- Validation Accuracy vs Epoch
- Training Loss vs Epoch
- Validation Loss vs Epoch

These plots help analyze model learning behaviour, convergence, and possible overfitting.

---

## Results

The project includes:

- Dataset exploration
- Image preprocessing
- MLP model implementation
- Baseline model evaluation
- Hyperparameter optimization
- Optimized model evaluation
- Confusion matrix visualization
- Hyperparameter search analysis
- Baseline vs optimized model comparison

---

## Performance Comparison

The baseline and optimized models were compared using:

- Accuracy
- Precision
- Recall
- F1-score
- Training Time

The optimized model configuration was selected based on cross-validation performance.

---

## Key Concepts Covered

- Multi-Layer Perceptron
- Artificial Neural Networks
- Forward Propagation
- Activation Functions
- Softmax Classification
- Categorical Cross Entropy
- Image Flattening
- Feature Normalization
- Hyperparameter Optimization
- Model Evaluation

---

## Requirements

Install the required packages using:

```bash
pip install -r requirements.txt
```

---

## References

1. Ian Goodfellow, Yoshua Bengio, Aaron Courville – *Deep Learning*
2. Christopher Bishop – *Pattern Recognition and Machine Learning*
3. Simon Haykin – *Neural Networks and Learning Machines*
4. Fashion-MNIST Dataset
5. TensorFlow/Keras Documentation
6. Scikit-learn Documentation
