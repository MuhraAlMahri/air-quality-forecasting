# 🌫️ Probabilistic Air Quality Forecasting with Bayesian Inference

This project forecasts PM10 air pollution levels in **Abu Dhabi** and **Dubai** using both classical and probabilistic time series models. We implement and compare **ARIMA** and **Gaussian Process Regression (GPR)** to not only predict pollutant concentrations, but also quantify forecast uncertainty—an essential aspect of environmental risk analysis.


## 📁 Project Structure

├── notebooks/
│   └── ML_project_completed.ipynb       ← main notebook
├── report/
│   └── Air_Quality_Report.docx          ← detailed writeup
├── data/
│   ├── average-of-air-pollutants-concentration-2011-2022.xlsx  ← raw dataset
│   └── Interpolated_PM10_Levels.csv     ← cleaned/interpolated data
├── requirements.txt                     ← dependencies
└── README.md                            ← this file



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
