# 📦 Inventory Demand Forecasting

This project focuses on predicting the **daily sales demand** for items in a retail store using various regression algorithms. The main goal is to improve inventory planning and minimize overstock or stockout scenarios.

---

## 📁 Project Structure

InventoryDemandForecasting/
├── InventoryDemandProject.ipynb # Jupyter notebook with complete workflow
├── train.csv.zip # Historical sales data (used for training)
├── test.csv # Evaluation dataset
├── requirements.txt # Libraries used in this project
└── README.md # Project documentation


---

## 🚀 Project Objective

To accurately forecast the number of items sold per day for a given store and item, using historical sales data and machine learning models.

---

## 📊 Dataset Description

The dataset contains the following columns:

| Column | Description |
|--------|-------------|
| `date`  | Date of the sale |
| `store` | Store ID (1 to 10) |
| `item`  | Item ID (1 to 50) |
| `sales` | Number of items sold |

**Time Range:** 2013-01-01 to 2017-12-31  
**Prediction Target:** Daily sales (`sales`)

---

## 🛠️ Feature Engineering

Additional features derived from `date`:
- `year`, `month`, `day`
- `weekday`: Day of the week (0 = Monday)
- `weekend`: Binary indicator for weekends
- `holiday`: Binary indicator using Indian national holidays

---

## 🧠 Models Used

We experimented with the following regression models:

- `LinearRegression`
- `Ridge`, `Lasso`
- `DecisionTreeRegressor`
- `RandomForestRegressor`
- `ExtraTreesRegressor`
- `KNeighborsRegressor`
- `GradientBoostingRegressor`
- `XGBoostRegressor`

**Hyperparameter tuning** was done using `GridSearchCV`.

We also implemented **Quantile Regression** with Gradient Boosting to estimate prediction intervals.

---

## 🧪 Evaluation Metrics

- **R² Score** (Coefficient of Determination)
- **MAPE** (Mean Absolute Percentage Error)
- **Explained Variance**

Sample result with tuned `GradientBoostingRegressor`:

Training time: 0.16s
Prediction time: 0.01s
Explained variance: 0.518
MAPE: 19.7%
R2 Score: 0.359


---

## 📦 Requirements

Install all dependencies using:

```bash
pip install -r requirements.txt


