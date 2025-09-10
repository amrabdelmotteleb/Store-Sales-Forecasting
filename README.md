# Store Sales – Time Series Forecasting (ARIMA Approach)

This repository contains an ARIMA-based solution for the [Kaggle Store Sales – Time Series Forecasting competition](https://www.kaggle.com/c/store-sales-time-series-forecasting).  
The goal of the competition is to forecast daily sales for different product families across multiple stores.  

This notebook was originally published within a blog post by the **Warwick Data Science Society** around 4 years ago.

---

## Approach

The notebook [`blog_notebook.ipynb`](./blog_notebook.ipynb) demonstrates the process of building and evaluating an **ARIMA model** on the sales time series of a specific product family (**BREAD/BAKERY**) in **store 44**.

---

## Key Steps

### 1. Data Selection & Preparation
- Filtered the training dataset to include sales for one store–family pair.  
- Split the data into a training set and a test set (last 16 days reserved for testing).  
- Visualized both sets for exploratory analysis.  

### 2. Stationarity Check
- Plotted the raw series and observed non-stationarity.  
- Conducted an **ADF (Augmented Dickey-Fuller) test**, confirming non-stationarity (`p-value > 0.05`).  
- Applied differencing (first-order differencing made the series stationary).  

### 3. Model Identification
- Inspected **ACF** and **PACF** plots to determine AR (`p`) and MA (`q`) terms.  
- Selected an ARIMA configuration based on observed patterns.  

### 4. Model Training & Evaluation
- Fitted the ARIMA model on the training set.  
- Generated forecasts for the test period (16 days).  
- Compared predictions against actual sales to assess performance.  

---
