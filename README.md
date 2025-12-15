# Breast Cancer Classification using Logistic Regression

## Overview
This project implements a **binary classification model** to predict whether a breast tumor is **benign or malignant** using the **Breast Cancer Wisconsin Diagnostic Dataset**.  
The project demonstrates both:
- Logistic Regression implemented **from scratch** using NumPy
- Logistic Regression using **Scikit-learn** for comparison

The workflow follows the supervised learning principles taught in Andrew Ng’s *Supervised Machine Learning* course.

---

## Dataset Description
- Dataset: Breast Cancer Wisconsin Diagnostic Dataset
- Source: Kaggle
- File used: `data.csv`
- Number of samples: 569
- Number of features: 30 numerical features
- Target variable: `diagnosis`
  - `M` → Malignant (1)
  - `B` → Benign (0)

Unnecessary columns such as `id` and `Unnamed: 32` are removed during preprocessing.

---

## Project Workflow

### 1. Data Loading and Cleaning
- Dataset loaded using Pandas.
- Dropped irrelevant columns.
- Converted target labels from categorical to binary values.

### 2. Data Normalization
- Min–Max normalization applied to all features:
  \[
  x_{normalized} = \frac{x - x_{min}}{x_{max} - x_{min}}
  \]
- Normalization ensures stable and faster gradient descent convergence.

### 3. Train-Test Split
- Dataset split into training and testing sets.
- Test size: 15%
- Data reshaped to match mathematical formulation of logistic regression.

---

## Logistic Regression (From Scratch)

### Key Components Implemented
- Weight and bias initialization
- Sigmoid activation function
- Forward propagation
- Binary cross-entropy loss
- Backward propagation
- Gradient descent parameter updates
- Prediction function with threshold = 0.5

### Training Details
- Learning rate: 1
- Number of iterations: 100
- Cost reduction visualized using a cost vs iteration plot

### Performance
- Training Accuracy: ~80.7%
- Testing Accuracy: ~81.3%

---

## Logistic Regression using Scikit-learn

- Model: `sklearn.linear_model.LogisticRegression`
- Max iterations: 150
- Random state: 42

### Performance
- Training Accuracy: ~86.3%
- Testing Accuracy: ~89.5%

---

## Observations
- Custom implementation helps in understanding the mathematics behind logistic regression.
- Scikit-learn implementation achieves higher accuracy due to optimized solvers.
- Normalization plays a crucial role in convergence.
- Logistic regression performs well on structured medical datasets.

---

## Technologies Used
- Python
- NumPy
- Pandas
- Matplotlib
- Scikit-learn

---

## References
- Breast Cancer Wisconsin Dataset (Kaggle)
- Andrew Ng – Supervised Machine Learning
- Scikit-learn Documentation
