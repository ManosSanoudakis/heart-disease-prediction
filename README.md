# Heart Disease Prediction using Machine Learning

## 📌 Project Overview
This project focuses on predicting the presence of heart disease using machine learning techniques and clinical patient data.
Multiple classification models were evaluated and compared using a rigorous and reproducible pipeline, with special emphasis on medical-appropriate evaluation metrics.

The final selected model is **Logistic Regression**, chosen based on both performance and interpretability.

## 📊 Dataset
- Samples: 1,025
- Features: 13 clinical attributes
- Target: Binary (0 = No disease, 1 = Disease)
- No missing values

## ⚙️ Methodology
- Train/Test split with stratification
- Stratified 5-fold cross-validation
- ROC-AUC as primary metric
- Hyperparameter tuning with GridSearchCV

## 🏆 Final Model
**Logistic Regression**
- Test ROC-AUC ≈ 0.88
- Recall (disease class) ≈ 0.82

## 💾 Model Saving
The final pipeline model is saved using joblib.

## 🧠 Key Takeaways
- Simple, interpretable models can outperform complex ones
- Proper evaluation matters more than model complexity

## 📌 Tools
Python, pandas, scikit-learn, matplotlib, seaborn