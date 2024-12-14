# Final Project - Team 7 Analysis

## Overview
This project focuses on analyzing the stock performance of multiple companies using historical trading data. The notebook processes datasets to uncover trends, detect anomalies, and calculate key financial metrics. The primary aim is to deliver actionable insights through robust data analysis and visualization.

---

## Objectives
- Organize and preprocess financial datasets for effective analysis.
- Detect outliers in trading volumes and handle missing data in stock prices.
- Analyze and calculate key financial metrics like daily price spreads and rolling medians.
- Visualize stock trends and anomalies to communicate insights effectively.

---

## Dataset Description
### Source
The datasets consist of CSV files stored in the directory.

### Fields in Each Dataset:
- `Date`: The trading date.
- `Open`: Stock opening price.
- `High`: Highest stock price during the day.
- `Low`: Lowest stock price during the day.
- `Close`: Closing stock price.
- `Adj Close`: Adjusted closing price (accounts for splits/dividends).
- `Volume`: Number of shares traded.
- `Company`: Identifier derived from the filename during preprocessing.

---

## Workflow and Methodology

### **1. Data Preparation**
- Iteratively loaded CSV files into Pandas DataFrames.
- Added a `Company` column by extracting filenames.
- Parsed the `Date` column to enable time-series analysis.
- Addressed missing values in key fields (`Close`, `Adj Close`, `Volume`) using forward and backward filling.

### **2. Exploratory Data Analysis (EDA)**
- **Rolling Medians**:
  - Calculated for stock prices to smooth fluctuations and identify long-term trends.
- **Outlier Detection**:
  - Anomalies in trading volumes were flagged using statistical thresholds.
- **Average Daily Spread**:
  - Calculated as the difference between daily `High` and `Low` prices.

### **3. Visualization**
- Rolling Median Graphs: Highlight smoothed stock price trends.
- Volume Trend Graphs: Showcase spikes and outliers in trading volumes.
- Comparative Bar Charts: Present average daily spreads across companies.

---

## Key Findings
1. **Data Completeness**:
   - Missing values in `Close` and `Adj Close` columns were interpolated successfully.
2. **Volume Anomalies**:
   - Detected significant outliers in trading volumes for BRK-A and MCD.
3. **Volatility**:
   - BRK-A exhibited the highest average daily spread (1730.32), while WEN had the lowest (0.35).
4. **Trends**:
   - Rolling median graphs revealed consistent trends and isolated anomalies for individual companies.

---

## Challenges
1. **Missing Data**:
   - Required careful interpolation to ensure consistent analysis.
2. **Outlier Detection**:
   - Managing extreme anomalies in trading volumes required dynamic thresholds.
3. **Deprecated Methods**:
   - Encountered warnings due to deprecated functionality, such as `fillna(method='bfill')`.

---


### Outputs
- Rolling median graphs for stock prices.
- Volume trend graphs highlighting outliers.
- Summary metrics, including average daily spreads.

---

## Key Metrics
### Outliers in Trading Volumes
- **BRK-A**: 485 outliers (highest).
- **MCD**: 946 outliers detected.

### Average Daily Spreads (High-Low):
- **BRK-A**: 1730.32 (highest volatility).
- **WEN**: 0.35 (lowest volatility).
- Other companies: Spread ranged between 0.54 and 3.74.

---

## Visualization Examples
1. **Rolling Median Graph**:
   - Shows smoothed stock price trends for BRK-A.
2. **Volume Trend Graph**:
   - Highlights spikes and anomalies in trading volume.
3. **Comparative Bar Chart**:
   - Visualizes average daily spreads across all analyzed companies.

---



## Authors :

**Randolph**, **Sergio**, **Alex**, **Konstantinos**, **Aditi**
