# Final Project - Team 7 Analysis

## Overview

This notebook analyzes financial datasets of various companies, focusing on stock performance metrics like trading volume, daily price spreads, and trends over time. The primary objective is to preprocess and visualize data, identify anomalies, and extract actionable insights.

## Workflow & Methodology 
1. Data Preparation

•	Objective: Ensure datasets are consistent and ready for analysis.
   
•	Steps:
	1.	Loaded all CSV files from the ./ProjectDatasets/Team_7 directory using Python.
	2.	Extracted company names from file names and appended them as a new column (Company).
	3.	Parsed the Date column to ensure accurate time-series analysis.
	4.	Added checks for missing values in critical columns (Open, High, Low, Close, Adj Close, Volume).
	5.	Interpolated missing values using forward and backward filling to maintain data integrity.
    
2. Analysis

1. Rolling Medians:
	•	Applied to stock prices to smooth short-term fluctuations and highlight overall trends.
2. Outlier Detection:
	•	Identified anomalies in the Volume column using thresholds based on statistical deviations.
3. Key Metrics:
   Average Daily Spread:
	•	Calculated as the difference between High and Low prices, highlighting price volatility.

3.  Visualization

The notebook includes the following visualizations:

	1.	Rolling Median Graphs:
	   •	Display smooth trends in stock prices, helping identify long-term patterns.
	2.	Volume Trends:
	   •	Highlight significant spikes and outliers in trading volumes for each company.
	3.	Comparative Bar Charts:
	   •	Show average daily spreads across all companies to highlight comparative volatility.


## Key Findings

  1.	Data Completeness:
	   •	Missing values for Close and Adj Close prices were filled using interpolation, ensuring no data gaps for analysis.
	2.	Trading Volume Anomalies:
	   •	Detected significant spikes in trading volume, notably for BRK-A and MCD, suggesting potential unusual trading activity.
	3.	Volatility:
	   •	BRK-A exhibited the highest daily spread, reflecting extreme price fluctuations compared to other companies.
	4.	Trends:
	   •	Rolling median graphs revealed consistent long-term trends and highlighted anomalies for certain companies.

## Challenges Faced

  1.	Missing Data:
	   •	Addressed using forward and backward filling methods to interpolate missing values.
	2.	Outlier Detection:
	   •	Managing extreme outliers in trading volume required setting appropriate thresholds.
	3.	Deprecated Functions:
	   •	Encountered warnings for deprecated functions like fillna(method='bfill'), which will need updates in the future.

## Visualization Examples
	•	Rolling Median of Stock Prices:
	   •	Example graph showcasing smoothed trends for BRK-A.
	•	Trading Volume Outliers:
	   •	Volume spikes highlighted with annotations for companies like MCD and DPZ.
	•	Comparative Bar Chart:
	   •	Average daily price spreads for all companies, comparing relative volatility.

## Authors :

**Randolph**, **Sergio**, **Alex**, **Konstantinos**, **Aditi**
