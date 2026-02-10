# Wine Classification Project – Antigravity Rules

## Project Overview
This project builds a complete machine learning pipeline to classify wines into
three classes using the UCI Wine dataset (`sklearn.datasets.load_wine()`).

The workflow includes exploratory data analysis, feature engineering,
multi-class classification with XGBoost, and model evaluation.

## Dataset
- Source: `sklearn.datasets.load_wine()`
- Samples: 178
- Features: 13 numeric chemical measurements
- Target: 3 wine classes
- Task type: Multi-class classification

## Core Rules
- Treat this strictly as a **classification** problem (not regression)
- Always use **stratified** train/test splits
- Always use **standard scaling** for numeric features
- Prefer reproducible pipelines with explicit random seeds

## Modeling Expectations
- Use XGBoost for multi-class classification
- Use 5-fold stratified cross-validation
- Evaluate using:
  - Accuracy
  - Precision (macro and per-class)
  - Recall (macro and per-class)
  - F1-score (macro and per-class)
  - Confusion matrix (with heatmap)
- Generate and save feature importance plots

## Output Requirements
- Save all artifacts under `output/`
- Organize outputs into subfolders:
  - `output/eda/`
  - `output/data/`
  - `output/model/`
- Ensure outputs are reproducible and well-documented
