# Store Inventory demand forecasting project

## 🪸 Overview

The dataset is related to store inventory demand forecasting, specifically for tracking the number of items sold at different stores on specific dates.



---

## 🌊 Introduction

This file contains historical data used for training machine learning models to forecast store inventory demand.
Data Fields:
date: The date of the sale data. It represents the specific date when the sales occurred.
store: A unique identifier or ID for each store. This helps in distinguishing between different store locations.
item: A unique identifier or ID for each item that is sold in the stores.
sales: The number of items sold at a particular store on a specific date. This is the target variable for the forecasting task, which you aim to predict for future dates.

---

## 🧭 Data Description

### 📘 1. Store Inventory demand forecasting project
- date: The date of the sale data. It represents the specific date when the sales occurred.
- store: A unique identifier or ID for each store. This helps in distinguishing between different store locations.
- item: A unique identifier or ID for each item that is sold in the stores.
- sales: The number of items sold at a particular store on a specific date. This is the target variable for the forecasting task, - - which you aim to predict for future dates.

### 🧹 2. Data Cleaning & Transformation
- Standardized variables

---

## 📊 Exploratory Data Analysis

Key insights:
- Every Store has an upward trend.
- Yearly and Weekly seasonality exists for every Store.

---

## 🎨 Visualization
- Montly sales distribution of all stores and item over a month.
![Boxplot displaying monthly sales distribution across all stores and items, showing median, quartiles, and outlier values for each month](images/monthly_sales_distribution.png)
- Median sales of items has been increasing every year.
![Line chart showing median sales across all stores and items over multiple years, demonstrating upward trend in sales growth annually](images/Median_of_sales_for_all_stores_and_item.png)

- There is yearly seasonality that exists in the sales with outliers every month.
- Median sales on rises for first six months then it it decline till the end of year.
![Boxplot comparing monthly sales for each item, displaying higher median values in first six months that decline toward year end with scattered outliers throughout](images/Boxplot_for_monthly_sales_for_each_item.png)

- Median sales of each store rises during first six months then it declines for next six months.
![Boxplot showing monthly sales patterns for each store, with peak median sales in the first half of the year gradually declining through the second half](images/boxplot_for%20monthly_sales_for_each_store.png)

- Sales rate of every item on each store has been rising by yearly.
![Growth visualization comparing sales rates of items across stores by year, showing consistent upward trajectory year over year](images/growth_of_item_by_store_by_year.png)

- Seasonal decomposition of every item by each store indicate a rising trend, yearly seasonality and residual that exists.
![Seasonal decomposition chart breaking down sales data by store and item into trend component showing upward growth, seasonal component displaying yearly cyclical pattern, and residual component showing remaining variations](images/seasonal_decomposition.png)

---


---

## 🤖 Modeling

- **Techniques:** Grouped time series forecasting model for mulitple stores and items.
- NHiTSModel, GluonTs, Time series probblistic modeling, neuralforecast.
- **Feature Engineering:** Standardised data for modeling.
- **Validation:**Prediction of 3 months of stock in the future.
- **Metrics:** MAE, R square, Root mean squared error, MAPE, SMPE. 

---

## 📈 Results & Discussion

- Stores have weekly and yearly seasonality.
- It has upward trend.
- Metrics: Average metrics of all stores.
  RMSE: 7.793
  MAE: 6.195
  MAPE: 13.086
  rsq: 0.567

# Forecasting visual 
GluonTs models inventory prediction
![Time series forecast chart from GluonTs model showing inventory predictions with blue bars representing historical sales data from 2013 to 2017 and red bars highlighting the 3-month forecasted period, demonstrating strong weekly and yearly seasonal patterns](images/gluonts_inventory_prediction.png)

Darts models inventory prediction
![Time series forecast chart from Darts model displaying inventory predictions with blue area representing historical sales data spanning multiple years and red area indicating the forecasted future period, showing consistent seasonal fluctuations and overall upward trend](images/darts_future_forecast.png)
---

## ⚙️ Installation & Requirements

**Dependencies:**

pip install pandas numpy matplotlib seaborn darts, pytorch_lightning, GluonTs, neuralforecast.
Python version for gluonTs 3.10
python version for darts and neuralforecast 3.11
