# Healthcare Lab Test Demand Forecasting

A demonstration project for monthly laboratory test demand forecasting using **ETS (Exponential Smoothing)** and **XGBoost**.

> **Data note:** This public repository uses synthetic/sample data for demonstration. No private or patient-level healthcare data is included.

## Objective

Forecast monthly demand for multiple laboratory tests and compare forecasting performance using walk-forward validation.

## Approach

1. Aggregate daily test volumes to monthly totals.
2. Use a 6-month validation window to compare ETS and XGBoost.
3. Select the model with the lower validation MAE for each test.
4. Generate monthly forecasts.
5. Evaluate forecasts with MAE, RMSE and Error %.
6. Visualize actual vs predicted demand.

## Models

- ETS / Holt-Winters Exponential Smoothing
- XGBoost Regressor

## Features used by XGBoost

- Lag 1, 2, 3, 6 and 12 months
- Rolling 3, 6 and 12 month averages
- Month
- Trend index

## Repository Structure

```text
healthcare-lab-test-forecasting/
├── README.md
├── lab_forecasting.ipynb
├── requirements.txt
├── data/
│   └── sample_lab_data.csv
├── results/
└── charts/
```

## How to Run

Install dependencies:

```bash
pip install -r requirements.txt
```

Open `lab_forecasting.ipynb` in Jupyter Notebook, JupyterLab, VS Code, or Google Colab and run the cells from top to bottom.

## Evaluation Metrics

- **MAE:** Average absolute difference between actual and predicted values.
- **RMSE:** Penalizes larger forecasting errors more strongly than MAE.
- **Error %:** Absolute percentage difference between actual and predicted values.

## Disclaimer

This repository is a portfolio demonstration. The sample dataset is synthetic and is not representative of any specific hospital, patient population, or healthcare organization.
