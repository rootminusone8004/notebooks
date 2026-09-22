# Machine Learning Curriculum Notebooks

Welcome to the Machine Learning course repository! This repository contains a structured, modular series of interactive Jupyter notebooks (`.ipynb`) designed to take students from numerical foundations to applied machine learning modeling and deployment.

Every module is built with an incremental difficulty curve: introductory examples establish core conceptual mechanics, while advanced sections demonstrate production-grade, complex techniques.

---

## Curriculum Structure

Each module is organized into its own numbered folder and contains progressively challenging notebooks:

```text
notebooks/
├── README.md
├── 01_numpy/                 # Numerical computing, vectorization, linear algebra, and ML from scratch (5 notebooks)
├── 02_pandas/                # Tabular wrangling, MultiIndexes, method chaining, and feature engineering (6 notebooks)
├── 03_matplotlib/            # Publication-grade plotting, dual axes, GridSpec, and ML diagnostic visualizations (4 notebooks)
├── 04_seaborn/               # Statistical data visualization, faceted grids, clustermaps, and automated EDA (4 notebooks)
├── 05_scikit_learn/          # Supervised & unsupervised ML, pipelines, probability calibration, and validation (5 notebooks)
├── 06_pickle/                # Python object serialization, bytecode protocols, security, safe unpickling, and cloudpickle (4 notebooks)
├── 07_joblib/                # Large array persistence, compression codecs, memory mapping, caching, and parallel computing (4 notebooks)
├── 08_opencv/                # Computer vision, morphology, contour analysis, ORB matching, and ML integration (6 notebooks)
├── 09_tensorflow_keras/      # Deep learning, autodiff, Keras APIs, callbacks, tf.data, CNNs, and custom loops (6 notebooks)
├── data_files/               # Repository CSV and Excel (.xlsx) tabular datasets
└── images/                   # Dedicated computer vision test images and benchmarks
```

---

## Prerequisites & Environment Setup

To run these notebooks locally or in an interactive environment (such as VS Code, JupyterLab, or Google Colab), install the required dependencies:

```bash
pip install numpy pandas matplotlib seaborn scikit-learn scipy openpyxl opencv-python tensorflow keras joblib cloudpickle jupyter
```

---

## Module Directory & Curriculum Map

| Module | Directory | Status | Notebooks Count | Foundational Topics | Advanced & Complex Usages |
|---|---|---|---|---|---|
| **01** | [`01_numpy/`](./01_numpy/) | ✅ Complete | 5 Notebooks | Ndarrays, slicing, views vs copies, broadcasting, dot products, matrix algebra. | Structured arrays, memory mapping (`np.memmap`), sliding windows, Einstein summation (`np.einsum`), Truncated SVD, Cholesky solvers, Ridge/Momentum/Softmax from scratch. |
| **02** | [`02_pandas/`](./02_pandas/) | ✅ Complete | 6 Notebooks | Series, DataFrames, safe `.loc`/`.iloc`, missing data imputation, groupby `.agg`, merges. | MultiIndex coordinate slicing (`IndexSlice`), `.pipe()` method chaining, subgroup-conditional imputation, `pd.merge_asof`, out-of-fold smoothed target encoding, cyclical sine/cosine features. |
| **03** | [`03_matplotlib/`](./03_matplotlib/) | ✅ Complete | 4 Notebooks | OO interface (`fig, ax`), scatter with colorbars, horizontal bars, histograms, box plots, subplots. | Dual Y-axes (`twinx`), shaded overfitting spans (`axvspan`), annotations (`annotate`), hexbin density maps (`LogNorm`), inset zoom subplots (`inset_axes`), multi-class OvR ROC, 3D loss topography. |
| **04** | [`04_seaborn/`](./04_seaborn/) | ✅ Complete | 4 Notebooks | Axes-level vs figure-level, `histplot`, `kdeplot`, `ecdfplot`, `scatterplot`, `boxplot`, `pairplot`. | Multi-faceted conditioning (`displot`), factor interactions (`pointplot`), metadata clustermaps (`row_colors`), automated collinearity pruning, automated EDA diagnostic pipeline. |
| **05** | [`05_scikit_learn/`](./05_scikit_learn/) | ✅ Complete | 5 Notebooks | Estimator/Transformer API, `ColumnTransformer`, pipelines, OLS/Ridge/Lasso, PCA, K-Means, GridSearchCV. | Custom Transformers (`BaseEstimator`/`TransformerMixin`), `TransformedTargetRegressor`, probability calibration (`CalibratedClassifierCV`), DBSCAN density clustering, `TimeSeriesSplit` walk-forward validation. |
| **06** | [`06_pickle/`](./06_pickle/) | ✅ Complete | 4 Notebooks | In-memory vs disk serialization (`dumps`/`loads`, `dump`/`load`), bytecode protocols 0–5, picklable limitations, bypass of `__init__()`. | Protocol 5 Out-of-Band (`PickleBuffer`) zero-copy memory transfers, custom state hooks (`__getstate__`/`__setstate__`), schema evolution & backward compatibility, `__reduce__` factory control, RCE vulnerability exploits, `RestrictedUnpickler` allowlisting, HMAC-SHA256 tamper-evident signing, distributed serialization of lambdas/closures with `cloudpickle`, format comparison matrix. |
| **07** | [`07_joblib/`](./07_joblib/) | ✅ Complete | 4 Notebooks | `joblib.dump()`/`load()`, NumPy array chunking, multi-algorithm compression (`zlib`, `gzip`, `bz2`, `lzma`, `lz4`), `Memory` caching. | Scikit-Learn pipeline serialization envelopes, multi-codec performance benchmarking, zero-copy OS memory mapping (`mmap_mode='r'` / `'c'`), out-of-core batch streaming on datasets exceeding RAM, persistent feature engineering memoization, cache eviction/quota management, multi-core parallel computing with `Parallel(delayed(...))`, `loky` backend shared memory optimization, parallel cross-validation. |
| **08** | [`08_opencv/`](./08_opencv/) | ✅ Complete | 6 Notebooks | Array representation, I/O flags, BGR vs RGB, drawing primitives, resizing, spatial convolution, Canny edge detection. | HSV color segmentation, CLAHE on LAB luminance, 4-point perspective warp (Homography), vision data augmentation with synchronized bounding boxes, bilateral filtering, morphological illumination correction, Douglas-Peucker shape approximation (`approxPolyDP`), rotated bounding boxes (`minAreaRect`), ORB invariant keypoints, Lowe's ratio test, RANSAC homography localization, multi-scale template matching, marker-controlled Watershed segmentation, HOG feature extraction + SVM image classification, OpenCV DNN inference (`blobFromImage`). |
| **09** | [`09_tensorflow_keras/`](./09_tensorflow_keras/) | ✅ Complete | 6 Notebooks | Tensor ranks, immutable constants vs. mutable `tf.Variable`, matrix math (`matmul`, `@`), broadcasting, Autodiff with `tf.GradientTape`, Sequential/Functional/Subclassing Keras APIs, Callbacks (`EarlyStopping`, `ModelCheckpoint`), `tf.data.Dataset`, 2D Convolutions (`Conv2D`, `MaxPooling2D`). | Multi-variable gradients & persistent tapes, custom gradient descent loop from scratch, `@tf.function` graph compilation, deep residual MLP (ResNet skip connections) with multi-task heads, custom Keras Layer subclassing with learnable scaling, Cosine Decay learning rates with warmup, custom callbacks for validation telemetry & anomaly detection, end-to-end tabular preprocessing models directly consuming raw data, transfer learning & two-stage fine-tuning (MobileNetV2), feature map visualization, custom loss subclasses (Focal Loss), overriding `train_step()` with gradient clipping, and Convolutional Denoising Autoencoders. |

---

## Pedagogical Design

Every notebook follows a consistent 4-step learning path:
1. **Learning Objectives**: Clear milestones for what students will master.
2. **Conceptual Foundations**: Theory, mathematical formulations, and visual intuition.
3. **Worked Examples**: Fully commented code demonstrating foundational ML patterns and edge cases.
4. **Advanced Complex Usages**: Real-world production techniques and algorithms solving challenging ML problems.
