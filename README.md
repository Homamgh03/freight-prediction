# Freight Rate Machine Learning Assessment

This repository contains the complete end-to-end machine learning solution for predicting freight rates for Spotter.

## 📁 Project Structure
- `train.py` (or your Notebook): Data cleaning, feature engineering, and model training script using XGBoost.
- `predict.py` (or your Notebook): Generates the 12,000 required predictions for validation.
- `score.py`: Official validation script provided by Spotter to check output integrity.
- `validation_predictions.csv`: The final generated predictions file.
- `requirements.txt`: Required Python dependencies.
- `scorer_results/`: Contains the generated December 2025 chart (`candidate_december.png`).

---

## 🚀 Run Instructions

1. **Install Dependencies:**
   Make sure you have Python installed, then run the following command to install the required packages:
   ```bash
   pip install -r requirements.txt

Run the Official Scorer & Generate Chart:
Execute the validation script to verify predictions and generate the December forecast visualization:

Bash
python score.py --predictions validation_predictions.csv --december-predictions data/december_chart_inputs.csv
🛠️ Methodology & Approach
Data Quality Engineering: Handled anomalies by correcting negative load weights, and imputed missing values using robust statistical medians.

Feature Engineering: Extracted temporal features (month, day, day of week) and applied Label Encoding to categorical equipment types.

Model Choice: Utilized an optimized XGBoost Regressor to capture non-linear relationships and deliver robust generalization on tabular transportation data.