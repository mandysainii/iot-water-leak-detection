IoT Water Leak Detection System
Overview

This project implements a machine learning–based IoT solution for detecting water leakage events using sensor and infrastructure data. The objective is to minimize missed leaks in a safety-critical monitoring environment.

IoT Context

The system simulates a smart water infrastructure pipeline where pressure, flow rate, vibration, RPM, and operational metrics are continuously monitored. Machine learning models analyze this data to identify potential leak events and trigger alerts.

Models Implemented

Logistic Regression (baseline classification model)

LSTM (time-series deep learning model using rolling windows)

Class imbalance mitigation using balanced class weights

Methodological Considerations

Train/test split with stratification (logistic regression)

Time-aware split for sequence modeling (LSTM)

Feature scaling applied only on training data to prevent data leakage

Rolling window size of 60 time steps for temporal modeling

Recall used as primary evaluation metric due to safety-critical requirements

Key Findings

Logistic Regression achieved high recall (~0.91) for leak detection.

Unweighted LSTM collapsed to majority-class predictions.

Weighted LSTM improved recall (~0.27) but introduced substantial false positives.

Simpler linear models outperformed deep learning for this dataset.

Technologies

Python, scikit-learn, TensorFlow/Keras, NumPy, Pandas, Matplotlib, Seaborn
