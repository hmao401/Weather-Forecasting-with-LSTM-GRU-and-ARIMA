# Data-Driven Forecasting of Climate and Weather Using LSTM and XGBoost
This project investigated the use of machine learning and deep learning techniques for climate and weather forecasting, focusing on LSTM networks and XGBoost regression. Using the Global Historical Climatology Network (GHCN-Daily) dataset from Arctic Bay, Canada (1999–2021), I preprocessed daily meteorological data (temperature, precipitation) by handling missing values, scaling, and engineering lagged and calendar features.
Models Implemented:
LSTM: Sequence-based forecasting with sliding windows, designed to capture temporal dependencies.
XGBoost: Gradient-boosted trees applied to lagged features and cyclical time encodings.
Forecasting Tasks:
Climate (monthly averages): Long-term seasonal trends.
Weather (daily values): Short-term, high-frequency fluctuations.
Key Results:
XGBoost consistently outperformed LSTM for both monthly and daily forecasts, achieving near-perfect scores (MAE = 0.28 for monthly, 0.05 for daily).
LSTM generalized better in long-term and multi-station scenarios but struggled with data sparsity and extremes.
Visual analyses showed XGBoost replicated sharp transitions, while LSTM smoothed seasonal cycles.
Extensions: Conducted long-range (20-year) projections, spatial climate comparisons across global stations, and correlation analyses to investigate teleconnections and spatial coherence.
This study highlights the trade-offs between tree-based ensemble models and recurrent neural networks in environmental time series forecasting, showing the potential of hybrid data-driven approaches to complement traditional physics-based methods.
