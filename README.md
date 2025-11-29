# 📈 Stock Price Prediction using LSTM

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Deep Learning](https://img.shields.io/badge/Deep%20Learning-LSTM%20%2F%20TensorFlow-orange)
![License](https://img.shields.io/badge/License-MIT-green)

## 📖 Overview
This project is a machine learning application designed to predict future stock prices based on historical data. It utilizes **Long Short-Term Memory (LSTM)** networks, a type of Recurrent Neural Network (RNN) capable of learning long-term dependencies in time-series data.

## 📘 Theoretical Background

### 1. Time Series Analysis
Stock price prediction is a classic problem in **Time Series Analysis**. Unlike standard regression problems where data points are independent, stock prices are sequential—today's price is heavily influenced by yesterday's price and trends over the past weeks or months. To predict the future value, the model must understand the *temporal order* and dependencies in the historical data.

### 2. Recurrent Neural Networks (RNN)
Standard feedforward neural networks (like CNNs or MLPs) assume inputs are independent of each other. This limitation makes them poor candidates for stock prediction, where order matters.

**Recurrent Neural Networks (RNNs)** address this by having an internal "memory." In an RNN, the output from the previous step is fed back into the network as input for the current step. This allows the network to process sequences of inputs and maintain a "state" containing information about what it has seen so far.

However, standard RNNs suffer from the **Vanishing Gradient Problem**. As the sequence grows longer (e.g., looking back at 6 months of stock data), the gradients used to update the network weights become smaller and smaller, eventually becoming insignificant. This causes the network to "forget" earlier data points.

### 3. Long Short-Term Memory (LSTM)
**Long Short-Term Memory (LSTM)** networks are a specialized type of RNN designed specifically to solve the vanishing gradient problem. They are capable of learning long-term dependencies, making them ideal for financial forecasting where past trends influence future prices.

LSTMs achieve this using a complex internal structure called a **Cell State**, which runs through the entire chain with only minor linear interactions. The LSTM can add or remove information to the cell state using structures called **Gates**:

* **Forget Gate:** Decides what information from the previous state is no longer relevant (e.g., forgetting an old trend when the market regime changes).
* **Input Gate:** Decides what new information (current price) is important to store in the cell state.
* **Output Gate:** Decides what the next hidden state should be based on the current cell state.

By regulating the flow of information, LSTMs can distinguish between recent noise (daily volatility) and significant long-term trends (bull/bear markets).

## 🛠️ Technologies Used
* **Language:** Python
* **Deep Learning:** TensorFlow / Keras
* **Data Manipulation:** Pandas, NumPy
* **Visualization:** Matplotlib, Seaborn
* **Data Source:** Yahoo Finance (`yfinance`)

## 🚀 Installation & Setup

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/zerodha537/Stock_Prediction.git](https://github.com/zerodha537/Stock_Prediction.git)
    cd Stock_Prediction
    ```

2.  **Install dependencies:**
    ```bash
    pip install numpy pandas matplotlib tensorflow yfinance scikit-learn
    ```

3.  **Run the prediction script:**
    ```bash
    python main.py
    ```

## 📊 Results
*(Add your prediction charts here)*
The model output compares the **Actual Stock Price** vs. the **Predicted Stock Price** to visualize accuracy.

## 📝 License
This project is open-source and available under the MIT License.
