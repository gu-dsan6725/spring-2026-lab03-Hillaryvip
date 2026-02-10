# Skill: analyze-wine-data

## Purpose
Guide the AI assistant through a complete exploratory data analysis (EDA) workflow for the UCI Wine classification dataset.

This skill standardizes how EDA is performed so it can be reused across projects.

## Inputs
- Wine dataset loaded via `sklearn.datasets.load_wine()`
- Output directory path (default: `output/eda/`)

## Step-by-Step Instructions

1. Load the Wine dataset and convert it into a `polars.DataFrame`.
2. Log the dataset shape, column names, and data types.
3. Compute and log summary statistics for all numeric features.
4. Check class distribution for the three wine classes and log class balance.
5. Generate distribution plots (histograms or KDEs) for each feature, grouped or colored by class.
6. Compute a correlation matrix for numeric features and save a correlation heatmap.
7. Perform basic outlier detection using IQR or z-score methods and summarize findings.
8. Save all plots and artifacts to the specified output directory.
9. Log completion of EDA with a clear summary of findings.

## Outputs
- Summary statistics (logged)
- Feature distribution plots
- Correlation heatmap
- Outlier detection summary
- All outputs saved under `output/eda/`
