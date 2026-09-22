# Module 02: Pandas for Machine Learning

This module equips students with the data wrangling, cleaning, transformation, and feature engineering skills required to handle real-world machine learning datasets.

---

## Notebook Overview & Difficulty Progression

| # | Notebook | Difficulty | Description & Key Topics |
|---|---|---|---|
| **01** | [`01_series_and_dataframe_fundamentals.ipynb`](./01_series_and_dataframe_fundamentals.ipynb) | 🟢 Beginner | `pd.Series`, `pd.DataFrame`, reading CSVs, schema inspection (`info()`, `describe()`), and memory optimization with category and numeric downcasting. |
| **02** | [`02_indexing_filtering_and_assignment.ipynb`](./02_indexing_filtering_and_assignment.ipynb) | 🟢 Beginner | Label (`.loc`) vs Position (`.iloc`), multi-clause boolean filtering (`&`, `\|`, `~`), `.isin()`, `.between()`, `.query()`, and eliminating `SettingWithCopyWarning`. |
| **03** | [`03_data_cleaning_and_missing_values.ipynb`](./03_data_cleaning_and_missing_values.ipynb) | 🟡 Intermediate | Missing data detection (`.isna()`), statistical imputation (Mean, Median, Mode, `ffill`), missingness indicators, deduplication, and `.str` normalization. |
| **04** | [`04_aggregations_grouping_and_pivot_tables.ipynb`](./04_aggregations_grouping_and_pivot_tables.ipynb) | 🟡 Intermediate | Split-Apply-Combine with `groupby()`, multi-feature `.agg()`, within-group normalization via `.transform()`, pivot tables, and `crosstab()`. |
| **05** | [`05_combining_datasets_and_timeseries.ipynb`](./05_combining_datasets_and_timeseries.ipynb) | 🟡 Intermediate | Relational joins (`pd.merge()` with inner, left, outer), row/column concatenation, datetime `.dt` components, rolling windows, and autoregressive lag features. |
| **06** | [`06_feature_engineering_with_pandas.ipynb`](./06_feature_engineering_with_pandas.ipynb) | 🔴 Advanced | One-Hot Encoding (`get_dummies` with `drop_first=True`), ordinal mapping, equal-width (`cut`) vs equal-frequency (`qcut`) binning, Tukey's IQR outlier filtering, and $X, y$ partitioning for Scikit-Learn. |

---

## Recommended Learning Path

1. Open notebooks in sequential order starting from `01`.
2. Follow along with the conceptual explanations and run the worked code blocks.
3. Review the **ML Pro-Tips** (e.g., preventing the dummy variable trap, avoiding data leakage during imputation, and preserving missingness signals).
