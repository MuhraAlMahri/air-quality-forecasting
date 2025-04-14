# Probabilistic Air Quality Forecasting with Bayesian Inference

This project forecasts PM10 pollution levels in Abu Dhabi and Dubai using time series models—ARIMA and Gaussian Process Regression (GPR)—to offer both point predictions and uncertainty estimates.

## 📊 Dataset

- Source: UAE Federal Competitiveness and Statistics Center
- Years: 2011–2022
- Cities: Abu Dhabi, Dubai

## 🧠 Modeling

- **ARIMA (1,1,1)**: Classical forecasting method
- **Gaussian Process Regression (RBF Kernel)**: Bayesian method with 95% credible intervals

## 🔍 Results

| City        | ARIMA Forecast (2023) | GPR Forecast (2023, 95% CI)         |
|-------------|-----------------------|-------------------------------------|
| Abu Dhabi   | 135.62 µg/m³          | 136.91 µg/m³ [121.9 – 151.9]        |
| Dubai       | 129.75 µg/m³          | 127.58 µg/m³ [110.2 – 144.7]        |

## 📁 Structure

- `notebooks/` – Final Jupyter notebook
- `data/` – Cleaned and interpolated datasets
- `report/` – Project report in Word
- `src/` – Optional Python scripts for model reuse

## ⚙️ Requirements

```bash
pip install -r requirements.txt
