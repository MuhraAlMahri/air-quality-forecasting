# 🌫️ Probabilistic Air Quality Forecasting with Bayesian Inference

This project focuses on forecasting PM2.5 air pollution levels in Delhi using three distinct time series models:
	•	ARIMA: A classical statistical model for time series forecasting.
	•	Bayesian Structural Time Series (BSTS): A probabilistic model that incorporates uncertainty estimation.
	•	Gaussian Process Regression (GPR): A non-parametric model capable of capturing complex, non-linear relationships.

Our objective is to compare these models in terms of predictive accuracy and their ability to quantify uncertainty, which is crucial for public health decision-making.


## 📁 Project Structure
```
air-quality-forecasting/
│
├── README.md                     ← Project summary, motivation, models
├── requirements.txt              ← Dependencies (e.g., numpy, matplotlib, pymc, etc.)
├── ML703_air_quality.ipynb      ← Main notebook (clean, commented)
├── air-quality-india.csv         ← Cleaned version (optional)
```


## 📈 Dataset

- Source: **UAE Federal Competitiveness and Statistics Center (FCSC)**
- Years: **2011–2022**
- Variables: Annual average PM10 concentrations per city
- Missing values for 2012 were interpolated

<br>

## 🧠 Models Implemented

### 1. ARIMA (1,1,1)
- Classical time series model
- No uncertainty estimates

### 2. Gaussian Process Regression (GPR)
- Bayesian method using an RBF kernel
- Generates predictive distributions with **95% credible intervals**

<br>

## 🔍 Forecast Results (2023)

| City        | ARIMA Forecast (µg/m³) | GPR Forecast (µg/m³, 95% CI)        |
|-------------|------------------------|-------------------------------------|
| Abu Dhabi   | 135.62                 | 136.91 [121.9 – 151.9]              |
| Dubai       | 129.75                 | 127.58 [110.2 – 144.7]              |

<br>

## 📦 How to Run

1. Clone the repo:
   ```bash
   git clone https://github.com/MuhraAlMahri/air-quality-forecasting
   cd air-quality-forecasting
2. Create a virtual environment (optional but recommended):
   ```bash
   python -m venv venv
   source venv/bin/activate  # or venv\Scripts\activate on Windows
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
4. Run the notebook:
   ```bash
   jupyter notebook notebooks/ML_project_completed.ipynb

## 📚 References
	•	Rasmussen, C.E., & Williams, C.K.I. (2006). Gaussian Processes for Machine Learning. MIT Press.
	•	Hyndman, R.J., & Athanasopoulos, G. (2018). Forecasting: Principles and Practice.
	•	UAE Federal Competitiveness and Statistics Center (2022)


## ✨ Developed by Ayesha Alhammadi and Muhra AlMahri
## 📘 Course: ML703 – Probabilistic and Statistical Inference, Spring 2025
