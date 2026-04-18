# 📈 Apple Stock Price Prediction using Deep Learning (RNN & LSTM)

## 🚀 Project Overview

This project focuses on predicting Apple stock prices using deep learning techniques. Since stock prices are sequential in nature, Recurrent Neural Networks (RNN) and Long Short-Term Memory (LSTM) models were implemented to capture temporal dependencies.

The models were trained to perform both **single-step (1-day)** and **multi-step (5-day, 10-day)** forecasting using historical stock data.

---

## 🎯 Objectives

* Predict Apple stock prices using historical data
* Implement **SimpleRNN** and **LSTM** models
* Perform:

  * 1-day prediction
  * 5-day prediction
  * 10-day prediction
* Compare model performance using evaluation metrics

---

## 📊 Dataset

* Historical Apple stock data (`AAPL.csv`)
* Features:

  * Date
  * Open, High, Low, Close
  * Adj Close (Target Variable)
  * Volume

👉 **Why Adj Close?**
Adjusted Close reflects the true stock value after accounting for dividends and stock splits.

---

## 🧹 Data Preprocessing

* Converted `Date` column to datetime format
* Set `Date` as index (time-series structure)
* Handled missing values (forward fill)
* Selected **Adj Close** for modeling
* Applied **MinMax Scaling** (0–1 normalization)
* Created sequences:

  * Input: past 60 days
  * Output: 1, 5, or 10 future values

---

## 🧠 Model Architecture

### 🔹 SimpleRNN

* Captures short-term dependencies
* Architecture:

  * SimpleRNN (50 units)
  * Dropout (0.2)
  * Dense output layer

---

### 🔹 LSTM

* Captures long-term dependencies using memory cells
* Architecture:

  * LSTM (50 units)
  * Dropout (0.2)
  * Dense output layer

---

## ⚙️ Training Details

* Loss Function: Mean Squared Error (MSE)
* Optimizer: Adam
* Epochs: 10
* Batch Size: 32

---

## 🔍 Key Insights

* LSTM outperformed SimpleRNN due to its ability to capture long-term dependencies.
* Multi-step forecasting is more challenging due to error accumulation.
* Model performance may vary slightly due to randomness and data patterns.

---

## ⚡ Challenges Faced

* Handling time-series data correctly
* Managing shape transformations for multi-step outputs
* Ensuring proper scaling and inverse scaling
* Understanding multi-output predictions

---

## 🔧 Hyperparameter Tuning

GridSearchCV is not efficient for deep learning models like RNN/LSTM.
Instead, manual tuning was performed.

👉 Future improvement:

* Use **Keras Tuner** for optimizing:

  * Number of units
  * Dropout rate
  * Learning rate

---

## 💼 Business Use Cases

* 📊 Algorithmic trading strategies
* 📉 Risk management & portfolio optimization
* 📅 Financial forecasting
* 🏦 Investment decision support

---

## 🚀 Future Improvements

* Add technical indicators (RSI, MACD, Moving Averages)
* Incorporate news sentiment analysis
* Use advanced models (GRU, Transformers)
* Perform hyperparameter tuning with Keras Tuner

---

## 🛠️ Tech Stack

* Python 🐍
* Pandas, NumPy
* Matplotlib
* Scikit-learn
* TensorFlow / Keras

---

## 🙌 Conclusion

This project demonstrates how deep learning models can effectively capture patterns in time-series data. LSTM proved to be more powerful than SimpleRNN for stock price prediction due to its ability to retain long-term dependencies.

---

## 👩‍💻 Author

**Sanju Sarvashni**

---

⭐ If you found this project useful, consider giving it a star!
