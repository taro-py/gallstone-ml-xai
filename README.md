# gallstone-ml-xai  
Explainable Machine Learning for Gallstone Disease with tabular DataType  

Project structure:  

```
gallstone-ml-xai/
├── dataset/
│   ├── dataset-uci.xlsx
│   ├── best_model.joblib
│   └── scaler.joblib
├── code/
│   ├── eda_and_models.ipynb
│   └── 02_shap_xai_analysis.ipynb
├── figures/
│   ├── shap_*.png, lime_*.png, ranking_comparison.png, body_composition_correlation.png
│   └── feature_ranking_comparison.csv
├── report/
│   ├── report.tex
│   └── ieee_report.pdf
├── presentation/
│   └── presentation.pptx
├── requirements.txt
├── .gitignore
└── README.md
```

How to run:

1. Create an environment with Python 3.12 and install the dependencies: `pip install -r requirements.txt`
2. Open the notebooks from the `code/` folder and run `eda_and_models.ipynb` first, then `02_shap_xai_analysis.ipynb`.
