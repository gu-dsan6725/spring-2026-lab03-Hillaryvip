# Workflow: run-wine-eda

## Purpose
Execute a complete exploratory data analysis workflow for the UCI Wine
classification dataset, following project rules and data-quality checks.

## Preconditions
- Follow all rules in `.gemini/GEMINI.md`
- Enforce data checks from `.agent/rules/data-quality.md`
- Follow coding standards in `.agent/rules/code-style-guide.md`

## Steps

1. Load the Wine dataset using `sklearn.datasets.load_wine()`.
2. Convert the dataset into a `polars.DataFrame`.
3. Validate data quality:
   - Confirm 13 numeric features
   - Confirm 3 target classes
   - Check for missing or infinite values
4. Log dataset shape, column names, and data types.
5. Compute and log summary statistics for all features.
6. Analyze and log class balance.
7. Generate feature distribution plots grouped by class.
8. Compute a correlation matrix and save a heatmap.
9. Perform basic outlier detection (IQR or z-score) and summarize results.
10. Save all plots and artifacts to `output/eda/`.
11. Log a concise summary of EDA findings.

## Outputs
- Summary statistics (logged)
- Distribution plots
- Correlation heatmap
- Outlier analysis summary
- Artifacts saved under `output/eda/`
