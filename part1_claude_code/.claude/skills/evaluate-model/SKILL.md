# Skill: evaluate-classifier

## Purpose
Guide the AI assistant through a standardized evaluation workflow for a multi-class classification model trained on the UCI Wine dataset.
This skill ensures consistent evaluation practices and can be reused across different classification projects.

## Inputs
- Trained classification model
- Test dataset (features + labels)
- Output directory path (default: `output/model/`)

## Step-by-Step Instructions

1. Load the trained model and the held-out test dataset.
2. Generate predictions and predicted class probabilities.
3. Compute overall evaluation metrics:
   - Accuracy
   - Precision (macro and per-class)
   - Recall (macro and per-class)
   - F1-score (macro and per-class)
4. Generate a confusion matrix and save both the raw matrix and a heatmap visualization.
5. Compute and plot feature importance for the trained XGBoost classifier.
6. Log all metrics using the project’s required logging format.
7. Save evaluation metrics to a structured file.
8. Summarize model strengths, weaknesses, and potential improvements.
9. Save all artifacts to the specified output directory.

## Outputs
- accuracy, precision, recall, F1
- Confusion matrix and heatmap
- Feature importance plot
- JSON or CSV
- All outputs saved under `output/model/`
