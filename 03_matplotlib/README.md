# Module 03: Matplotlib for Machine Learning

This module teaches students how to create publication-quality figures, diagnostic training dashboards, and intuitive machine learning model evaluations using Matplotlib's Object-Oriented interface. Every notebook progresses from clear foundational concepts to production-grade advanced patterns.

---

## Notebook Overview & Difficulty Progression

| # | Notebook | Difficulty | Foundational Concepts | Advanced / Complex Usages |
|---|---|---|---|---|
| **01** | [`01_anatomy_of_a_figure_and_pyplot.ipynb`](./01_anatomy_of_a_figure_and_pyplot.ipynb) | 🟢 Beginner | Figure Anatomy (Figure, Axes, Spines, Ticks), Stateful Pyplot vs **Object-Oriented (`fig, ax`) Interface**, multi-metric line styling, labels, legends, and axis styling. | Dual Y-Axes (`ax.twinx()`) tracking disparate scales (Loss vs Accuracy), shaded overfitting diagnostic spans (`ax.axvspan`), and dynamic checkpoint annotations with custom arrows (`ax.annotate`). |
| **02** | [`02_core_statistical_plots.ipynb`](./02_core_statistical_plots.ipynb) | 🟢 Beginner | 4D Scatter plots with continuous colormaps, annotated horizontal bar charts for **feature importances**, histograms with density scaling, and box plots for IQR and outliers. | Hexagonal 2D Binning (`ax.hexbin`) with Logarithmic Color Normalization (`LogNorm`) to resolve severe overplotting on massive ($N=100,000$) datasets. |
| **03** | [`03_multi_plot_layouts_and_subplots.ipynb`](./03_multi_plot_layouts_and_subplots.ipynb) | 🟡 Intermediate | Multi-panel subplots with shared axes (`sharex`, `sharey`), programmatic grid iteration via `.ravel()`, and advanced asymmetric layouts with **`GridSpec`** for training dashboards. | Inset Zoom Subplots (`ax.inset_axes` with `indicate_inset_zoom`) for micro-structural inspection of convergence oscillations and transient anomalies within parent plots. |
| **04** | [`04_advanced_customization_and_ml_visualizations.ipynb`](./04_advanced_customization_and_ml_visualizations.ipynb) | 🔴 Advanced | Dual-axis charts (`twinx`), event annotations with arrows, **2D Classifier Decision Boundaries (`contourf`)**, ROC & AUC curves, and high-DPI publication exports (`savefig`). | Multi-Class One-vs-Rest (OvR) ROC analysis with per-class AUC curves, and 3D Optimization Loss Surfaces (`Axes3D`, `plot_surface`) with gradient descent optimization trajectory. |

---

## Recommended Learning Path

1. Open notebooks sequentially starting from `01`.
2. Follow the Object-Oriented paradigm throughout—avoid relying on stateful `plt.plot()` calls.
3. Review the code cells to master the visual evaluation of overfitting, feature relevance, and decision surfaces.
