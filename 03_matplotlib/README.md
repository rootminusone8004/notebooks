# Module 03: Matplotlib for Machine Learning

This module teaches students how to create publication-quality figures, diagnostic training dashboards, and intuitive machine learning model evaluations using Matplotlib's Object-Oriented interface.

---

## Notebook Overview & Difficulty Progression

| # | Notebook | Difficulty | Description & Key Topics |
|---|---|---|---|
| **01** | [`01_anatomy_of_a_figure_and_pyplot.ipynb`](./01_anatomy_of_a_figure_and_pyplot.ipynb) | 🟢 Beginner | Figure Anatomy (Figure, Axes, Spines, Ticks), Stateful Pyplot vs **Object-Oriented (`fig, ax`) Interface**, multi-metric line styling, legends, and early stopping markers. |
| **02** | [`02_core_statistical_plots.ipynb`](./02_core_statistical_plots.ipynb) | 🟢 Beginner | 4D Scatter plots with continuous colormaps, annotated horizontal bar charts for **feature importances**, histograms with probability density, and box plots for IQR and outliers. |
| **03** | [`03_multi_plot_layouts_and_subplots.ipynb`](./03_multi_plot_layouts_and_subplots.ipynb) | 🟡 Intermediate | Multi-panel subplots with shared axes, programmatic grid iteration via `.ravel()`, and advanced asymmetric layouts with **`GridSpec`** for training dashboards. |
| **04** | [`04_advanced_customization_and_ml_visualizations.ipynb`](./04_advanced_customization_and_ml_visualizations.ipynb) | 🔴 Advanced | **Dual-axis charts (`twinx`)** for simultaneous loss & accuracy monitoring, event annotations with arrows, **2D Classifier Decision Boundaries (`contourf`)**, ROC & AUC curves, and high-DPI publication exports (`savefig`). |

---

## Recommended Learning Path

1. Open notebooks sequentially starting from `01`.
2. Follow the Object-Oriented paradigm throughout—avoid relying on stateful `plt.plot()` calls.
3. Review the code cells to master the visual evaluation of overfitting, feature relevance, and decision surfaces.
