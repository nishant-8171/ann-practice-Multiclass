# ANN Multiclass Classification — Practice Project

## Project Overview

This is a beginner-friendly machine learning practice project that uses an **Artificial Neural Network (ANN)** to classify handwritten digits from the MNIST dataset.

The objective is to train a neural network that can recognize digits from **0 to 9** using grayscale images.

**Project Type:** Practice / Learning Project  
**Task:** Multiclass Image Classification  
**Dataset:** MNIST Handwritten Digits

## Technologies Used

- Python
- TensorFlow and Keras
- NumPy
- Matplotlib
- Scikit-learn
- Jupyter Notebook

## Project Workflow

1. Load the MNIST dataset using Keras.
2. Explore and visualize handwritten digit images.
3. Normalize pixel values between 0 and 1.
4. Build an ANN using the Keras Sequential API.
5. Compile the model using the Adam optimizer and sparse categorical cross-entropy loss.
6. Train the model for 25 epochs with a 20% validation split.
7. Generate predictions for test images.
8. Evaluate the model using accuracy.
9. Visualize training and validation loss.

## ANN Model Architecture

| Layer | Configuration |
|---|---|
| Flatten | Converts 28 × 28 images into 784 features |
| Dense | 128 neurons, ReLU activation |
| Dense | 32 neurons, ReLU activation |
| Output Dense | 10 neurons, Softmax activation |

The model contains **104,938 trainable parameters**.

## Data Preprocessing

The MNIST dataset is loaded directly from TensorFlow/Keras. Each image contains 28 × 28 grayscale pixels.

Pixel normalization is performed using:

```python
x_train = x_train / 255.0
x_test = x_test / 255.0
```

This scales pixel values from 0–255 to 0–1, helping the neural network train more effectively.

## Model Training

The model is compiled with the following settings:

- **Optimizer:** Adam
- **Loss Function:** Sparse Categorical Cross-Entropy
- **Evaluation Metric:** Accuracy
- **Epochs:** 25
- **Validation Split:** 20%

## Results

**Test Accuracy: 97.75%**

The trained model predicts handwritten digit classes from 0 to 9. The notebook also visualizes training and validation loss to examine the model's learning behaviour.

## How to Run the Project

### 1. Install the dependencies

```bash
pip install tensorflow matplotlib scikit-learn jupyter pandas
```

### 2. Open Jupyter Notebook

```bash
jupyter notebook
```

### 3. Run the notebook

Open `ANN_malticlass.ipynb` and execute the cells in order. TensorFlow/Keras will download the MNIST dataset when required.

## Key Learning Outcomes

- Understanding multiclass classification
- Loading and preprocessing image data
- Building an ANN with TensorFlow/Keras
- Understanding Flatten, Dense, ReLU, and Softmax
- Selecting an appropriate loss function
- Training and validating a neural network
- Generating predictions using `model.predict()`
- Evaluating model accuracy
- Visualizing training and validation loss

## Future Improvements

- Add a confusion matrix and classification report.
- Visualize predicted and actual digit labels together.
- Experiment with different network architectures.
- Save and reload the trained model.
- Compare ANN performance with a Convolutional Neural Network (CNN).

## Repository Structure

```text
.
├── ANN_malticlass.ipynb
└── README.md
```

## Project Note

This project is created for **practice and learning purposes** to develop a foundational understanding of artificial neural networks and image classification. It is not intended to be a production-ready application.
