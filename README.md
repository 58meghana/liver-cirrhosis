Here's a **short and neat `README.md`** file version of your project summary, tailored for clarity and GitHub friendliness:

---

# Liver Cirrhosis Stage Prediction

Predicting Stage 4 liver cirrhosis using clinical and demographic data from the Mayo Clinic PBC study.

## 🔍 Project Overview

This project uses machine learning to classify whether a patient is in **Stage 4 (severe)** cirrhosis based on clinical features. It includes:

* Data cleaning and preprocessing
* Exploratory Data Analysis (EDA)
* Model training (Logistic Regression & XGBoost)
* Model interpretation using SHAP
* Experimental survival analysis

## 📊 Dataset

* Source: Mayo Clinic Trial (1974–1984)
* 418 patients, 19 features
* Features include: age, sex, bilirubin, copper, albumin, prothrombin, etc.
* Target: Binary label — Stage 4 (1) vs. Stages 1–3 (0)

## 🛠️ Methods

### Preprocessing

* Missing values: Imputed (median for numerics, mode for categoricals)
* Encoding: Categorical to numeric (e.g., Sex, Drug)

### EDA

* Visualized distributions and relationships using Seaborn (countplots, kdeplots, regplots)

### Modeling

* **Logistic Regression**: Baseline (\~70.3% accuracy)
* **XGBoost Classifier**: Best model (\~76.1% accuracy, AUC = 0.74)
* Evaluation: Accuracy, Precision, Recall, F1, ROC-AUC

### Interpretation

* SHAP values used to identify key features:

  * 🟢 **Copper**, **Bilirubin**, **SGOT**, **Age**, **Prothrombin**, **Albumin**

## 🚀 How to Run

### Requirements

```bash
pip install numpy pandas matplotlib seaborn scikit-learn xgboost shap lifelines
```

### Instructions

1. Upload `cirrhosis.csv` to `/content/sample_data/` (for Google Colab)
2. Run all cells in the Colab notebook

## ⚠️ Known Issues

* **Survival analysis** section is incomplete due to dataframe modification. Reload original dataset before this step.

## 🔮 Future Work

* Complete survival modeling
* Hyperparameter tuning (e.g., GridSearchCV)
* Try other models (e.g., LightGBM, CatBoost)
* Feature engineering enhancements

---

Let me know if you’d like a version with badges, visuals, or links!
