# 🏃 LSTMs for Human Activity Recognition

![TensorFlow](https://img.shields.io/badge/TensorFlow-v1.0.0-orange)
![Python](https://img.shields.io/badge/Python-3.6%2B-blue)
![License](https://img.shields.io/badge/License-MIT-green)

## 📖 Overview
This project performs **Human Activity Recognition (HAR)** using the UCI Smartphone dataset and an **LSTM (Long Short-Term Memory)** Recurrent Neural Network (RNN).

The goal is to classify the type of movement into **six categories** based on sensor data (accelerometer and gyroscope):
1.  `WALKING`
2.  `WALKING_UPSTAIRS`
3.  `WALKING_DOWNSTAIRS`
4.  `SITTING`
5.  `STANDING`
6.  `LAYING`

Compared to classical approaches, using LSTMs requires **almost no feature engineering**. The raw data is fed directly into the neural network, which acts as a black box to model the problem.

## 📊 Dataset Details
The dataset used is the **UCI HAR Dataset**.
* **Input:** Sensor signals (accelerometer and gyroscope) from a smartphone attached to the waist.
* **Preprocessing:** Noise filters applied; sampled in fixed-width sliding windows of 2.56 sec (128 readings/window) with 50% overlap.
* **Filtering:** A Butterworth low-pass filter (0.3 Hz cutoff) was used to separate body acceleration from gravity.

> **Note:** This project uses the almost raw data (only gravity is filtered out).

## 🧠 Architecture
### What is an RNN?
A Recurrent Neural Network (RNN) processes sequences of data (time series). In this project, a **"many-to-one"** architecture is used:
* **Input:** Time series of feature vectors (one vector per time step).
* **Output:** A probability vector for classification.



[Image of Recurrent Neural Network architecture]


### What is an LSTM?
An LSTM (Long Short-Term Memory) is an improved RNN designed to avoid the vanishing gradient problem, making it easier to train on long sequences.

## 🛠️ Installation & Usage

### Prerequisites
* Python 3.x
* TensorFlow (v1.0.0 or compatible legacy versions)
* NumPy
* Scikit-learn
* Matplotlib
