# Heart Disease Prediction

Accuracy is a comfortable metric until you remember what a false negative means here: someone goes home thinking they're fine. This project is built around that problem. When the cost of being wrong isn't symmetric, you stop optimizing for accuracy and start caring about recall and AUC.

## Dataset

[Heart Disease UCI - Kaggle](https://www.kaggle.com/datasets/johnsmith88/heart-disease-dataset). 1,025 patient records, 13 clinical features, no missing values. Binary target: disease present or not. Clean data meant I could focus entirely on modeling.

## Results

Three classifiers trained and compared with stratified 5-fold cross-validation and `GridSearchCV` tuning throughout: Logistic Regression, Random Forest, and SVC. All pipelines used `class_weight="balanced"` to handle the medical cost of missing a positive case, and `RobustScaler` for the models that needed it.

The final model is Logistic Regression. Not because it scored highest on paper, but because in a medical context you need to be able to explain why the model flagged someone. A black box that's 2% more accurate isn't a good trade.

| Metric | Score |
|---|---|
| ROC-AUC | ~0.88 |
| Recall (disease class) | ~0.82 |

With a dataset this size, regularization and proper cross-validation mattered more than which model I picked. The complexity ceiling hits fast at 1k rows.

## Setup

```bash
git clone https://github.com/your-username/heart-disease-prediction.git
cd heart-disease-prediction
pip install -r requirements.txt
jupyter notebook
```

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

## Structure

```
heart-disease-prediction/
├── data/
├── notebooks/
├── models/
├── requirements.txt
└── README.md
```
