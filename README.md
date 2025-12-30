
# 🏡 House Price Prediction Using Machine Learning

This repository contains the full, reproducible workflow for the Major Project **“House Price Prediction Using Machine Learning.”**
It uses the **Ames Housing Dataset** to build and evaluate regression models.

---

## 📂 Repository Structure

```
.
├── README.md
├── requirements.txt
├── LICENSE                  # optional (MIT)
├── .gitignore
├── .github/
│   └── workflows/
│       └── run-experiments.yml
│
├── src/
│   └── appendix_full_code.py
│
├── data/
│   └── appendix_ames_subset.csv
│
├── reports/                 # generated tables (metrics, stats, feature importances, splits)
└── images/                  # generated plots (heatmap, pairplot, importances, residuals, etc.)
```

---

## 🧠 Project Description

Models implemented:
- **Linear Regression**
- **Decision Tree Regressor**
- **Random Forest Regressor**

Evaluation metrics:
- **MAE**, **RMSE**, **R²**

Visualizations:
- Correlation heatmap, pairplot
- Random Forest feature importance
- Predicted vs Actual (for all models)
- Residual distribution (Linear Regression)

> Note: The repo uses a **small 15‑row subset** for fast demo runs (embedded in the script and also provided as `data/appendix_ames_subset.csv`). For stronger results, run models on the **full Ames dataset (~2,930 rows)**.

---

## 🧪 How to Reproduce Locally

1. Install dependencies:
```bash
pip install -r requirements.txt
```

2. Run the main script:
```bash
python src/appendix_full_code.py
```

Artifacts will be saved into:
- **reports/**: `appendix_metrics.csv`, `appendix_metrics.json`, `appendix_descriptive_stats.csv`, `appendix_feature_importance.csv`, `appendix_split_sizes.csv`, `appendix_tables.xlsx`
- **images/**: `appendix_corr_heatmap.png`, `appendix_pairplot.png`, `appendix_feature_importance.png`, `appendix_pred_vs_actual_*.png`, `appendix_residuals_linear.png`

---

## 🤖 Run in GitHub Actions (CI)

The workflow `.github/workflows/run-experiments.yml` automatically:
- sets up Python,
- installs requirements,
- runs `src/appendix_full_code.py`,
- uploads **tables** and **plots** as **GitHub Action artifacts**.

Check the **Actions** tab → latest run → **Artifacts** to download results.

---

## 📊 Data Sources & Documentation

- **AmesHousing (CRAN manual)**: official documentation of the 82 features.
  https://cran.r-project.org/web/packages/AmesHousing/AmesHousing.pdf
- **Raw CSV mirror** (community mirror of Ames data):
  https://github.com/wblakecannon/ames/blob/master/data/housing.csv

---

## 📜 Citation

If you use this repository, please cite:
> “House Price Prediction Using Machine Learning – Major Project (2025)”

Author: **Gitanjali Chavan**
