# Housing Price Prediction - Data Pipeline & Regression Model

[![Python](https://img.shields.io/badge/python-3.11+-blue.svg)](https://www.python.org)
[![XGBoost](https://img.shields.io/badge/XGBoost-Latest-green.svg)](https://xgboost.readthedocs.io/)

## 📝 Overview

Data engineering pipeline that loads, validates, and transforms real estate data, then predicts housing prices using XGBoost regression.

- **Dataset:** 1,460 houses × 81 features
- **Target:** Sale Price ($14K - $755K)
- **Model Performance:** RMSE $27,340 | Log-RMSE 0.1393

---

## 🎯 Key Features

✅ Load and explore real estate data (CSV)  
✅ Handle missing values and outliers  
✅ Feature engineering & log transformation  
✅ Train/validation split  
✅ XGBoost regression model  
✅ RMSE evaluation and predictions  

---

## 🛠️ Tech Stack

- **Python 3.11+** | Pandas | NumPy
- **Visualization:** Matplotlib, Seaborn
- **ML:** Scikit-learn, XGBoost
- **Development:** Jupyter Notebook

---

## 📦 Installation

```bash
# Clone repo
git clone https://github.com/your-username/housing-price-pipeline.git
cd housing-price-pipeline

# Create virtual environment
python -m venv venv
source venv/bin/activate

# Install dependencies
pip install pandas numpy matplotlib seaborn scikit-learn xgboost jupyter

# Download data
# Kaggle: Home Data for ML Course
# Place train.csv and test.csv in /data/raw/
```

---

## 🚀 Usage

```bash
jupyter notebook Regression.ipynb
```

**Pipeline Steps:**
1. Load training & test data
2. Exploratory Data Analysis (distributions, correlations)
3. Handle missing values & scale features
4. Apply log transformation to target variable (SalePrice)
5. Train XGBoost model with validation set
6. Convert predictions back to real prices
7. Evaluate with RMSE

---

## 📊 Results

| Metric | Value |
|--------|-------|
| Training Records | 1,170 |
| Validation Records | 290 |
| **RMSE (Real Prices)** | $27,340 |
| **RMSE (Log Scale)** | 0.1393 |

**Interpretation:** On average, predictions are off by ~$27K (±9% for $300K house)

---

## 📁 Project Structure

```
housing-price-pipeline/
├── Regression.ipynb          # Main notebook
├── README.md
├── requirements.txt
└── data/
    ├── raw/
    │   ├── train.csv
    │   └── test.csv

```

---

## 🔑 Data Transformations

- **Log Transformation:** y = log1p(SalePrice) → normalizes skewed distribution
- **Missing Values:** Imputation strategy based on feature importance
- **Feature Scaling:** Standardization for model stability
- **Train/Val Split:** Stratified 80/20 split

---

## 📚 Kaggle Dataset

Source: [Home Data for ML Course](https://www.kaggle.com/competitions/home-data-for-ml-course/data)

---

**Author:** Ramiro Pérez | [GitHub](https://github.com/pfcperez)  
**Status:** ✅ Complete
