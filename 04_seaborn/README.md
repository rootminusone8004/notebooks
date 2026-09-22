# Module 04: Seaborn for Machine Learning

This module teaches students modern statistical data visualization, multi-dimensional feature interaction mapping, and disciplined Exploratory Data Analysis (EDA) workflows using Seaborn. Every notebook progresses from clear foundational concepts to production-grade advanced patterns.

---

## Notebook Overview & Difficulty Progression

| # | Notebook | Difficulty | Foundational Concepts | Advanced / Complex Usages |
|---|---|---|---|---|
| **01** | [`01_architecture_and_distribution_plots.ipynb`](./01_architecture_and_distribution_plots.ipynb) | 🟢 Beginner | Figure-Level vs. **Axes-Level architecture**, themes & palettes, `sns.histplot` with KDE, 2D bivariate density surfaces, and **Empirical Cumulative Distribution Functions (ECDF)**. | Multi-faceted conditioning grids with Figure-Level `sns.displot` mapping `col`, `row`, and `hue` simultaneously with non-parametric kernel density surfaces. |
| **02** | [`02_relational_and_categorical_plots.ipynb`](./02_relational_and_categorical_plots.ipynb) | 🟢 Beginner | 5-variable scatter plots (`hue`, `style`, `size`), automated bootstrap confidence intervals (`lineplot`), and categorical distribution comparison (**Box, Violin, and Strip plots**). | Faceted relational grids (`sns.relplot`) across multiple categorical splits, and factor interaction estimation with `sns.pointplot` and bootstrap 95% confidence intervals. |
| **03** | [`03_matrix_plots_and_correlation_heatmaps.ipynb`](./03_matrix_plots_and_correlation_heatmaps.ipynb) | 🟡 Intermediate | Pearson & Spearman correlations, **upper-triangle masked heatmaps (`np.triu`)**, identifying multicollinearity, and **Hierarchical Clustermaps** with dendrograms. | Patient/sample clustermaps with dual metadata color bars (`row_colors`), and automated programmatic collinearity pruning pipelines filtering features by correlation threshold. |
| **04** | [`04_multi_plot_grids_and_eda_workflow.ipynb`](./04_multi_plot_grids_and_eda_workflow.ipynb) | 🔴 Advanced | Pairwise scatter grids (`pairplot`), custom triangle mappings (`PairGrid`), small multiples (`FacetGrid`), and a **complete 5-step Exploratory Data Analysis (EDA) workflow** for ML. | Modular, automated EDA diagnostic reporting pipeline with statistical skewness screening and multi-faceted violin distribution summaries. |

---

## Recommended Learning Path

1. Open notebooks sequentially starting from `01`.
2. Follow the statistical rationale behind each visualization type.
3. Pay close attention to how visualizations directly motivate feature selection, log transformations, and dimensionality reduction.
