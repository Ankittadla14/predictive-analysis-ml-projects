# Predictive Analysis — ML Projects (Coursework)

End‑to‑end mini‑projects from my **Predictive Analysis** course, consolidated into a single repository. 
Covers **data preprocessing**, **classification (KNN)**, and **regression** with **linear models** and a simple **MLP (neural network)**, including proper evaluation and comparison.

## 📂 Repository Structure
```
predictive-analysis-ml-projects/
├─ notebooks/
│  ├─ 01_data_preprocessing.ipynb      # from Homework 2
│  ├─ 02_classification_knn.ipynb      # from Homework 4
│  └─ 03_regression_models.ipynb       # from Homework 5
├─ data/                                # optional: small sample datasets only
├─ README.md
├─ requirements.txt
└─ .gitignore
```
> ⚠️ **Note:** Do not commit large datasets. Add only a small *sample* to `data/` and link the full dataset externally (Drive/Dropbox/etc.).

## 🧠 Topics Covered
- **Data Cleaning & Preprocessing:** missing values, encoding categoricals (one‑hot), scaling/normalization, leakage‑safe splits
- **Classification:** k‑Nearest Neighbors (distance metrics, `k`, and weights)
- **Regression:** Linear Regression, KNN Regression, MLPRegressor (feed‑forward neural net)
- **Model Evaluation:**
  - Classification: accuracy, confusion matrix, precision/recall/F1 (macro/weighted)
  - Regression: MAE, RMSE, R²; cross‑validation for robustness
- **Best Practices:** pipelines (`ColumnTransformer` + `Pipeline`), train‑only fitting of scalers/encoders, hyperparameter tuning with `GridSearchCV`

## 🚀 Quickstart
1) **Clone** the repo and create an environment:
```bash
git clone https://github.com/<your-username>/predictive-analysis-ml-projects.git
cd predictive-analysis-ml-projects
python -m venv .venv
# Windows: .venv\Scripts\activate
# macOS/Linux: source .venv/bin/activate
pip install -r requirements.txt
```

2) **Datasets**
- Put small sample files in `data/` (kept under version control).
- Store large/original datasets outside Git and link to them in this README.
- If a notebook expects a specific path, update the path cell to target your local copy in `data/`.

3) **Run the notebooks**
- Open Jupyter or VS Code, then run:
```bash
python -m ipykernel install --user --name=pa-ml-env
jupyter notebook  # or "jupyter lab"
```
- Execute cells top‑to‑bottom. Set `random_state=42` for reproducibility where applicable.

## 📒 Notebook Guide
- **01_data_preprocessing.ipynb** (from HW2)
  - EDA snapshots; imputation strategies; encoding; scaling; train/test split; data card summary.
- **02_classification_knn.ipynb** (from HW4)
  - Distance‑based KNN classifier; CV grid for `n_neighbors`, `weights`, `p`; confusion matrix & classification report.
- **03_regression_models.ipynb** (from HW5)
  - Linear baseline vs KNN vs MLPRegressor; `ColumnTransformer` pipelines; MAE/RMSE/R² + 5‑fold CV.

## ✅ Results (fill after running)
| Task | Best Model | Key Params | Metric(s) |
|------|------------|------------|-----------|
| Classification | e.g., KNN | k=7, weights=distance | Accuracy=…, F1(macro)=… |
| Regression | e.g., MLP | layers=(64,32), alpha=1e‑4 | RMSE=…, MAE=…, R²=… |

> Tip: Save figures/tables to `notebooks/figures/` and link them here.

## 🛡️ Reproducibility & Hygiene
- Use **pipelines** to avoid data leakage.
- Keep **random seeds** fixed for splits and model training (`random_state=42`).
- Track environment with `pip freeze > requirements-lock.txt` (optional).

## 📎 Data Policy
- Respect dataset licenses. Do **not** push proprietary or personal data.
- For >25–100 MB files, use external storage and link them here.

## 📜 License
This repository is intended for educational demonstration. Add a LICENSE if you plan to reuse code in other projects.
