# Data Quality Rules – Wine Classification

## Purpose
Ensure data integrity, correctness, and suitability for multi-class
classification on the UCI Wine dataset.

## Data Validation Rules
- Confirm the dataset contains exactly 13 numeric feature columns
- Confirm the target variable has exactly 3 unique classes
- Verify no missing values in features or target
- Verify no infinite values after feature engineering

## Class Balance
- Compute and log class distribution
- Flag severe imbalance if any class represents <20% of samples

## Feature Checks
- Verify all features are numeric
- Apply standard scaling before modeling
- Log feature ranges and summary statistics

## Split Integrity
- Always use stratified train/test splits
- Confirm class proportions are preserved after splitting

## Output
- Log all data quality checks
- Halt training if critical data quality violations are found
