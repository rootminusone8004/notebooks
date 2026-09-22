# Machine Learning Curriculum Notebooks

Welcome to the Machine Learning course repository! This repository contains a structured, modular series of interactive Jupyter notebooks (`.ipynb`) designed to take students from numerical foundations to applied machine learning modeling and deployment.

---

## Curriculum Structure

Each module is organized into its own numbered folder and contains progressively challenging notebooks:

```text
notebooks/
├── README.md
├── 01_numpy/                 # Numerical computing, vectorization, and linear algebra (5 notebooks)
├── 02_pandas/                # Tabular data manipulation, cleaning, and feature engineering (6 notebooks)
├── 03_matplotlib/            # Publication-grade plotting and ML diagnostic visualizations (4 notebooks)
├── 04_seaborn/               # Statistical data visualization and Exploratory Data Analysis (4 notebooks)
└── 05_scikit_learn/          # Supervised & unsupervised machine learning algorithms and pipelines (5 notebooks)
```

---

## Prerequisites & Environment Setup

To run these notebooks locally or in an interactive environment (such as VS Code, JupyterLab, or Google Colab), install the required dependencies:

```bash
pip install numpy pandas matplotlib seaborn scikit-learn scipy joblib jupyter
```

---

## Module Directory & Curriculum Map

| Module | Directory | Status | Notebooks Count | Description |
|---|---|---|---|---|
| **01** | [`01_numpy/`](./01_numpy/) | ✅ Complete | 5 Notebooks | Array creation, multidimensional slicing, broadcasting rules, linear algebra, and ML algorithms from scratch. |
| **02** | [`02_pandas/`](./02_pandas/) | ✅ Complete | 6 Notebooks | Series, DataFrames, data cleaning, groupby aggregations, timeseries, and feature engineering for ML. |
| **03** | [`03_matplotlib/`](./03_matplotlib/) | ✅ Complete | 4 Notebooks | Object-Oriented interface, core statistical plots, multi-panel `GridSpec` dashboards, and diagnostic ML curves. |
| **04** | [`04_seaborn/`](./04_seaborn/) | ✅ Complete | 4 Notebooks | Statistical distributions, multivariate relational plots, masked correlation heatmaps, and 5-step EDA workflow. |
| **05** | [`05_scikit_learn/`](./05_scikit_learn/) | ✅ Complete | 5 Notebooks | Preprocessing pipelines, regularized regression, classification, clustering/PCA, and hyperparameter tuning. |

---

## Pedagogical Design

Every notebook follows a 4-step learning path:
1. **Learning Objectives**: Clear milestones for what students will master.
2. **Conceptual Foundations**: Theory, mathematical formulations, and visual intuition.
3. **Worked Examples**: Fully commented code demonstrating practical ML patterns and edge cases.
4. **Common Pitfalls & Best Practices**: Crucial debugging tips (e.g., views vs copies, dummy variable trap, data leakage).
