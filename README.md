# Handwritten Digit Recognition using CNN (MNIST)
### Deep Learning Course Project

## 1. Problem Description
This project implements a Deep Learning model for handwritten digit recognition using Convolutional Neural Networks (CNN). The objective is to classify grayscale handwritten digit images into 10 classes (0–9) to assist in automated digit recognition tasks.

## 2. Dataset
The project utilizes the widely used **MNIST** dataset.
- **Source:** Automatically downloaded using `torchvision.datasets`.
- **Details:** 60,000 training images and 10,000 testing images.
- **Image Size:** 28 × 28 pixels (Grayscale).

## 3. Preprocessing
The following preprocessing steps were applied to the images using PyTorch transforms:
- Converted images to tensors using `ToTensor()`.
- Normalized pixel values to the range [-1, 1] using `Normalize((0.5,), (0.5,))`.

## 4. Model Architecture
A custom Convolutional Neural Network (CNN) was built using `torch.nn.Module` with the following structure:
- **Hidden Layers:** - Conv2D Layer (1 → 32 channels) + ReLU + MaxPooling2D
  - Conv2D Layer (32 → 64 channels) + ReLU + MaxPooling2D
  - Fully Connected (Dense) Layer (3136 → 128) + ReLU
- **Enhancement Technique:** Added a **Dropout** layer (0.25) before the final output to prevent overfitting.
- **Output Layer:** Fully Connected Layer (128 → 10 classes).

## 5. Experimentation & Results
The model was trained for 5 epochs with a batch size of 64 using `CrossEntropyLoss`. Two mandatory experiments were conducted by varying the optimizer:

| Model | Optimizer | Learning Rate | Final Accuracy | Final Loss |
| :--- | :--- | :--- | :--- | :--- |
| **Experiment 1** | **Adam** | 0.001 | 99.12% | 0.0272 |
| **Experiment 2** | **SGD** | 0.010 | 97.97% | 0.0652 |

**Conclusion:** The Adam optimizer converged faster and achieved a higher accuracy compared to SGD for this specific image classification task.

## 6. How to Run
1. Open the provided `.ipynb` file in Google Colab or Jupyter Notebook.
2. Ensure you have the required libraries installed:
   ```bash
   pip install torch torchvision matplotlib
