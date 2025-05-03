# 🌫️ Air Quality Forecasting with Probabilistic Models

**Authors**: Muhra ALMahri, Ayesha AlHammadi  
**Course**: ML703 – Probabilistic and Statistical Inference  
**Institution**: Mohamed bin Zayed University of Artificial Intelligence (MBZUAI), Abu Dhabi

---

## 📌 Project Overview

This project focuses on forecasting PM2.5 air pollution levels in Delhi using three distinct time series models:

- **ARIMA**: A classical statistical model for time series forecasting.
- **Bayesian Structural Time Series (BSTS)**: A probabilistic model that incorporates uncertainty estimation.
- **Gaussian Process Regression (GPR)**: A non-parametric model capable of capturing complex, non-linear relationships.

Our objective is to compare these models in terms of predictive accuracy and their ability to quantify uncertainty, which is crucial for public health decision-making.

---

## 📊 Dataset

- **Source**: [Kaggle](https://www.kaggle.com/)
- **Location**: Anand Vihar monitoring station, Delhi, India
- **Timeframe**: 2004–2019
- **Features**: Hourly PM2.5 measurements
- **Preprocessing**:
  - Aggregated hourly data to daily averages
  - Interpolated missing values
  - Normalized time indices for modeling

---

## 🧠 Methodology

### 1. ARIMA (AutoRegressive Integrated Moving Average)
- **Configuration**: SARIMA (2,1,2)(1,1,1,30)
- **Characteristics**:
  - Captures linear trends and seasonality
  - Does not provide uncertainty estimates

### 2. BSTS (Bayesian Structural Time Series)
- **Implementation**: PyMC
- **Components**:
  - Local linear trend
  - Gaussian noise
- **Advantages**:
  - Provides posterior distributions
  - Quantifies uncertainty through credible intervals

### 3. GPR (Gaussian Process Regression)
- **Kernel**: RationalQuadratic
- **Input**: Normalized time index
- **Pros**:
  - Captures non-linear trends
  - Provides confidence intervals
- **Cons**:
  - Sensitive to kernel choice
  - Computationally intensive for large datasets

---

## 📈 Results

### Evaluation Metrics

| Model   | RMSE  | MAE   |
|---------|-------|-------|
| ARIMA   | 6.01  | 4.98  |
| BSTS    | 4.35  | 3.43  |
| GPR     | 16.00 | 15.39 |


---

## 🧾 Conclusion

- **ARIMA** serves as a reliable baseline but lacks uncertainty quantification.
- **BSTS** provides a balance between accuracy and interpretability, making it suitable for policy-making scenarios.
- **GPR** demonstrates the importance of incorporating additional features for improved performance.

---

## 🔭 Future Work

- Incorporate exogenous variables (e.g., weather data) to enhance model performance.
- Explore advanced kernel functions for GPR to better capture complex patterns.
- Develop ensemble models combining the strengths of ARIMA, BSTS, and GPR.
- Extend the forecasting horizon beyond 30 days to assess long-term predictions.

---

## 🛠️ Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/MuhraAlMahri/air-quality-forecasting.git
   cd air-quality-forecasting
   ```

2. Install the required packages:
   ```bash
   pip install -r requirements.txt
   ```

---

## 📁 Repository Structure

```
air-quality-forecasting/
├── data/                   # Contains the dataset
├── figures/                # Generated plots and figures
├── notebooks/              # Jupyter notebooks for analysis
├── requirements.txt        # List of required Python packages
└── README.md               # Project overview and documentation
```

---

## 📄 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
