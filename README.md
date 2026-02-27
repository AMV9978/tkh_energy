## TKH_Energy Project Overview (Energy Efficiency + Linear Regression)

This Phase 1 project is a portfolio-style **end-to-end data science workflow** focused on building a baseline **Linear Regression** model using the **UCI Energy Efficiency** dataset. The main purpose is not to be perfect, but to clearly demonstrate understanding of the full process of going from raw data → exploration → cleaning → modeling → evaluation.

### Why this dataset?
Buildings consume a large amount of energy, and small design choices can have a real impact on heating and cooling demand. This dataset includes **768 building simulations** with **8 design features** (X1–X8) such as **relative compactness, surface area, wall area, roof area, overall height, orientation, glazing area, and glazing area distribution**. The targets represent energy demand:
- **Y1 = Heating Load**
- **Y2 = Cooling Load**

For this project, I focus on predicting **Heating Load (Y1)** (and may optionally build a second model for **Cooling Load (Y2)**) to understand how these building characteristics influence energy performance.

### What this project demonstrates
This repository shows a complete, reproducible workflow:
1. **Exploratory Data Analysis (EDA):** Inspect shape, data types, distributions, correlations, and initial insights.
2. **Data Wrangling & Pre-processing:** Clean the dataset, verify data quality, and prepare features for regression (including handling categorical-style variables like orientation/glazing distribution).
3. **Modeling:** Train a baseline Linear Regression model on a train/test split.
4. **Evaluation & Diagnostics:** Measure performance using **R²** and **RMSE**, and use residual plots to understand where the model performs well or struggles.
5. **Interpretation:** Review key predictors (coefficients) to explain which building features most influence the predicted heating load.

### Repository Structure
- `data/raw/` contains the original dataset file.
- `data/processed/` contains the cleaned dataset used for modeling.
- `notebooks/01_explore.ipynb` includes EDA and initial findings.
- `notebooks/02_clean.ipynb` includes cleaning and preprocessing steps and saves the processed CSV.
- `notebooks/03_model.ipynb` trains the regression model and reports metrics/plots.
- `docs/figures/` contains exported plots used in this README.
