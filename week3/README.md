# Shopify Stock Market Analysis

## 📌 Project Overview

This project analyzes **Shopify stock market data** using Python and Pandas. The analysis focuses on stock prices, trading volume, daily price changes, returns, and unusual trading-volume days.

The dataset contains historical Shopify stock information including **Open, High, Low, Close, Adjusted Close, Volume, and Date**.

## 📂 Dataset

**File:** `shopify_stock.csv`

The dataset contains **2,469 records** and the following columns:

* `date` – Trading date
* `open` – Opening stock price
* `high` – Highest price during the trading day
* `low` – Lowest price during the trading day
* `close` – Closing stock price
* `adj_close` – Adjusted closing price
* `volume` – Number of shares traded

## 🛠️ Technologies Used

* Python
* NumPy
* Pandas
* Matplotlib
* Jupyter Notebook

## 🔍 Analysis Performed

### 1. Data Loading

The Shopify stock dataset is loaded using Pandas.

```python
df = pd.read_csv("shopify_stock.csv")
```

### 2. Data Exploration

The project examines:

* Dataset shape
* Column information
* Statistical summary
* First few records
* Data types

### 3. Data Preprocessing

The following preprocessing steps were performed:

* Converted the `date` column into datetime format
* Checked for missing values
* Removed missing records
* Checked for duplicate records
* Removed duplicate records
* Sorted the data according to date

### 4. Daily Price Change

A new column called `Daily_delta` is created to calculate the difference between the closing and opening prices.

```python
df["Daily_delta"] = df["close"] - df["open"]
```

### 5. Daily Return

A `Daily_Return` column is created to analyze the percentage return based on opening and closing prices.

```python
df["Daily_Return"] = (df["close"] - df["open"] / df["open"]) * 100
```

### 6. Trading Volume Analysis

The project calculates:

* Average trading volume
* Maximum trading volume
* Minimum trading volume

An anomaly threshold is also calculated as twice the average trading volume.

```python
threshold = 2 * average_volume
```

Trading days where the volume exceeds this threshold are identified as **anomalous trading days**.

### 7. Statistical Analysis

The project calculates statistical measures for daily returns:

* Mean
* Variance
* Standard deviation

These measures help understand the general behavior and variability of Shopify's daily stock returns.

## 📊 Key Analysis Areas

The project focuses on:

* Shopify stock price movement
* Opening vs. closing prices
* Daily price changes
* Daily returns
* Trading volume
* High-volume/anomalous trading days
* Return variability

## 📁 Project Structure

```text
Shopify-Stock-Analysis/
│
├── Shopify_task.ipynb
├── shopify_stock.csv
└── README.md
```

## ▶️ How to Run

1. Clone or download this repository.
2. Make sure Python is installed.
3. Install the required libraries:

```bash
pip install numpy pandas matplotlib jupyter
```

4. Place `Shopify_task.ipynb` and `shopify_stock.csv` in the same folder.
5. Open the notebook using Jupyter:

```bash
jupyter notebook
```

6. Run the notebook cells sequentially.

## 🎯 Objective

The main objective of this project is to understand and analyze historical Shopify stock data using **Python-based data analysis techniques**, while identifying price movements, returns, trading-volume patterns, and anomalous trading days.

## 👩‍💻 Author

**Pradeepa D**

BCA Student
Kamaraj College, Thoothukudi
