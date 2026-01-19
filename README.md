# Inventory Demand Forecasting Using Machine Learning

This project implements an end-to-end **inventory demand forecasting system** using supervised machine learning regression techniques.  
The objective is to predict **monthly sales quantity for product–store (SKU) combinations** using historical inventory, sales, purchase, and vendor data.

The system compares multiple regression models and identifies the best-performing algorithm for real-world retail inventory planning.

---

## 📌 Problem Statement

Given historical inventory, sales, purchase, and vendor data for a multi-store retail chain, build a machine learning model to accurately forecast **next-month sales demand** for each product-store combination.

The model must:
- Capture non-linear demand patterns
- Generalize to unseen product–store–month combinations
- Minimize prediction error (MAE, RMSE)
- Achieve strong explanatory power (R²)
- Support model comparison for production deployment

---

## 🎯 Objectives

- Build a complete data preprocessing and feature engineering pipeline
- Engineer time-series and domain-specific inventory features
- Train and evaluate multiple regression models
- Compare models using cross-validation
- Select the best-performing model for demand forecasting
- Generate production-ready predictions for inventory planning

---

## 🧠 Key Concepts & Techniques

- Supervised Regression Learning
- Time-Series Feature Engineering (lags, rolling statistics)
- Feature Scaling and Categorical Encoding
- K-Fold Cross-Validation
- Ensemble Learning (Random Forest, Extra Trees, XGBoost, LightGBM)
- Model Evaluation using MAE, RMSE, and R²

---

## 📊 Dataset Overview

- **Domain:** Retail Inventory Management
- **Time Period:** January 2016 – December 2016
- **Granularity:** Monthly, product–store (SKU) level
- **Unique SKUs:** 16,932
- **Raw Records:** ~24.6 million transactions

### Data Sources
- Beginning & Ending Inventory Records
- Daily Sales Transactions
- Purchase Orders & Receiving Data
- Vendor Invoices and Lead Times

---

## 🛠️ Feature Engineering

### Numerical Features
- Historical sales (lagged 1, 2, 3, 6 months)
- Rolling means and standard deviations (3 & 6 months)
- Purchase price, freight, landed cost
- Profit per unit
- Lead time
- Beginning & ending inventory
- Month and year indicators

### Categorical Features
- Brand
- Store
- Vendor
- Product size

---

## 🤖 Models Implemented

- Linear Regression
- Ridge Regression
- Lasso Regression
- Decision Tree Regressor
- Random Forest Regressor
- Extra Trees Regressor
- K-Nearest Neighbors
- XGBoost Regressor
- LightGBM Regressor

---

## 📈 Model Performance Summary

### Best Performing Model (Test Set)
- **Model:** XGBoost
- **R²:** 0.8928
- **MAE:** 27.89
- **RMSE:** 96.94

Tree-based ensemble models consistently outperformed linear models, demonstrating strong capability in capturing complex demand patterns.

---

## 🔁 Workflow Overview

1. Load and consolidate multiple raw CSV datasets
2. Clean and standardize inventory and sales data
3. Aggregate daily data to monthly level
4. Engineer time-series and domain-specific features
5. Apply scaling and encoding pipelines
6. Train multiple regression models
7. Perform 5-fold cross-validation
8. Compare models and select best performer
9. Generate and export demand forecasts

---

## ▶️ How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/inventory-demand-forecasting.git
