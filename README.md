# ❤️ Heart Disease Prediction — Machine Learning Project

This repository contains a complete, production‑ready machine learning project for predicting heart disease using clinical data.

## 📁 Project Structure
- `data/heart.csv` — dataset
- `notebooks/ml_project_clean.ipynb` — analysis & training notebook
- `models/best_model.pkl` — trained ML model
- `requirements.txt` — dependencies
- `.gitignore` — ignored files list

## 🔍 Overview
The project includes preprocessing, EDA, multiple model training, hyperparameter tuning, evaluation (accuracy, confusion matrix, ROC), and saving the best-performing model.

## 🚀 How to Use
### 1. Install dependencies
```
pip install -r requirements.txt
```

### 2. Open the notebook
```
jupyter notebook notebooks/ml_project_clean.ipynb
```

### 3. Load the trained model in Python
```python
import joblib
model = joblib.load("models/best_model.pkl")
```

## ⭐ Notes
This folder is GitHub‑ready. Extract it and push it with:

```
git add .
git commit -m "Upload heart disease ML project"
git push -u origin main
```
