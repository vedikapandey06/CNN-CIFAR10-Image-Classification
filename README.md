# CNN-CIFAR10-Image-Classification
Image classification using a Convolutional Neural Network (CNN) on the CIFAR-10 dataset using TensorFlow and Keras.

# Image Classification using CNN

## 📌 Project Overview

This project implements a **Convolutional Neural Network (CNN)** for image classification using the **CIFAR-10 dataset**. The model is developed using **TensorFlow and Keras** and is trained to classify color images into one of ten different categories.

The project demonstrates the complete workflow of an image classification problem, including data preprocessing, CNN architecture design, model training, evaluation, and prediction.

---

## 🎯 Objectives

* Load and preprocess the CIFAR-10 dataset.
* Normalize image pixel values.
* Design a Convolutional Neural Network using convolution and pooling layers.
* Train the CNN model on the CIFAR-10 training dataset.
* Evaluate the model using accuracy and loss.
* Generate a confusion matrix to analyze classification performance.
* Display predictions for sample test images.

---

## 📊 Dataset

The **CIFAR-10 dataset** contains 60,000 color images belonging to 10 different classes.

| Feature           | Details     |
| ----------------- | ----------- |
| Total Images      | 60,000      |
| Training Images   | 50,000      |
| Testing Images    | 10,000      |
| Image Size        | 32 × 32 × 3 |
| Number of Classes | 10          |
| Image Type        | RGB Color   |

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

## ⚙️ Data Preprocessing

The following preprocessing steps were performed:

1. Loaded the CIFAR-10 dataset using TensorFlow Keras.
2. Visualized sample images from the dataset.
3. Normalized pixel values from the range `0–255` to `0–1`.
4. Converted the class labels into one-hot encoded vectors.
5. Prepared the processed data for CNN training and evaluation.

---

## 🧠 CNN Architecture

The Convolutional Neural Network consists of the following layers:

```text
Input Image (32 × 32 × 3)
        ↓
Conv2D - 32 Filters
3 × 3 Kernel + ReLU
        ↓
MaxPooling2D
2 × 2 Pool
        ↓
Conv2D - 64 Filters
3 × 3 Kernel + ReLU
        ↓
MaxPooling2D
2 × 2 Pool
        ↓
Flatten
        ↓
Dense - 128 Neurons
ReLU Activation
        ↓
Output Layer - 10 Neurons
Softmax Activation
```

### Model Configuration

* **Optimizer:** Adam
* **Loss Function:** Categorical Cross-Entropy
* **Metric:** Accuracy
* **Epochs:** 10
* **Batch Size:** 64
* **Validation Split:** 20%

---

## 📈 Results

The trained CNN achieved the following performance:

| Metric              |     Result |
| ------------------- | ---------: |
| Training Accuracy   | **80.40%** |
| Validation Accuracy | **69.86%** |
| Test Accuracy       | **69.46%** |
| Test Loss           | **0.9346** |

The model successfully learned to classify images from the CIFAR-10 dataset. The difference between training and validation performance indicates some degree of overfitting, which could potentially be reduced using techniques such as data augmentation, dropout, and batch normalization.

---


## 🖼️ Results & Visualizations

The `results/` folder contains:

* Sample CIFAR-10 images used for exploratory analysis
* CNN model summary
* Training and validation accuracy graph
* Training and validation loss graph
* Confusion matrix
* Sample predictions with actual and predicted labels

---

## 🛠️ Technologies Used

* Python
* TensorFlow
* Keras
* NumPy
* Matplotlib
* Scikit-learn
* Google Colab
* Jupyter Notebook

---

## 🚀 How to Run

1. Open `CNN_CIFAR10.ipynb` in **Google Colab** or Jupyter Notebook.
2. Install/import the required libraries.
3. Run the notebook cells sequentially.
4. The CIFAR-10 dataset will be downloaded automatically through TensorFlow Keras.
5. Train the CNN model and evaluate its performance.

---

## 📚 References

* TensorFlow: https://www.tensorflow.org/
* CIFAR-10 Dataset: https://www.cs.toronto.edu/~kriz/cifar.html
* TensorFlow CIFAR-10 Dataset API: https://www.tensorflow.org/api_docs/python/tf/keras/datasets/cifar10
* Chollet, F. *Deep Learning with Python*. Manning Publications.
