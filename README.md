# 📈 TATA Global Stock Price Prediction using LSTM

This project builds a deep learning model to predict the stock prices of **TATA Global Beverages Ltd** using **LSTM (Long Short-Term Memory)** neural networks, a type of Recurrent Neural Network (RNN) ideal for time series data.

## 🎯 Objective

- Predict future stock prices based on historical stock market data.
- Visualize and compare the real vs. predicted stock prices.

## 📚 Dataset

- **Training Data**: `NSE-TATAGLOBAL.csv`
- **Testing Data**: `tatatest.csv`
- **Features Used**: Mainly the `Open` stock price.

## 🛠️ Project Workflow

1. **Data Loading**:
   - Load the stock price datasets using pandas.
   - Focus on the 'Open' column for modeling.

2. **Data Preprocessing**:
   - Perform **MinMax Scaling** (Normalization) to scale stock prices between 0 and 1.
   - Create sequences of 60 time steps to predict the next stock price.

3. **Building the LSTM Model**:
   - Stack **4 LSTM layers** with **Dropout** to prevent overfitting.
   - Add a final **Dense layer** for output.
   - Compile the model using **Adam optimizer** and **Mean Squared Error** loss.

4. **Training the Model**:
   - Train the model over 100 epochs with a batch size of 32.

5. **Making Predictions**:
   - Predict stock prices on the test set.
   - Perform inverse scaling to get stock prices back to original scale.

6. **Visualization**:
   - Plot real vs predicted stock prices for comparison.

## 🚀 How to Run

1. Install the necessary libraries:

```bash
pip install numpy pandas matplotlib tensorflow scikit-learn
