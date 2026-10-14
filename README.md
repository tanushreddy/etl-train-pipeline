# ETL Train Pipeline

An end-to-end automated ML data pipeline built with scikit-learn.

## Pipeline Stages

| Stage | Description |
|-------|-------------|
| Extract | Load Iris dataset as a DataFrame |
| Validate | Check for missing values and required columns |
| Transform | Standard-scale all features |
| Train | Fit a Random Forest classifier (80/20 split) |
| Evaluate | Report accuracy and per-class metrics |
| Persist | Save model and scaler as `.pkl` files in `artifacts/` |

## Usage

```bash
python pipeline.py
```

## Output

```
=== Automated Data Pipeline Started ===
[EXTRACT ] loaded 150 rows x 5 cols
[VALIDATE] no missing values, target present -> OK
[TRANSFORM] standard-scaled 4 features
[TRAIN ] model fitted, test accuracy = 1.000
[REPORT ] per-class metrics:
...
[PERSIST ] saved model -> artifacts/model.pkl
[PERSIST ] saved scaler -> artifacts/scaler.pkl
=== Pipeline Completed Successfully ===
```
