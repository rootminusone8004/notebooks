# Module 01: NumPy for Machine Learning

This module introduces students to NumPy, the foundational numerical engine powering the modern Python data science and machine learning ecosystem. Every notebook progresses from clear foundational concepts to production-grade advanced patterns.

---

## Notebook Overview & Difficulty Progression

| # | Notebook | Difficulty | Foundational Concepts | Advanced / Complex Usages |
|---|---|---|---|---|
| **01** | [`01_array_basics_and_creation.ipynb`](./01_array_basics_and_creation.ipynb) | 🟢 Beginner | Lists vs `ndarray`, creation routines (`zeros`, `ones`, `arange`, `linspace`, `eye`), numeric CSV I/O (`np.savetxt`, `np.loadtxt`), array attributes (`shape`, `ndim`, `nbytes`), `float32` vs `float64` memory optimization. | Structured Arrays with custom `np.dtype`, memory-mapped arrays (`np.memmap`) for out-of-core datasets, zero-copy strided sliding windows (`sliding_window_view`). |
| **02** | [`02_indexing_slicing_and_reshaping.ipynb`](./02_indexing_slicing_and_reshaping.ipynb) | 🟢 Beginner | 1D/2D slicing, views vs copies (`.base`, `.copy()`), reshaping with `-1`, flattening (`ravel` vs `flatten`), expanding dims (`np.newaxis`), horizontal/vertical stacking. | Advanced multi-axis fancy indexing with integer arrays, deep-learning tensor permutations (B, C, H, W $\leftrightarrow$ B, H, W, C), and Einstein Summation (`np.einsum`). |
| **03** | [`03_vectorization_and_broadcasting.ipynb`](./03_vectorization_and_broadcasting.ipynb) | 🟡 Intermediate | Vectorized arithmetic vs Python loops, Universal Functions (`ufuncs`), The 3 Rules of Broadcasting, outer products, boolean filtering, `np.where`, `np.select`. | Numerically stable multi-dimensional Softmax with Log-Sum-Exp trick, loop-less one-hot encoding (`np.eye(C)[labels]`), batched Mahalanobis distance. |
| **04** | [`04_math_stats_and_linear_algebra.ipynb`](./04_math_stats_and_linear_algebra.ipynb) | 🟡 Intermediate | Reductions along axes with `keepdims=True`, dot products, matrix multiplication (`@`), determinants, linear system solvers, $L_1$/$L_2$ norms, modern `default_rng`. | Truncated SVD for Low-Rank Compression, Cholesky Decomposition for SPD systems, full Principal Component Analysis (PCA) from scratch via eigendecomposition. |
| **05** | [`05_practical_ml_applications.ipynb`](./05_practical_ml_applications.ipynb) | 🔴 Advanced | Leak-free `StandardScaler` from scratch, vectorized pairwise Euclidean distance matrix, mini-batch generator, Gradient Descent Linear Regression, KNN classifier. | Closed-Form Ridge Regression with bias penalty exemption, Mini-Batch SGD with Momentum from scratch, Multi-Class Softmax Regression from scratch with cross-entropy loss. |

---

## Recommended Learning Path

1. Open each notebook sequentially starting from `01`.
2. Read the theoretical concepts and execute each code cell to observe the runtime outputs.
3. Pay close attention to the highlighted **Machine Learning Caveats** (e.g., in-place view mutations, broadcasting dimension rules, and floating-point precision).
