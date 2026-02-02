# H1N1 and Seasonal Flu Vaccine Prediction

Predicting H1N1 and Seasonal Flu vaccine uptake using machine learning.

## 📊 Project Overview

This project uses a **MultiOutputClassifier with Logistic Regression** to predict:
- H1N1 vaccine uptake
- Seasonal flu vaccine uptake

## 📈 Model Performance

- **Overall AUC Score**: 0.8234
- **H1N1 Vaccine AUC**: 0.8156
- **Seasonal Vaccine AUC**: 0.8312

## 🔧 Model Details

- **Algorithm**: Logistic Regression (L2 regularization, C=1)
- **Features**: 36 numerical features
- **Preprocessing**: Median imputation + Standard scaling
- **Train/Test Split**: 67% train / 33% test (stratified)
- **Framework**: scikit-learn

## 📁 Files

- `complete_anaylsis.ipynb` - Full analysis and model training notebook
- `my_submission.csv` - Final predictions on test set
- `.gitignore` - Excludes large CSV data files

## 🎯 Top Predictive Features

1. h1n1_concern
2. h1n1_knowledge
3. opinion_h1n1_vacc_effective

## 🚀 Usage

```python
# Load the trained pipeline and make predictions
from sklearn.pipeline import Pipeline
import pandas as pd

# Load your data
X_test = pd.read_csv("test_set_features.csv", index_col="respondent_id")

# Predictions are in my_submission.csv
```

## 📝 Dataset

Data from [DrivenData](https://www.drivendata.org/) H1N1 and Seasonal Flu Vaccine Competition

## ✅ Next Steps

- [ ] Try gradient boosting models (XGBoost, LightGBM)
- [ ] Implement feature engineering
- [ ] Test different imputation strategies
- [ ] Hyperparameter tuning

---

**Author**: Data Analysis Team  
**Date**: February 2, 2026
