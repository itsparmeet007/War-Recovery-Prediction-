# 🌍 Comparative War Impact Forecasting & Recovery Score Prediction

> **Matrix Algebra Analysis of Ukraine-Russia vs Israel-Palestine Conflicts**  
> Manav Rachna International Institute of Research and Studies

---

## 📌 Project Overview

This project builds a complete **Machine Learning framework** to predict war recovery scores across two simultaneous geopolitical conflicts — **Ukraine-Russia** and **Israel-Palestine** — using real daily socioeconomic, military, and humanitarian data.

The core idea: can a model trained on one conflict **predict recovery in a completely different war?**  
**Answer: Yes — 80.18% accuracy.** ✅

---

## 🏆 Key Results

| Metric | Result |
|--------|--------|
| 🎯 Best Model | Random Forest |
| 📈 R² Score | **95.59%** |
| 📉 MAE | **1.87** |
| 🔁 Cross-Conflict Accuracy | **80.18%** (target was 72%) |
| 🧩 PCA Components | 10 (retaining 95% variance) |
| 📊 Dataset Size | 4,022 daily observations |

---

## 📁 Project Structure

```
War-Impact-Forecasting-ML/
│
├── 📓 MCFD2.ipynb                  ← Complete notebook (all 6 phases)
├── 📊 dual_conflict_dataset.csv    ← Raw dataset
├── 📊 cleaned_dataset.csv          ← Cleaned dataset (Phase 1 output)
├── 📄 README.md                    ← You are here
└── 📁 figures/                     ← All visualizations
    ├── boxplot_recovery.png
    ├── recovery_over_time.png
    ├── correlation_bar.png
    ├── scree_plot.png
    ├── pca_biplot.png
    ├── model_comparison.png
    ├── shap_summary.png
    └── confusion_matrix.png
```

---

## 🔬 Research Pipeline — 6 Phases

```
Phase 1 → Data Cleaning
          Stratified median imputation | Negative value clipping | 4022 rows

Phase 2 → Exploratory Data Analysis
          Recovery score trends | Correlation analysis | Country comparison

Phase 3 → PCA & Matrix Algebra
          Covariance matrix | Eigendecomposition | 19 → 10 components

Phase 4 → Machine Learning Models
          Linear Regression | XGBoost | SVR | Random Forest → R²=95.59%

Phase 5 → SHAP Explainability
          PC6 identified as primary driver (Food Price + Infrastructure)

Phase 6 → Cross-Conflict Generalization
          Train on Ukraine-Russia → Test on Israel-Palestine → 80.18%
```

---

## 📊 Dataset

- **Countries:** Ukraine, Russia, Palestine, Israel
- **Date Range:** January 2021 – December 2024
- **Observations:** 4,022 daily records
- **Features:** 24 original → 19 numeric → 10 PCA components

**Feature Categories:**

| Category | Features |
|----------|----------|
| 📈 Economic | GDP, Inflation, Unemployment, Food & Energy Price Index |
| ⚔️ Military | Death Toll, Casualties, Explosive Incidents, Conflict Area |
| 🏚️ Humanitarian | Internal Displacement, External Refugees, Infrastructure Damage |
| 🤝 Aid | Humanitarian Aid, Foreign Military Aid |
| 🎯 Target | Recovery Score (0–100) |

---

## 🧮 Mathematical Framework

**Standardization:**
```
X_scaled = StandardScaler().fit_transform(X)   # shape: (4022, 19)
```

**Covariance Matrix:**
```
C = (1 / n-1) × XᵀX                           # shape: (19, 19)
```

**PCA Eigendecomposition:**
```
C = QΛQᵀ
n_components_95 = 10                           # 95% variance retained
```

---

## 🤖 Model Comparison

| Model | MAE | RMSE | R² |
|-------|-----|------|----|
| Linear Regression | 3.31 | 4.25 | 87.35% |
| XGBoost Default | 2.04 | 2.90 | 94.09% |
| XGBoost Tuned | 1.96 | 2.65 | 95.06% |
| SVR (RBF) | 2.04 | 2.63 | 95.14% |
| **Random Forest ⭐** | **1.87** | **2.51** | **95.59%** |

---

## 🔁 Cross-Conflict Generalization

| Class | Precision | Recall | F1 |
|-------|-----------|--------|----|
| High Recovery | 0.72 | 1.00 ✅ | 0.83 |
| Low Recovery | 1.00 ✅ | 0.60 | 0.75 |
| **Overall** | — | — | **80.18%** |

> Model trained **only on Ukraine-Russia** data correctly predicts **Israel-Palestine** recovery 80% of the time — proving universal conflict recovery patterns exist.

---

## 💡 Key Finding

**PC6 = Food Price Index + Infrastructure Destruction** is the single most important driver of war recovery.

> 📌 Policy Implication: Humanitarian organizations should prioritize **food security AND infrastructure reconstruction simultaneously** — not as separate priorities.

---

## 🛠️ Tech Stack

```python
Python 3.x
├── pandas          # Data manipulation
├── numpy           # Matrix algebra
├── matplotlib      # Visualization
├── seaborn         # Statistical plots
├── scikit-learn    # PCA, ML models, metrics
├── xgboost         # Gradient boosting
└── shap            # Explainability
```

---

## 🚀 How to Run

```bash
# Clone the repository
git clone https://github.com/YOUR_USERNAME/War-Impact-Forecasting-ML.git

# Install dependencies
pip install pandas numpy matplotlib seaborn scikit-learn xgboost shap

# Open the notebook
jupyter notebook MCFD2.ipynb
```

---

## 👤 Author

**Parmeet Singh**  
Manav Rachna International Institute of Research and Studies  
Faridabad, Haryana — 121004

---

## 📄 Paper

> *Comparative War Impact Forecasting & Recovery Score Prediction: Matrix Algebra Analysis of Ukraine-Russia vs Israel-Palestine Conflicts*  
> Submitted for Conference Publication — 2025

---

## ⭐ If this helped you

Give it a **star** ⭐ and share it — this is open research for humanitarian purposes.
