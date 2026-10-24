# SVM Heart Disease Classifier

A small learning project: a support vector machine that classifies heart disease from 11 clinical features, built with scikit-learn in one notebook.

![Python](https://img.shields.io/badge/Python-3-blue) ![scikit-learn](https://img.shields.io/badge/scikit--learn-SVC-orange)

## Overview

`heart.csv` has 918 patients and 11 features (age, sex, chest pain type, resting blood pressure, cholesterol, fasting blood sugar, resting ECG, max heart rate, exercise angina, ST depression, ST slope). 508 patients (55%) are labelled with heart disease. The notebook explores the data, one-hot encodes the categorical columns, standardises the features, and trains an RBF-kernel SVM. For a screening task, missed patients (false negatives) matter more than overall accuracy, so recall on the disease class is the main number below.

## Results

Default `SVC()` on a single held-out test split of 184 patients (107 with disease, 77 without):

| Metric (disease class) | Value |
|---|---|
| Recall | 0.897 (96 of 107 found, 11 missed) |
| Precision | 0.914 |
| F1 | 0.906 |
| Accuracy (both classes) | 0.891 |

These come from one 80/20 split with no confidence interval, so treat them as a rough estimate. A grid search over `C`, `gamma` and kernel (best CV accuracy 0.871) did not help: the tuned model scored 0.875 accuracy and 0.88 disease recall on the same test split, below the default model.

## How it works

1. Load `heart.csv` and explore distributions and correlations.
2. One-hot encode the 5 categorical columns (20 input features after encoding).
3. 80/20 train/test split (`random_state=42`), `StandardScaler` fit on the training set only.
4. Train `SVC()` with default settings, then a `GridSearchCV` over `C`, `gamma` and `kernel`.

## Repository layout

```
.
├── model.ipynb   # analysis and model, outputs saved
└── heart.csv     # 918 rows, 12 columns
```

## Run it

There is no `requirements.txt`. Install the libraries the notebook imports:

```bash
pip install numpy pandas matplotlib seaborn scikit-learn jupyterlab
jupyter lab model.ipynb
```

## Limitations and next steps

- 172 rows have `Cholesterol = 0`, which is a missing value, not a real reading. The notebook does not treat it as missing.
- Results rest on one 184-patient test split. Stratified cross-validation with per-fold recall would give a more reliable estimate.
- The ROC cell uses hard class predictions instead of SVM scores, so its "ROC AUC" output is not a real AUC. The confusion-matrix print cell also mislabels true positives and true negatives; the classification report above is the correct source.
- No threshold tuning: for screening, the decision threshold should be set to reach a target recall.

---

Built by Rayan Saleh Al-Dwlah · [LinkedIn](https://www.linkedin.com/in/rayanaldwlah)
