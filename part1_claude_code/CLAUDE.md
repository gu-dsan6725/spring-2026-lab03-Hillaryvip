# Wine Classification ML Project

## Project Overview
This project performs exploratory data analysis and builds an XGBoost **classification** model on the UCI Wine dataset using `sklearn.datasets.load_wine()`.

The goal is to classify wines into **three classes** based on 13 chemical features such as alcohol, malic acid, ash, flavanoids, phenols, and proline.

This project is designed to demonstrate how Claude Code can be guided using project rules, hooks, skills, and slash commands to build a complete machine learning pipeline.

## Coding Standards

### Language and Tools
- Use Python 3.11+
- Use `uv` for package management (never pip)
- Use `polars` for data manipulation (not pandas)
- Use `ruff` for linting and formatting
- Use `pytest` for testing
- Use `scikit-learn` for data loading, preprocessing, and evaluation
- Use `xgboost` for model training
- Use `matplotlib` (and seaborn if needed) for visualization

### Code Style
- Use type annotations for all function parameters (one parameter per line)
- All private helper functions must start with an underscore (`_`) and appear at the top of the file
- Public functions should be defined after private functions
- Functions should generally be no longer than 30–50 lines
- Use two blank lines between function definitions
- Use multi-line imports

### Logging
Always use the following logging configuration:

```python
import logging

logging.basicConfig(
    level=logging.INFO,
    format="%(asctime)s,p%(process)s,{%(filename)s:%(lineno)d},%(levelname)s,%(message)s",
)
```

- Use `logging.info()` for pipeline progress
- Use `logging.debug()` when a `--debug` flag is enabled

### Constants
- Do not hard-code constants inside functions
- Declare constants at the top of the file with type annotations
- Examples include random seeds, test split ratios, and cross-validation folds

### Data and Modeling Rules
- Treat the Wine dataset as a **multi-class classification problem**
- Always use **stratified** train/test splits
- Apply **standard scaling** before modeling
- Use **5-fold stratified cross-validation**
- Report the following metrics:
  - Accuracy
  - Precision, Recall, and F1-score (macro and per-class)
  - Confusion matrix
- Generate feature importance plots for the trained model


### Output
- Save all plots, data artifacts, and reports under the `output/` directory
- Organize outputs into logical subfolders (e.g., `output/eda/`, `output/data/`, `output/model/`)
- Pretty-print dictionaries in logs using `json.dumps(data, indent=2, default=str)`
- Ensure scripts are reproducible via CLI arguments such as `--seed` and `--output-dir`
