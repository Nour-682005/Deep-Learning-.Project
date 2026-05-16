# Deep-Learning-.Project
# Handwritten Digit Recognition using CNN (MNIST)

## 1. Problem Description
This project implements a Deep Learning model for handwritten digit recognition using Convolutional Neural Networks (CNN).

The goal is to classify grayscale handwritten digit images from the MNIST dataset into 10 classes (0–9).

---

## 2. Dataset
The project uses the MNIST dataset.

- Dataset Source: Automatically downloaded using torchvision
- Dataset Link: http://yann.lecun.com/exdb/mnist/

Dataset Information:
- Training Images: 60,000
- Testing Images: 10,000
- Image Size: 28 × 28
- Classes: 10 digits (0–9)

---

## 3. Preprocessing
The following preprocessing steps were applied:

- Convert images to tensors using `ToTensor()`
- Normalize pixel values to range [-1, 1]

```python
transforms.Normalize((0.5,), (0.5,))
```

---

## 4. Model Architecture
A custom CNN model was implemented using:

- Conv2D Layer (1 → 32)
- ReLU Activation
- MaxPooling
- Conv2D Layer (32 → 64)
- ReLU Activation
- MaxPooling
- Fully Connected Layer
- Dropout (0.25)
- Output Layer (10 classes)

Enhancement Technique:
- Dropout to reduce overfitting

---

## 5. Training Configuration
Training settings:

- Epochs: 5
- Batch Size: 64
- Loss Function: CrossEntropyLoss

Two experiments were conducted.

---

## 6. Experiments

### Experiment 1
- Optimizer: Adam
- Learning Rate: 0.001

### Experiment 2
- Optimizer: SGD
- Learning Rate: 0.01

---

## 7. Results Comparison

| Model | Optimizer | Learning Rate | Accuracy | Loss |
|---|---|---|---|---|
| Model A | Adam | 0.001 | 99.12% | 0.0272 |
| Model B | SGD | 0.01 | 97.97% | 0.0652 |

---

## 8. Analysis
Two experiments were performed using different optimizers.

- Adam optimizer achieved better performance with higher accuracy and lower loss.
- SGD optimizer achieved lower accuracy and required more time to converge.

Conclusion:
Adam optimizer performed better than SGD for MNIST handwritten digit classification.

---

## 9. Visualization
Training and validation curves are included:

- Training vs Validation Loss
- Training vs Validation Accuracy

Project Results:

![Training Results](results.png)

---

## 10. How to Run

1. Open Google Colab or Jupyter Notebook
2. Install required libraries:

```bash
pip install torch torchvision matplotlib
```

3. Run all notebook cells in order

---

## 11. Repository Contents
Repository includes:

- Source code notebook
- README file
- Results image

---
