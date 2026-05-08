# Heart Disease Prediction

A machine learning project that predicts the presence of heart disease from clinical patient data. Built with a focus on evaluation metrics that actually matter in a medical context — not just accuracy.

---

## Why this project

Accuracy alone is a poor metric when the cost of a false negative is someone's life. This project explores how to build and evaluate classification models responsibly, prioritizing recall on the disease class and ROC-AUC over surface-level performance numbers.

---

## Dataset

- **1,025 patient records**, 13 clinical features
- Binary target: `0` = No disease, `1` = Disease present
- No missing values — minimal preprocessing required

Features include age, chest pain type, resting blood pressure, cholesterol, fasting blood sugar, and more.

---

## What's inside

- Data exploration and visualization
- Multiple classification models trained and compared
- Stratified 5-fold cross-validation throughout
- Hyperparameter tuning with `GridSearchCV`
- Final model exported as a reusable pipeline

---

## Results

The final model is **Logistic Regression** — chosen not just for performance, but because it's interpretable. In a medical setting, being able to explain *why* the model flagged a patient matters.

| Metric | Score |
|---|---|
| ROC-AUC | ~0.88 |
| Recall (disease class) | ~0.82 |

One of the more interesting findings: simpler models held their own against more complex ones. With a dataset of this size, regularization and proper evaluation mattered more than model choice.

---

## Getting started

**Clone the repo**
```bash
git clone https://github.com/your-username/heart-disease-prediction.git
cd heart-disease-prediction
```

**Install dependencies**
```bash
pip install -r requirements.txt
```

**Run the notebook**
```bash
jupyter notebook
```

---

## Requirements

```
pandas
numpy
matplotlib
seaborn
scikit-learn
joblib
```

Python 3.8+ recommended.

---

## Project structure

```
heart-disease-prediction/
│
├── data/                  # Dataset
├── notebooks/             # Main analysis notebook
├── models/                # Saved model pipeline (joblib)
├── requirements.txt
└── README.md
```

---

## Key takeaways

- Recall matters more than accuracy when false negatives are costly
- Cross-validation and proper stratification prevent misleadingly optimistic results
- Logistic Regression is still a strong baseline — and one you can actually explain
