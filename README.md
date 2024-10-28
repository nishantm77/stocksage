# Stock Price Prediction using Long-Short Term Memory (LSTM) Networks

## Description
This project aims to develop a robust stock price prediction model utilizing Long Short-Term Memory (LSTM) networks, a type of recurrent neural network (RNN) well-suited for time-series forecasting. The model leverages historical stock price data to identify patterns and trends, enabling it to predict future stock prices with improved accuracy.

### Key Features:
- **Data Collection**:
  The project fetches historical stock data from Yahoo Finance using the yfinance library, allowing for easy access to a wide range of stock tickers.
- **Data Preprocessing**:
  The data is preprocessed using Min-Max scaling to normalize the price values, ensuring that the LSTM model can learn effectively from the input data.
- **LSTM Model Architecture**:
  The model is built using Keras, featuring multiple LSTM layers with dropout regularization to prevent overfitting. The architecture is designed to capture long-term dependencies in the stock price data.
- **Training and Evaluation**:
  The model is trained on a portion of the historical data, with the remaining data reserved for testing. Performance metrics such as Mean Squared Error (MSE) and Mean Absolute Error (MAE) are used to evaluate the     model's accuracy.
- **Future Price Prediction**:
  After training, the model can predict future stock prices for a specified number of days, providing valuable insights for investors and traders.
- **Visualization**:
  The project includes visualizations that compare actual stock prices with predicted prices, helping to assess the model's performance visually.

### Technologies Used
- **Python (3.7 and above recommended)**
- **Libraries**: 
  - `NumPy`
  - `Pandas`
  - `yfinance`
  - `Scikit-learn`
  - `TensorFlow/Keras`
  - `Matplotlib`
## Usage Instructions
### 1. Prerequisites
- **Install Python**: If you haven't already, download and install Python from the official Python website.
- Use pip to install the necessary libraries. You can run the following command in your terminal:
```bash
pip install yfinance pandas scikit-learn tensorflow matplotlib
```
- Explanation of Libraries:
  - *yfinance*: Fetches historical stock data from Yahoo Finance.
  - *pandas*: Provides data structures and data analysis tools.
  - *scikit-learn*: Offers tools for data preprocessing and machine learning.
  - *TensorFlow/Keras*: Used for building and training neural networks, including LSTM models.
  - *matplotlib*: For creating visualizations of the data and predictions.


### 2. Code Overview
- The code consists of a **StockPredictor** class that handles the following tasks:

  - Fetching historical stock data from Yahoo Finance.
  - Preprocessing the data for LSTM training.
  - Building and training the LSTM model.
  - Making predictions for future stock prices.
  - Plotting the actual vs. predicted stock prices.
### 3. Setting-up the code
- **Download the Code**: Copy the provided code into a Python file, for example, stock_predictor.py.

- **Modify Parameters**: In the `main()` function, you can set the following parameters:

  - `ticker`: The stock symbol you want to predict (e.g., 'AAPL' for Apple Inc., 'NVDA' for NVIDIA).
  - `start_date`: The start date for fetching historical data (format: 'YYYY-MM-DD').
  - `end_date`: The end date for fetching historical data (you can use the current date).

```bash
ticker = 'AAPL'  # Stock symbol
start_date = '2023-01-01'  # Start date
end_date = datetime.now().strftime('%Y-%m-%d')  # Current date
```

### 4. Run the code

To run the code, navigate to the directory where your `stock_predictor.py` file is located and execute the following command in your terminal or command prompt:

```bash
python stock_predictor.py
```

### 5. Output

- The script will fetch the historical stock data for the specified ticker and date range.
- It will preprocess the data, train the LSTM model, and make predictions for the next 30 days.
- Finally, it will plot the actual stock prices against the predicted prices and print the predicted prices for the next 30 days in the console.

### 6. Customization

- You can customize the number of epochs and batch size in the `train_model` method to optimize the model's performance.
- Adjust the `sequence_length` parameter in the `prepare_data` method to change how many previous days are used to predict the next day's price.


## Conclusion

This guide provides a comprehensive overview of how to set up and use the stock price prediction code using LSTM in Python. Feel free to modify the parameters and experiment with different stocks to see how the model performs!


  
