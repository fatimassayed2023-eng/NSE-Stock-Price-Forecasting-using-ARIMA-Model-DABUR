# Assignment Title: Stock Price Forecasting using ARIMA Model (NSE) 

---

## (1) Problem Statement

Stock market data is highly dynamic and influenced by various factors. Predicting future stock prices manually is difficult due to trends, seasonality, and randomness.

The problem is to analyze historical stock price data of an NSE-listed company and forecast future prices using time series analysis techniques such as the ARIMA model.

---

## (2) Objective

* To collect historical stock price data from NSE
* To preprocess and clean the dataset
* To analyze trends in stock prices
* To build a time series forecasting model using ARIMA
* To predict future stock prices
* To visualize historical and forecasted data

---

## (3) Dataset

* **Source:** NSE Historical Data (official NSE website)
* **Features:**

  * `Date` → Trading date
  * `Close Price` → Daily closing price
* **Size:**

  * Data collected for the past 1 year (approx. 250 trading days)

---

## (4) Methodology

### **1. Data Preprocessing**

* Converted `Date` column into datetime format
* Set date as index for time series analysis
* Handled missing values using forward fill / interpolation
* Sorted data chronologically

---

### **2. Exploratory Data Analysis (EDA)**

* Plotted closing price trend over time
* Observed upward/downward trends and volatility
* Checked for seasonality and patterns

---

### **3. ARIMA Model Implementation**

#### **(a) Stationarity Test (ADF Test)**

* Applied Augmented Dickey-Fuller (ADF) test
* If p-value > 0.05 → data is non-stationary
* Applied differencing to make data stationary

#### **(b) ACF & PACF Analysis**

* ACF plot used to determine MA(q) component
* PACF plot used to determine AR(p) component
* Identified optimal values of (p, d, q)

#### **(c) Model Training**

* Built ARIMA model using selected parameters
* Fitted model on training data
* Evaluated using residual analysis

---

### **4. Model Evaluation**

* Checked residual errors
* Verified no autocorrelation in residuals
* Compared predicted vs actual values

---

## (5) Results

* The ARIMA model successfully captured the trend in stock prices
* Stationarity was achieved after differencing
* The model showed good alignment with actual data

### **Insights:**

* Stock prices exhibit volatility but follow trends
* ARIMA can effectively model time series data
* Forecast accuracy depends on parameter tuning

---

## (6) Future Price Prediction

* Forecasted next **30 days closing prices** using ARIMA
* Combined historical and forecasted data in visualization

### Visualization:

<img width="986" height="528" alt="30 day Forecast" src="https://github.com/user-attachments/assets/b9364ecb-e3b2-4bd1-8a6c-a8f557a13b8e" />
<img width="1005" height="547" alt="DABUR price trend" src="https://github.com/user-attachments/assets/0dd347cb-73a2-49c4-a2ad-c9479a05e7b0" />
<img width="986" height="505" alt="forecast actual_Predicted" src="https://github.com/user-attachments/assets/2359fc1b-19e5-4d0b-b032-44315bf36cda" />




---

## (7) How to Run

### Step 1: Install dependencies

```bash id="j6g1az"
pip install pandas matplotlib statsmodels
```

### Step 2: Run the program

```bash id="g2n8rf"
python main.py
```

---

## (8) Conclusion

This project demonstrates the application of ARIMA for stock price forecasting. The model was able to capture trends and generate future predictions based on historical data.

Although stock prices are influenced by external factors, ARIMA provides a strong baseline model for time series forecasting.

---

## 📁 Project Structure

```id="q1bz0m"
project-folder/
│
├── data/
│   └── stock_data.csv
│
├── main.py
├── requirements.txt
└── README.md
```

---
