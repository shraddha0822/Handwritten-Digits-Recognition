# Handwritten Digit Recognition

This project implements a handwritten digit recognition system using TensorFlow and Keras with the MNIST dataset.

## Overview

The system classifies handwritten digits (0-9) from grayscale images using a deep learning model.

## Requirements

- Python 3.x
- TensorFlow
- NumPy
- Matplotlib

## Functionality:

1. Imports: Includes necessary libraries like TensorFlow, NumPy, and Matplotlib.
2. MNIST Dataset: Loads the MNIST dataset containing training and testing images of handwritten digits (0-9).
3. Data Preprocessing:
   * Visualizes the first 9 training images.
   * Normalizes pixel values between 0 and 1 for better training performance.
   * One-hot encodes labels for categorical crossentropy loss.
4. Model Architecture:
   * Defines a sequential model with:
       * Input layer (28x28 pixels, grayscale channel).
       * Flatten layer to convert images into a single vector.
       * Two Dense layers with 256 and 128 neurons respectively, each with ReLU activation and Dropout (50%) for         regularization.
       * BatchNormalization layers to improve training stability.
       * Output layer with 10 neurons and softmax activation for digit classification (0-9).
5. Model Compilation:
   * Uses RMSprop optimizer for efficient training.
   * Employs categorical crossentropy loss for multi-class classification.
   * Tracks accuracy as the evaluation metric.
6. Early Stopping:
   * Implements early stopping to prevent overfitting. This technique monitors validation loss and stops training if it doesn't improve for 3 consecutive epochs.
7. Model Training:
   * Trains the model for 50 epochs with a batch size of 32.
   * Splits 20% of training data for validation.
8. Training Visualization:
   * Plots training and validation accuracy/loss curves to analyze model performance.
9. Model Evaluation:
   * Evaluates the model's performance on unseen test data.
   * Prints the test accuracy.

## Instructions:

* Save the code as a Python file (e.g., mnist_classification.py).
* Run the script using python mnist_classification.py.
* The script will generate training progress plots and display a sample prediction.

## **License**

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
