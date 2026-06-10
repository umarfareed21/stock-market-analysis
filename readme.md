# 📈 Stock Market Data Pipeline and Analysis Using Python

## Overview

This project analyzes the last 30 days of stock market data for three major Canadian banks:

- Royal Bank of Canada (RY)
- Toronto-Dominion Bank (TD)
- Bank of Nova Scotia (BNS)

Using Python and financial data from Yahoo Finance, the project performs data collection, preprocessing, statistical analysis, and visualization to identify market trends and stock performance.

---

## Objectives

- Download stock market data using Yahoo Finance API.
- Analyze historical stock prices.
- Calculate 7-Day Rolling Averages.
- Calculate Daily Percentage Changes.
- Detect significant price drops greater than 2%.
- Visualize stock performance using professional charts.
- Generate a report for further analysis.

---

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- yfinance
- Jupyter Notebook

---

## Project Workflow

### 1. Data Collection

Stock data is downloaded directly from Yahoo Finance using the yfinance library.

Stocks analyzed:

- RY
- TD
- BNS

---

### 2. Data Preparation

The project extracts adjusted closing prices and checks for missing values before performing analysis.

---

### 3. Rolling Average Analysis

A 7-Day Rolling Average is calculated to smooth short-term fluctuations and identify underlying trends.

Formula:

Rolling Average = Average of Previous 7 Trading Days

---

### 4. Daily Return Analysis

Daily percentage returns are calculated to measure day-to-day stock performance.

Formula:
$$
\text{Daily Return} = \frac{\text{Current Price} - \text{Previous Price}}{\text{Previous Price}}
$$

---

### 5. Risk Detection

The project flags trading days where the stock price decreases by more than 2%.

Condition:

Daily Return < -2%

---

## Visualizations

### Closing Price vs 7-Day Rolling Average

Shows stock price trends and smoothed market movement.
![Rolling Average](visualizations/stock_performance/RY_performance.png)
![Rolling Average](visualizations/stock_performance/TD_performance.png)
![Rolling Average](visualizations/stock_performance/BNS_performance.png)

---

### Daily Return Distribution

Displays the frequency and distribution of daily returns.

![Daily Return Distribution](visualizations\ry_daily_return_distribution.png)
![Daily Return Distribution](visualizations\td_daily_return_distribution.png)
![Daily Return Distribution](visualizations\bns_daily_return_distribution.png)

---

### Correlation Heatmap

Measures the relationship between stock prices.

Correlation Values:

- +1 → Strong Positive Relationship
- 0 → No Relationship
- -1 → Strong Negative Relationship

![Correlation Heatmap](visualizations/correlation_heatmap.png)

---

### Daily Percentage Change

Tracks daily stock returns and market volatility.

---

### Box Plot of Returns

Highlights:

- Median Returns
- Volatility
- Outliers
- Distribution Spread

![Box Plot](visualizations/boxplot.png)

---

### Pairwise Relationship Analysis

Explores relationships among stock returns using scatter plots and distributions.

![pairwise Relationship Charts](visualizations/pair_charts.png)
---

## Project Structure

```text
stock-market-data-pipeline-analysis/
│
├── stock_analysis.ipynb
├── README.md
├── requirements.txt
├── stock_report.csv
│
└── visualizations/
    ├── stock_performance/
    │   ├── BNS_performance.png
    │   ├── RY_performance.png
    │   └── TD_performance.png
    │
    ├── bns_daily_return_distribution.png
    ├── boxplot.png
    ├── correlation_heatmap.png
    ├── daily_percentage_change.png
    ├── pair_charts.png
    ├── ry_daily_return_distribution.png
    └── td_daily_return_distribution.png
  
 ```

---

## Installation

Clone the repository:

```bash
git clone https://github.com/yourusername/stock-market-data-pipeline-analysis.git
```

Install required packages:

```bash
pip install -r requirements.txt
```

---

## Required Libraries

```bash
pip install pandas
pip install yfinance
pip install matplotlib
pip install seaborn
```

---

## Running the Project

Open the notebook:

```bash
jupyter notebook
```

Run:

```text
stock_analysis.ipynb
```

---

## Sample Output

The project generates:

- Stock Performance Charts
- Rolling Average Analysis
- Daily Return Analysis
- Correlation Matrix
- Risk Detection Flags
- CSV Report
---
## Key Insights

- All three Canadian bank stocks (RY, TD, and BNS) showed an overall upward trend during the 30-day analysis period, as indicated by both closing prices and 7-day rolling averages.

- The 7-day rolling averages smoothed short-term fluctuations and confirmed a consistent positive trend across all three stocks.

- Correlation analysis revealed a very strong positive relationship among the stocks:
  - BNS and TD: 0.97
  - RY and TD: 0.96
  - BNS and RY: 0.94

  This suggests that the three banking stocks tend to move in the same direction and are influenced by similar market factors.

- Daily returns for all stocks were generally concentrated around zero, indicating relatively stable day-to-day price movements.

- The box plot analysis showed similar return distributions across the three stocks, suggesting comparable levels of short-term volatility.

- TD exhibited the largest positive daily return (approximately 3.2%) and also experienced the largest negative daily return (approximately -2.5%), making it the most volatile stock among the three during the analysis period.

- The risk detection system identified one trading day where TD declined by more than 2%, while RY and BNS did not trigger any risk flags during the observation period.

- Pairwise relationship analysis further confirmed strong positive associations between stock returns, reinforcing the correlation heatmap findings.

- Overall, the selected banking stocks demonstrated strong co-movement, moderate volatility, and positive short-term performance throughout the analysis period.


---

## Author

**Mohammad Umar Fareed**



