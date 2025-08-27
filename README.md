# 📊 Predictive Analysis — Data Preprocessing, KNN & Regression

## 1. Introduction
This repository consolidates mini-projects from my **Predictive Analysis coursework**.  
It demonstrates the end-to-end **machine learning pipeline** on structured/tabular data:
1. **Data Preprocessing** (cleaning, encoding, scaling)  
2. **Classification** using **k-Nearest Neighbors (KNN)**  
3. **Regression** with **Linear Regression, KNN Regression, and MLP Neural Networks**

The goal is to highlight best practices in preparing real-world datasets, comparing classical ML algorithms, and evaluating model performance.

---

## 2. Repository Structure
```
.
├── notebooks/
│   ├── 01_data_preprocessing.ipynb    # Data cleaning, encoding, scaling
│   ├── 02_classification_knn.ipynb    # KNN classifier for categorical targets
│   └── 03_regression_models.ipynb     # Linear, KNN, and MLP regression
├── data/
│   └── README.md                      # Placeholder (store small samples only)
├── requirements.txt                   # Python dependencies
├── .gitignore                         # Ignore large/unnecessary files
└── README.md                          # Project documentation
```

---

## 3. Datasets
- Coursework datasets (e.g., **Car attributes, Pricing, Fuel Type**).  
- Full datasets are not committed to GitHub due to size restrictions.  
### How to Set Up:  
#### 1. Create a data/ folder in the repo root:
  ```bash
  mkdir -p data
  ```
#### 2. Place the dataset files inside ./data/ .
- For example:
  ```bash
  ./data/car_data.csv
  ./data/price_data.csv
  ```
#### 3. Update the dataset path in the notebooks if needed.
- Example:
  ```bash
  df = pd.read_csv("data/car_data.csv")
  ```
- Keep large/original files outside Git and update paths in the notebooks accordingly.

---

## 4. Methods

### 4.1 Data Preprocessing (`01_data_preprocessing.ipynb`)
- Missing value imputation (numeric = median, categorical = most-frequent).  
- Encoding of categorical features (one-hot).  
- Scaling of numeric features (standardization/normalization).  
- Train/test split for leakage-free evaluation.  

### 4.2 Classification (`02_classification_knn.ipynb`)
- **KNN Classifier** with hyperparameter tuning (`k`, distance metric, weights).  
- Model evaluation with **confusion matrix, accuracy, precision, recall, F1**.  

### 4.3 Regression (`03_regression_models.ipynb`)
- **Linear Regression** as baseline.  
- **KNN Regression** with grid search over neighbors/weights.  
- **MLP Regressor (Neural Net)** with hidden layers, regularization, early stopping.  
- Evaluation using **MAE, RMSE, R²**, plus **cross-validation**.

---

## 5. Reproducibility

### 5.1 Setup
```bash
python -m venv .venv
# Windows: .venv\Scripts\activate
# macOS/Linux: source .venv/bin/activate

pip install -r requirements.txt
```

### 5.2 Run Notebooks
```bash
jupyter notebook
# or
jupyter lab
```
Execute cells top-to-bottom. Adjust dataset paths in the `data/` folder as needed.

---

## 6. Files & Artifacts
- **`01_data_preprocessing.ipynb`**: EDA, cleaning, pipelines.  
- **`02_classification_knn.ipynb`**: Classifier training + metrics.  
- **`03_regression_models.ipynb`**: Regression models + evaluation.  
- **`requirements.txt`**: Core Python dependencies.  
- **`.gitignore`**: Prevents committing large/unnecessary files.  
- **`data/README.md`**: Placeholder instructions for dataset handling.  

---

## 7. Requirements
Core libraries:
- **numpy, pandas, scikit-learn, matplotlib, jupyter**

(see `requirements.txt` for full list)

---

## 8. License
Open-source for educational use.  

---

## 9. Acknowledgments
- University at Buffalo — *Predictive Analysis course*  
- Scikit-learn documentation for ML implementations  
