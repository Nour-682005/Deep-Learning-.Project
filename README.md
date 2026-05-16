# Medical Image Classification: Pneumonia Detection
### Deep Learning Course Project

## 1. Problem Description
This project focuses on classifying chest X-ray images into two categories: **Normal** and **Pneumonia**. The goal is to develop a Deep Learning model that can assist in medical diagnosis by automatically detecting signs of pneumonia from X-ray scans.

## 2. Dataset
- **Source**: [Chest X-Ray Images (Pneumonia) - Kaggle](https://www.kaggle.com/datasets/paultimothymooney/chest-xray-pneumonia)
- **Size**: 5,863 images.
- **Preprocessing**: Images were resized to 224x224 pixels and normalized (rescaled to [0, 1]).

## 3. Model Architecture
A Convolutional Neural Network (CNN) was implemented with the following architecture:
- **Multiple Hidden Layers**: Conv2D and MaxPooling2D layers for feature extraction.
- **Enhancement Techniques**: 
    - **Batch Normalization**: Applied for faster training and stability.
    - **Dropout**: Applied (0.5) to prevent overfitting.
- **Output Layer**: Dense layer with Sigmoid activation for binary classification.

## 4. Experimentation & Results
Two mandatory experiments were conducted by varying the **Optimizer** to compare performance:

| Experiment | Optimizer | Training Accuracy | Validation Accuracy | Final Loss |
| :--- | :--- | :--- | :--- | :--- |
| **Experiment 1** | **Adam** | ~96.7% | ~85.7% | 0.4195 |
| **Experiment 2** | **SGD** | ~98.0% | ~64.0% | 2.7200 |

### **Visualization**
The project includes training vs. validation loss and accuracy curves for both experiments to monitor performance and convergence.

## 5. Submission Requirements
- **Source Code**: Provided in the `deeep.ipynb` file.
- **Dataset**: Linked above.
- **README**: Includes problem description, dataset link, results table, and instructions.

## 6. How to Run
1. Download the `deeep.ipynb` file and open it in Google Colab.
2. Upload your `kaggle.json` API key to the session storage.
3. Run the cells sequentially to download the data and train the model.
