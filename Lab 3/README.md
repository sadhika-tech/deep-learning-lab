# CS3807 – Deep Learning Laboratory

## Experiment 3: Convolutional Neural Network Implementation Using CIFAR-10

## Objective

The objective of this experiment is to implement and analyze a Convolutional Neural Network (CNN) using the CIFAR-10 dataset.

The experiment includes:

- Loading and preprocessing the CIFAR-10 dataset.
- Understanding image dimensions and class distribution.
- Studying the effect of different kernel sizes.
- Comparing stride and padding configurations.
- Visualizing CNN feature maps.
- Comparing max pooling and average pooling.
- Training and evaluating a CNN model.
- Calculating precision, recall, F1-score, and confusion matrix.
- Studying the effect of increasing the number of filters.
- Comparing ReLU and Sigmoid activation functions.
- Calculating convolutional output dimensions and trainable parameters.

---

## Dataset

The CIFAR-10 dataset contains 60,000 colour images belonging to 10 classes.

| Dataset | Number of Images |
|--------|------------------|
| Training Set | 50,000 |
| Testing Set | 10,000 |
| Image Size | 32 × 32 |
| Channels | 3 |
| Number of Classes | 10 |

### Classes

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

---

## Model Architecture

The CNN model consists of the following layers:

```text
Input Layer
32 × 32 × 3
        ↓
Conv2D
16 Filters, 3 × 3 Kernel, ReLU
        ↓
MaxPooling2D
2 × 2 Pool Size
        ↓
Conv2D
32 Filters, 3 × 3 Kernel, ReLU
        ↓
MaxPooling2D
2 × 2 Pool Size
        ↓
Flatten
        ↓
Dense
128 Neurons, ReLU
        ↓
Dropout
        ↓
Dense
10 Neurons, Softmax
        ↓
Output
10 Classes
```

## Technologies Used

- Python
- TensorFlow
- Keras
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

---

## Installation

Install the required dependencies using:

```bash
pip install -r requirements.txt
