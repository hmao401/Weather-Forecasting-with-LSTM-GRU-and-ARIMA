# 🌍 Climate & Weather Forecasting with LSTM & XGBoost  

This project applies **machine learning** and **deep learning** to forecast temperature and precipitation in the Arctic. Using the **Global Historical Climatology Network (GHCN-Daily)** dataset from *Arctic Bay, Canada (1999–2021)*, I compare the performance of **XGBoost regression** and **LSTM networks** on both climate (monthly) and weather (daily) forecasting tasks.  

---

## 📂 Dataset  
- **Source:** [NOAA GHCN-Daily](https://www.ncei.noaa.gov/products/land-based-station/global-historical-climatology-network-daily)  
- **Region:** Arctic Bay, Canada (73°N, –85°W)  
- **Variables:** Daily TMAX, TMIN, PRCP (1999–2021)  
- **Preprocessing:**  
  - Missing value imputation (forward/backward fill)  
  - Log transformation of precipitation  
  - Lagged features & cyclical calendar features  
  - Min–Max scaling  

---

## 🛠️ Models Implemented  

- **LSTM (Deep Learning)**  
  - 30-day sliding window sequences  
  - Captured temporal dependencies & seasonal cycles  
  - Limitations: struggled with extremes & sparse precipitation  

- **XGBoost (Machine Learning)**  
  - Lagged features + cyclical encodings (month, day-of-week)  
  - Robust performance with minimal tuning  
  - Risk of overfitting on structured seasonal patterns  

---

## 🎯 Forecasting Tasks  

- **Climate (monthly averages)** → Long-term seasonal cycles  
- **Weather (daily values)** → High-frequency fluctuations  

---

## 📊 Key Results  

| Task | Model | MAE | R² | Notes |
|------|-------|-----|----|-------|
| Climate (monthly) | XGBoost | **0.28** | **1.00** | Captured peaks & transitions, risk of overfit |
| Climate (monthly) | LSTM | 1.45 | 0.64 | Smoothed cycles, underestimated extremes |
| Weather (daily)   | XGBoost | **0.05** | **1.00** | Replicated sharp transitions with high accuracy |
| Weather (daily)   | LSTM | 1.25 | 0.61 | Captured trends but missed high-frequency changes |

---

## 🔎 Extensions  

- 20-year long-range projections (LSTM)  
- Cross-station spatial comparisons  
- Correlation analyses (teleconnections & spatial coherence)  

---

## 📌 Key Insights  

- **XGBoost outperformed LSTM** on both tasks, especially in short-term forecasting  
- **LSTM generalized better** in multi-station and long-range contexts  
- Data-driven approaches can complement traditional physics-based forecasting models  

---

## 🚀 Tech Stack  

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)  ![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)  ![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)  ![Matplotlib](https://img.shields.io/badge/Matplotlib-00599C?style=for-the-badge&logo=plotly&logoColor=white)  ![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)  ![XGBoost](https://img.shields.io/badge/XGBoost-00599C?style=for-the-badge&logo=github&logoColor=white)  ![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white)  

---


