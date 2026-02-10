# Slash Command: /plan-wine

## Purpose
Generate a structured implementation plan for a complete machine learning pipeline
to classify wines into three classes using the UCI Wine dataset.

This command prepares the project for implementation while enforcing all rules
defined in `CLAUDE.md`.

---

## Objectives
- Build a reproducible ML pipeline for Wine classification
- Perform exploratory data analysis (EDA)
- Engineer features and prepare data for modeling
- Train and evaluate a multi-class XGBoost classifier
- Produce a comprehensive evaluation report

---

## Dataset
- Source: `sklearn.datasets.load_wine()`
- Samples: 178
- Features: 13 numeric chemical measurements
- Target: 3 wine classes
- Task type: Multi-class classification

---

## Architecture
The pipeline should be divided into the following scripts:

1. `01_eda.py`
   - Load and explore the dataset
   - Generate summary statistics and plots
   - Save EDA artifacts to `output/eda/`

2. `02_feature_engineering.py`
   - Create derived features 
   - Standard-scale features
   - Perform stratified train/test split
   - Save processed datasets to `output/data/`

3. `03_xgboost_model.py`
   - Train an XGBoost multi-class classifier
   - Use cross-validation
   - Evaluate model performance
   - Save model and metrics to `output/model/`

---

## Evaluation Metrics
- Accuracy
- Precision (macro and per-class)
- Recall (macro and per-class)
- F1-score (macro and per-class)
- Confusion matrix (with heatmap)
- Feature importance

---

## File Structure
part1_claude_code/
├── src/
│ ├── 01_eda.py
│ ├── 02_feature_engineering.py
│ └── 03_xgboost_model.py
output/
├── eda/
├── data/
└── model/