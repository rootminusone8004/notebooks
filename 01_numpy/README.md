# Module 01: NumPy for Machine Learning

This module introduces students to NumPy, the foundational numerical engine powering the modern Python data science and machine learning ecosystem.

---

## Notebook Overview & Difficulty Progression

| # | Notebook | Difficulty | Description & Key Topics |
|---|---|---|---|
| **01** | [`01_array_basics_and_creation.ipynb`](./01_array_basics_and_creation.ipynb) | 🟢 Beginner | Lists vs `ndarray`, array creation (`zeros`, `ones`, `arange`, `linspace`, `eye`), array attributes (`shape`, `ndim`, `nbytes`), `float32` vs `float64` memory optimization. |
| **02** | [`02_indexing_slicing_and_reshaping.ipynb`](./02_indexing_slicing_and_reshaping.ipynb) | 🟢 Beginner | 1D & multi-dimensional slicing, **views vs copies** (`.base`, `.copy()`), reshaping with `-1`, flattening (`ravel` vs `flatten`), expanding dimensions (`np.newaxis`, `expand_dims`), vertical/horizontal stacking. |
| **03** | [`03_vectorization_and_broadcasting.ipynb`](./03_vectorization_and_broadcasting.ipynb) | 🟡 Intermediate | Vectorization mechanics, universal functions (`ufuncs`), **The 3 Rules of Broadcasting**, outer products, boolean masking, conditional selection (`np.where`, `np.select`), prediction decoding (`argmax`, `argsort`). |
| **04** | [`04_math_stats_and_linear_algebra.ipynb`](./04_math_stats_and_linear_algebra.ipynb) | 🟡 Intermediate | Axis-wise reductions with `keepdims=True`, dot products, matrix multiplication (`@`), `np.linalg` (inversion, determinants, linear systems), **eigenvalues & eigenvectors (PCA intuition)**, $L_1$/$L_2$ regularization norms, modern random generation (`default_rng`). |
| **05** | [`05_practical_ml_applications.ipynb`](./05_practical_ml_applications.ipynb) | 🔴 Advanced | **Production-style StandardScaler** from scratch (preventing data leakage), **loop-less pairwise distance matrix**, **mini-batch generator**, **Linear Regression with Gradient Descent**, **Logistic Regression & classification metrics**, **KNN Classifier from scratch**. |

---

## Recommended Learning Path

1. Open each notebook sequentially starting from `01`.
2. Read the theoretical concepts and execute each code cell to observe the runtime outputs.
3. Pay close attention to the highlighted **Machine Learning Caveats** (e.g., in-place view mutations, broadcasting dimension rules, and floating-point precision).
