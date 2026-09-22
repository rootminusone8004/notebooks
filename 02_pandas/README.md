# Module 02: Pandas for Machine Learning

This module equips students with the data wrangling, cleaning, transformation, and feature engineering skills required to handle real-world machine learning datasets. Every notebook progresses from clear foundational concepts to production-grade advanced patterns.

---

## Notebook Overview & Difficulty Progression

| # | Notebook | Difficulty | Foundational Concepts | Advanced / Complex Usages |
|---|---|---|---|---|
| **01** | [`01_series_and_dataframe_fundamentals.ipynb`](./01_series_and_dataframe_fundamentals.ipynb) | 🟢 Beginner | `pd.Series`, `pd.DataFrame`, **CSV & Excel (`.xlsx`) file I/O** (`read_csv`, `read_excel`, `ExcelWriter`, `ExcelFile`, `usecols`, `chunksize`), schema inspection (`info()`, `describe()`), and memory optimization with category types. | Hierarchical MultiIndexes, Cartesian index construction (`from_product`), coordinate slicing with `pd.IndexSlice`, and unstack/stack reshaping. |
| **02** | [`02_indexing_filtering_and_assignment.ipynb`](./02_indexing_filtering_and_assignment.ipynb) | 🟢 Beginner | Label (`.loc`) vs Position (`.iloc`), multi-clause boolean filtering (`&`, `\|`, `~`), `.isin()`, `.between()`, `.query()`, and eliminating `SettingWithCopyWarning`. | Declarative method chaining with `.pipe()` and `.assign()`, dynamic querying referencing external environment variables (`@var`), and multi-branch vectorization via `np.select`. |
| **03** | [`03_data_cleaning_and_missing_values.ipynb`](./03_data_cleaning_and_missing_values.ipynb) | 🟡 Intermediate | Missing data detection (`.isna()`), statistical imputation (Mean, Median, Mode), missingness indicators, deduplication, and `.str` cleaning. | Subgroup-conditional imputation (`groupby().transform()`) to eliminate category bias, and structured feature extraction from complex log strings using named regex groups. |
| **04** | [`04_aggregations_grouping_and_pivot_tables.ipynb`](./04_aggregations_grouping_and_pivot_tables.ipynb) | 🟡 Intermediate | Split-Apply-Combine with `groupby()`, multi-feature `.agg()`, within-group normalization via `.transform()`, pivot tables, and `crosstab()`. | Expanding windows, cumulative metrics (`cumsum`, `cummax`), within-group percentile ranking (`rank(pct=True)`), and deep entity profiling via custom group `.apply()`. |
| **05** | [`05_combining_datasets_and_timeseries.ipynb`](./05_combining_datasets_and_timeseries.ipynb) | 🟡 Intermediate | Relational joins (`pd.merge()` with inner, left, outer), row/column concatenation, datetime `.dt` components, rolling windows, and lag features. | Asynchronous nearest-timestamp joins with `pd.merge_asof` (zero-leakage backward matching with tolerance), and Exponentially Weighted Moving Averages (`.ewm()`). |
| **06** | [`06_feature_engineering_with_pandas.ipynb`](./06_feature_engineering_with_pandas.ipynb) | 🔴 Advanced | One-Hot Encoding (`get_dummies` with `drop_first=True`), ordinal mapping, equal-width (`cut`) vs equal-frequency (`qcut`) binning, Tukey's IQR outlier clipping, and $X, y$ partitioning. | Leak-free Out-of-Fold (OOF) Smoothed Target Encoding with Bayesian m-estimates and K-Fold splitting, and cyclical sine/cosine projections for periodic temporal variables. |

---

## Recommended Learning Path

1. Open notebooks in sequential order starting from `01`.
2. Follow along with the conceptual explanations and run the worked code blocks.
3. Review the **ML Pro-Tips** (e.g., preventing the dummy variable trap, avoiding data leakage during imputation, and preserving missingness signals).
