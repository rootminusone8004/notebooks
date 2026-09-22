# Module 05: Scikit-Learn for Machine Learning

This module teaches students modern supervised and unsupervised machine learning algorithms, leak-free pipeline design, rigorous validation strategies, and production hyperparameter tuning using Scikit-Learn.

---

## Notebook Overview & Difficulty Progression

| # | Notebook | Difficulty | Description & Key Topics |
|---|---|---|---|
| **01** | [`01_preprocessing_and_pipeline_design.ipynb`](./01_preprocessing_and_pipeline_design.ipynb) | 🟢 Beginner | Estimators, Transformers, Predictors, stratified `train_test_split()`, numerical scalers (`StandardScaler`, `RobustScaler`), `OneHotEncoder`, `ColumnTransformer`, and leak-free **`Pipeline`** design. |
| **02** | [`02_supervised_regression_models.ipynb`](./02_supervised_regression_models.ipynb) | 🟡 Intermediate | Ordinary Least Squares vs **Ridge ($L_2$)** shrinkage and **Lasso ($L_1$)** automated feature selection, ElasticNet, regression metrics (RMSE, MAE, $R^2$), and **Residual Diagnostics**. |
| **03** | [`03_supervised_classification_models.ipynb`](./03_supervised_classification_models.ipynb) | 🟡 Intermediate | Logistic Regression, Random Forest Ensembles, handling **Imbalanced Data (`class_weight='balanced'`)**, Confusion Matrix diagnostics, Precision/Recall trade-offs, and **ROC-AUC curves**. |
| **04** | [`04_unsupervised_clustering_and_pca.ipynb`](./04_unsupervised_clustering_and_pca.ipynb) | 🟡 Intermediate | **Principal Component Analysis (PCA)**, Scree plots and variance explained, 2D latent projections, **K-Means clustering**, and finding optimal $K$ with the **Elbow Method and Silhouette Analysis**. |
| **05** | [`05_evaluation_metrics_and_hyperparameter_tuning.ipynb`](./05_evaluation_metrics_and_hyperparameter_tuning.ipynb) | 🔴 Advanced | Stratified K-Fold Cross-Validation, exhaustive **`GridSearchCV`**, probabilistic **`RandomizedSearchCV`**, Bias vs. Variance diagnosis via **`learning_curve()`**, and pipeline serialization with **`joblib`**. |

---

## Recommended Learning Path

1. Open notebooks sequentially starting from `01`.
2. Emphasize pipeline composition to ensure no data leakage occurs between training and validation folds.
3. Review the diagnostic curves (learning curves, ROC curves, residual plots, scree plots).
