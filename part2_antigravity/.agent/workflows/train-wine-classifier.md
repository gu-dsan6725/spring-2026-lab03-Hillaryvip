# Workflow: train-wine-classifier

## Purpose
Train and evaluate a multi-class XGBoost classifier for the UCI Wine dataset
using a reproducible and rule-driven workflow.

## Preconditions
- Follow all rules in `.gemini/GEMINI.md`
- Enforce data checks from `.agent/rules/data-quality.md`
- Use results from the EDA workflow
- Follow code style rules in `.agent/rules/code-style-guide.md`

## Steps

1. Load the processed Wine dataset.
2. Perform feature engineering, creating at least three derived features.
3. Apply standard scaling to all numeric features.
4. Split the data using a stratified train/test split.
5. Train an XGBoost multi-class classifier.
6. Perform 5-fold stratified cross-validation.
7. Generate predictions on the test set.
8. Compute evaluation metrics:
   - Accuracy
   - Precision (macro and per-class)
   - Recall (macro and per-class)
   - F1-score (macro and per-class)
9. Generate a confusion matrix and corresponding heatmap.
10. Compute and plot feature importance.
11. Save the trained model, metrics, and plots to `output/model/`.
12. Log a concise evaluation summary with recommendations.

## Outputs
- Trained model artifact
- Metrics (JSON or CSV)
- Confusion matrix + heatmap
- Feature importance plot
- Artifacts saved under `output/model/`
