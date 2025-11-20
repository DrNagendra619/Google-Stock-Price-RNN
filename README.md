# Google-Stock-Price-RNN
Google Stock Price RNN
# Google Stock Price Prediction using Recurrent Neural Networks (RNN) 📈💻

## Overview

This repository contains a Jupyter Notebook that utilizes a **Recurrent Neural Network (RNN)**, specifically likely an **LSTM (Long Short-Term Memory) model**, to forecast the future stock prices of **Google (GOOG or GOOGL)**. Time series forecasting is a classic application of deep learning, where the model learns temporal dependencies from historical market data.

The project demonstrates a complete deep learning workflow tailored for financial data:
1.  **Data Preprocessing:** Scaling and windowing time series data.
2.  **Model Building:** Designing an LSTM network architecture.
3.  **Prediction:** Generating forecasts for future stock prices.
4.  **Evaluation:** Comparing predicted prices against actual prices.

---

## Repository Files

| File Name | Description |
| :--- | :--- |
| `Google_Stock_Price_RNN.ipynb` | The main Jupyter notebook detailing the data preparation, RNN/LSTM architecture, training process, and visualization of the prediction results. |
| `[STOCK_DATA_FILE].csv` | *Placeholder for the historical Google stock price dataset used in the notebook (e.g., historical GOOGL data).* |

---

## Technical Stack

The project relies on specialized deep learning and data science libraries in Python:

* **Deep Learning Frameworks:** `TensorFlow` or `Keras` (for building and training the RNN/LSTM model).
* **Data Handling:** `pandas`, `numpy` (essential for manipulating time series data and preparing sequences).
* **Visualization:** `matplotlib` (for plotting historical prices vs. predicted prices).
* **Preprocessing:** `MinMaxScaler` (from `sklearn.preprocessing`) for normalizing the price data.
* **Environment:** Jupyter Notebook

---

## Methodology (RNN/LSTM)

### 1. Data Preparation
* **Feature Selection:** Typically uses the **'Open'** or **'Close'** price as the primary feature for prediction.
* **Scaling:** Data is scaled (e.g., between 0 and 1) to improve the stability and performance of the RNN.
* **Sequence Creation:** The key step involves creating time steps (or windows) where the input (X) is the stock price over the last *N* days, and the output (Y) is the stock price on day *N+1*.

### 2. LSTM Model
The LSTM network is chosen because of its ability to remember information over long sequences, making it particularly effective for capturing long-term trends in financial time series data.

### 3. Evaluation

Model performance is evaluated by plotting the predicted prices against the true prices on a separate test or validation set. The main metric used is typically the **Root Mean Squared Error (RMSE)** or **Mean Squared Error (MSE)**, which quantifies the average magnitude of the error.

---

## Setup and Usage

To run this analysis locally, ensure you have Python installed and follow these steps:

1.  **Clone the repository:**
    ```bash
    git clone [Your Repository URL]
    cd [Your Repository Name]
    ```

2.  **Ensure the Data is Present:**
    Place your historical stock data file (`[STOCK_DATA_FILE].csv`) in the repository's root directory.

3.  **Install dependencies:**
    ```bash
    pip install pandas numpy matplotlib tensorflow keras scikit-learn jupyter
    ```

4.  **Launch Jupyter:**
    ```bash
    jupyter notebook
    ```
    Open the `Google_Stock_Price_RNN.ipynb` file and execute the cells sequentially to train the model and see the forecasting results.
