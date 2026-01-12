# Electricity Price Prediction (Finland)

Predicting **hourly day-ahead electricity prices** using renewable-energy and market drivers such as **wind/solar production**, **balancing up-regulation bids**, and **net import/export**.

## Project highlights
- Time-series feature engineering (lags, calendar features) for day-ahead pricing.
- Ensemble models for non-linear relationships (XGBoost / Random Forest / Gradient Boosting).
- Model evaluation with RMSE, MAE, and R² + feature-importance interpretation.

## Data
This project expects the raw dataset file:

- `data/raw/MasterData.xlsx`

**The dataset is not included** (often too large and/or has licensing constraints).  
If you have the file locally, place it at the path above and run the notebook.

Data sources referenced in the report include Fingrid (renewables & balancing market), Nord Pool (day-ahead prices), and Statistics Finland (gas prices).

## Setup
### pip
```bash
python -m venv .venv
# Windows: .venv\Scripts\activate
# macOS/Linux: source .venv/bin/activate
pip install -r requirements.txt
```

### Run
```bash
jupyter lab
```
Open:
- `electricity_price_prediction_project.ipynb`

## Results (summary)
Models generally predict typical price ranges well, while **extreme price spikes** are harder to capture with the available features. See `electricity_price_prediction_report.pdf` for discussion and metrics.