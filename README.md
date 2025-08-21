# Perceptron & Logistic Regression

**📌 Project Overview**

This project explores **binary classification** using two classic machine learning models:
- Perceptron (built in Python)
- Logistic Regression (using sklearn)

The main goals are:
- Understand how perceptrons work through manual implementation.
- Apply gradient descent to update weights and bias during training.
- Experiment with learning rates and epochs to observe their effects on convergence.
- Compare results with a logistic regression model for the same dataset.

**📂 Dataset**
- Breast Cancer Wisconsin (Diagnostic) Dataset (from UCI ML Repository, available in sklearn.datasets).
- Each sample corresponds to a patient’s tumor measurements.
- Task: Predict whether the tumor is malignant (-1) or benign (1).

**⚙️ Methods**
_1. Data Preprocessing_
- Normalized features.
- Converted labels to -1 and 1.
- Split into training and test sets (train_test_split with random_state=123, test_size=0.2).

_2. Perceptron Implementation_
- Random initialization of weights (w) and bias (b).
- Prediction rule:
_y=sign(w⋅x+b)_
- Updates applied via gradient descent when misclassification occurs.
- Tracked training and testing accuracies across epochs.

_3. Logistic Regression (sklearn)_
- Implemented as a baseline.
- Accuracy compared with the custom perceptron model.

**📊 Results**

_Learning Rate Experiments_
- Small learning rates → very slow convergence.
- Large learning rates → unstable updates, oscillating decision boundary.
- Moderate rates achieved smooth convergence.

_Epochs_
- Too few epochs → underfitting, poor accuracy.
- Sufficient epochs (~100) → good separation of classes.
- Very large epochs → no further improvements once convergence reached.

_Comparison_
- Sklearn’s perceptron achieved similar accuracy (within 1–2%) to the custom implementation.
- Logistic Regression generally performed slightly more consistently, given its probabilistic nature.
