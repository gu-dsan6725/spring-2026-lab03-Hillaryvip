# Skill: wine-profiler

## Purpose
Profile the UCI Wine dataset to understand class-specific patterns,
feature distributions, and discriminative characteristics relevant to
multi-class classification.

This skill provides a reusable, standardized profiling workflow.

## Inputs
- Wine dataset loaded via `sklearn.datasets.load_wine()`
- Optional output directory (default: `output/eda/`)

## Step-by-Step Instructions

1. Load the Wine dataset and convert it to a `polars.DataFrame`.
2. Verify dataset integrity:
   - 13 numeric feature columns
   - 3 distinct target classes
3. Compute global summary statistics for all features.
4. Compute **class-specific** summary statistics (mean, std, min, max).
5. Generate feature distribution plots **per class**.
6. Analyze class separability by comparing feature means and variances.
7. Identify potentially discriminative features based on:
   - Between-class differences
   - Low within-class variance
8. Log key insights about which features best distinguish wine classes.
9. Save all profiling artifacts and plots to `output/eda/`.

## Outputs
- Global and class-specific statistics
- Per-class feature distribution plots
- Discriminative feature analysis
- Artifacts saved under `output/eda/`
