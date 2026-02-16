IoT Water Leak Detection System
Project Overview

This project implements a machine learning-based IoT application for detecting water leakage events using sensor and location data. The system compares a logistic regression baseline with a deep learning LSTM model to evaluate the impact of temporal modeling.

Methods Used

Logistic Regression (baseline classification)

LSTM (time-series modeling with rolling windows)

Class imbalance handling (balanced weights)

Time-aware train/test splitting

Feature scaling without data leakage

Key Findings

Logistic Regression achieved high recall (~0.91) for leak detection.

Unweighted LSTM collapsed to majority-class predictions.

Weighted LSTM improved recall (~0.27) but introduced many false positives.

Simpler linear models outperformed deep learning for this dataset.

Technologies

Python

scikit-learn

TensorFlow / Keras

NumPy / Pandas

Matplotlib / Seaborn
