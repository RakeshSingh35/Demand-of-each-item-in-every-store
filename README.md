# 📦 Store Inventory Demand Forecasting

A machine learning and deep learning forecasting project designed to predict future inventory demand across multiple stores and products using grouped time series forecasting techniques.

The project analyzes historical sales data, identifies seasonal patterns and trends, and forecasts future demand to support inventory planning and stock optimization.

---

# 🎯 Project Objective

Accurate inventory forecasting helps businesses:

* Reduce stock shortages
* Minimize overstocking costs
* Improve supply chain planning
* Optimize warehouse utilization
* Support demand-driven decision making

This project forecasts future sales volume for every Store–Item combination using advanced time series forecasting models.

---

# 📊 Dataset Overview

The dataset contains historical daily sales transactions.

| Feature | Description                            |
| ------- | -------------------------------------- |
| date    | Date of sales transaction              |
| store   | Unique store identifier                |
| item    | Unique item identifier                 |
| sales   | Number of units sold (Target Variable) |

---

# 🧾 Dataset Characteristics

* Daily observations
* Multiple stores
* Multiple products
* Strong seasonal behavior
* Long-term upward growth trend
* Suitable for grouped/hierarchical forecasting

---

# 🔍 Exploratory Data Analysis

Several exploratory analyses were performed to understand demand patterns.

## Key Findings

### 📈 Trend

* Sales increase steadily over time.
* Every store exhibits long-term growth.

### 🔄 Seasonality

Two major seasonal patterns were identified:

* Weekly seasonality
* Yearly seasonality

### 🏪 Store Behavior

* Sales increase during the first half of the year.
* Sales gradually decline during the second half.

### 📦 Item Behavior

* Most products follow similar yearly seasonal cycles.
* Product demand increases year-over-year.

---

# 📊 Visualizations

## Monthly Sales Distribution

Shows monthly sales variability across all stores and products.

![Monthly Sales Distribution](images/monthly_sales_distribution.png)

---

## Median Sales Trend

Median sales demonstrate continuous annual growth.

![Median Sales Trend](images/Median_of_sales_for_all_stores_and_item.png)

---

## Monthly Sales Distribution by Item

Illustrates yearly seasonality and monthly demand fluctuations.

![Monthly Sales by Item](images/Boxplot_for_monthly_sales_for_each_item.png)

---

## Monthly Sales Distribution by Store

Highlights store-level seasonal demand patterns.

![Monthly Sales by Store](images/boxplot_for%20monthly_sales_for_each_store.png)

---

## Annual Sales Growth by Store and Item.

This chart illustrates the year‑over‑year growth of total sales for each item across all stores.
It demonstrates how sales volumes increase annually, making it easy to compare performance trends across products and locations.
Growth rates are calculated as the percentage change in total sales compared to the previous year.

![Total sales by Store and Item over the year](images/Total_sales_of_item_by_store_by_year.png)

---
## 📈 Half‑Yearly Sales Ratio Trend
This plot shows the sales ratio, calculated as the current value divided by the previous value, across half‑yearly periods.
It highlights growth patterns by comparing each period’s sales to the preceding one, making trends in store‑item performance easy to interpret.
![Sales_ratio : Current_values/Previous_value](images/Sales_ratio_trends_by_store_item.png)

---

## Half‑Yearly Percentage Change in Sales
This plot illustrates the percentage change in sales across half‑yearly periods.
It compares each period’s sales to the previous one, highlighting growth trends for items across different stores.
![Plot of percentqge of sales over a period of time ](images/Percentage_changs_sales_store_item.png)
---
## Seasonal Decomposition

Trend, seasonality, and residual components for Store–Item combinations.

![Seasonal Decomposition](images/seasonal_decomposition.png)

---

# ⚙️ Feature Engineering

The following preprocessing steps were applied:

* Date parsing
* Time series indexing
* Weekly and monthly date.
* Indian holidays addition
* Standardization / normalization
* Group-wise forecasting preparation
* Future covariate generation
* Multi-series transformation

---

# 🤖 Forecasting Models

Several forecasting frameworks were evaluated.

## Darts

Models evaluated:

* NHiTS
* NBEATS
* Deep Learning Forecasting Models

Framework:

* Darts
* PyTorch Lightning

---

## GluonTS

Models evaluated:

* DeepAR
* Probabilistic Forecasting Models
* DeepAR model with saftey stocks.

Framework:

* GluonTS

---

## NeuralForecast

Models evaluated:

* NHiTS
* NHITS Probabilistic Forecasting
* Deep Learning Forecasting Architectures

Framework:

* NeuralForecast

---

# 🧪 Validation Strategy

Training Period:

* Historical sales data

Forecast Horizon:

* Next 90 days (3 Months)

Evaluation Type:

* Forward Forecasting
* Hold-Out Validation

---

# 📏 Evaluation Metrics

Performance was measured using:

| Metric     | Description                                                             |
| ---------- | ------------------------------------------------------------------------|
| AVG RMSE   | Average Root Mean Squared Error of every store-item combination         |                 |
| AVF MAE    | Average Mean Absolute Error of every store-item combination             |
| AVG MAPE   | Average Mean Absolute Percentage Error of every store-item combination. |                                 |
| AVG R²     | Average Coefficient of Determination of every store-item combination.   |                                 |

---

# 📈 Model Performance

Average performance across all Store–Item series:

| Metric   | Value   |
| ---------| ------- |
| AVG RMSE | 7.793   |
| AVG MAE  | 6.195   |
| AVG MAPE | 13.086% |
| AVG R²   | 0.567   |

---

# 🔮 Forecast Results

## GluonTS Forecast

Historical sales and future inventory demand predictions.

![GluonTS Forecast](images/GluonTs_future_forecast.png)

---

## Darts Forecast

Forecast generated using Darts forecasting models.

![Darts Forecast](images/darts_future_forecast.png)

---

# 💡 Business Insights

The analysis reveals:

* Strong weekly demand cycles
* Strong yearly seasonality
* Consistent long-term growth
* Demand peaks during the first half of the year
* Forecasting can significantly improve inventory planning

---

# 📂 Project Structure

```text
Store_Inventory_Forecasting/
│
├── dataset/
│   ├── df.csv
│── analysis.ipynb
|── gluonts_inventory_colab.ipynb
|── neuralforecast.ipynb
|── NHITS_darts.ipynb
│
├── images/
│   ├── monthly_sales_distribution.png
│   ├── Median_of_sales_for_all_stores_and_item.png
│   ├── Boxplot_for_monthly_sales_for_each_item.png
│   ├── boxplot_for_monthly_sales_for_each_store.png
│   ├── growth_of_item_by_store_by_year.png
│   ├── seasonal_decomposition.png
│   ├── gluonts_inventory_prediction.png
│   └── darts_future_forecast.png
│
├── requirements.txt
├── README.md
└── src/
```

---

# 🛠 Installation

## Clone Repository

```bash
git clone https://github.com/RakeshSingh35/Demand-of-each-item-in-every-store.git

cd Demand-of-each-item-in-every-store
```

---

## Install Dependencies

```bash
pip install pandas
pip install numpy
pip install matplotlib
pip install seaborn
pip install scikit-learn
pip install pytorch-lightning
pip install darts
pip install gluonts
pip install neuralforecast
```

---

# 🐍 Python Compatibility

| Framework      | Python Version |
| -------------- | -------------- |
| GluonTS        | 3.10           |
| Darts          | 3.11           |
| NeuralForecast | 3.11           |

---

# 🚀 Future Improvements

Potential enhancements include:

* Hierarchical Forecasting
* Temporal Fusion Transformer (TFT)
* TimeGPT Integration
* Ensemble Forecasting
* Inventory Optimization Layer
* Automated Retraining Pipeline

---

# 📜 License

This project is released under the MIT License.

---

# 👤 Author

Rakesh Kumar Singh

Data Science | Machine Learning | Time Series Forecasting
