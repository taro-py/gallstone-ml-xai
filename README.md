# Gallstone ML-XAI

**Explainable Machine Learning for Gallstone Disease using Tabular Data**

## Overview

An end-to-end tabular data analysis and Machine Learning project focused on identifying patterns associated with Gallstone Disease using the UCI Gallstone-1 dataset (319 patients, 38 features).

The project covers data ingestion, exploratory data analysis, data preprocessing, classification model development, evaluation and Explainable AI (XAI).

## Technical Workflow

**1. Data Analysis & Preparation**
- Excel data ingestion and validation using Pandas.
- Exploratory Data Analysis (EDA): distributions, 11 boxplots and Pearson correlation analysis.
- Feature inspection, target encoding and data preparation.
- Continuous and binary feature identification.

**2. Data Processing & Machine Learning**
- Feature preprocessing using `ColumnTransformer` and `StandardScaler`.
- Scikit-learn pipelines combining preprocessing and classification.
- Stratified train/test splitting and 5-Fold Cross-Validation.
- Training and comparison of Logistic Regression, Random Forest, SVM and XGBoost.
- Holdout evaluation using classification metrics and confusion matrices.

**3. Explainable AI**
- SHAP and LIME for model interpretability.
- Global feature importance and local prediction explanations.
- Feature ranking and correlation comparisons.

## Project Structure

```text
gallstone-ml-xai/
├── dataset/
│   ├── dataset-uci.xlsx
│   ├── best_model.joblib
│   └── scaler.joblib
├── code/
│   ├── eda_and_models.ipynb
│   └── 02_shap_xai_analysis.ipynb
├── figures/
│   ├── shap_*.png
│   ├── lime_*.png
│   ├── ranking_comparison.png
│   ├── body_composition_correlation.png
│   └── feature_ranking_comparison.csv
├── report/
│   ├── report.tex
│   └── ieee_report.pdf
├── presentation/
│   └── presentation.pptx
├── plan.md
├── requirements.txt
├── .gitignore
└── README.md
```

## How to Run

1. Create a Python 3.12 environment.
2. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

3. Open the notebooks inside `code/`.
4. Run `eda_and_models.ipynb` first to perform data analysis, preprocessing, model training and evaluation.
5. Run `02_shap_xai_analysis.ipynb` to perform the explainability analysis using SHAP and LIME.

## Technologies

Python · Pandas · NumPy · Matplotlib · Seaborn · Scikit-learn · XGBoost · SHAP · LIME · Joblib · Jupyter Notebook

## Limitations

The dataset contains only 319 patients. Evaluation is limited to internal cross-validation and a holdout test set, without external validation. Model explanations do not establish causality or clinical validity.

## Documentation

See `report/ieee_report.pdf` for the detailed methodology, experimental results and conclusions.
