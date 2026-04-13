# The Impact of Fuel Price Shock on Food Inflation in the United Kingdom

--------------


## Introduction

In the United Kingdom, fuel price shocks act as a significant cost amplifier across the food supply chain, driving up production and transportation costs, with retail food prices typically following with a lag of six to nine months. Food price shocks penetrate the supply chain through several interconnected channels, including the energy-intensive nature of modern agriculture, fertiliser dependency, logistics and distribution, and manufacturing and processing costs.


These combined pressures directly reshape consumer behaviour and market availability, leading to demand destruction, defensive shopping strategies, supply gaps, and a pronounced household squeeze. Ongoing tensions in the Middle East have intensified these pressures further, prompting industry bodies such as the Food and Drink Federation (FDF) to revise food inflation forecasts upward to at least 9% by the end of the year.





## Overview

This project investigates how **fuel price shocks in the UK transmit into food inflation and household demand behaviour**. It combines econometric modelling, time-series analysis, and demand estimation to understand:

- How quickly fuel price shocks affect food prices
- How strong the transmission is
- Which food categories are most affected
- How consumer demand responds to rising prices





## Research Question

> **How do fuel price shocks affect food prices and demand in the United Kingdom?**

**Simplified version:**
- When fuel prices rise, how long before food prices increase?
- How big is the impact?
- How do households adjust consumption?






## Objectives

- Model lagged impact of fuel prices on UK food CPI
- Measure transmission timing and peak response
- Identify heterogeneous effects across food categories
- Estimate demand response to price changes
- Test long-run equilibrium relationships







## Methodology Pipeline

**1. Exploratory Analysis**
- Pearson Correlation Matrix
- Cross-Correlation Function (CCF)
- Lag identification (0–12 months)


**2. Stationarity & Cointegration**
- Augmented Dickey-Fuller (ADF) Test
- Johansen Cointegration Test


**3. Lag Selection**
- Akaike Information Criterion (AIC)
- Bayesian Information Criterion (BIC)

✔ Purpose: Identify optimal lag structure for VAR/VECM models


**4. Econometric Models**

*Vector Autoregression (VAR)*
Captures dynamic interdependence between:
- Fuel prices (ULSP, ULSD)
- Food CPI
- Macroeconomic variables (Income, FX)

*🔗 Vector Error Correction Model (VECM)*
Used to model:
- Long-run equilibrium relationships
- Short-run deviations and corrections


**5. Sensitivity Analysis**

- Pass-through elasticity estimation using log-log models
- Comparison of fuel types (ULSP vs ULSD)
- Food category-level response analysis

✔ Purpose: Identify which food categories are most sensitive to fuel price shocks and measure heterogeneity in transmission strength






## Tools & Technologies

*Excel → Python (Statistical & Econometric Analysis) → Power BI (Interactive Visual Analytics)*


**Micorsoft Excel**
Used for:
- Initial data cleaning and formatting
- Quick descriptive statistics
- Data validation and preprocessing before Python modelling


**Python (Core Analysis)**
Used for:
- Data preprocessing (pandas, numpy)
- Statistical modelling (statsmodels)
- VAR / VECM estimation
- Granger causality tests
- Impulse Response Functions (IRF)
- Forecast Error Variance Decomposition (FEVD)
- Regression analysis (OLS, log-linear demand models)


**Power BI (Data Visualisation)**
Used for:
- Cross-correlation visualisations (CCF analysis)
- Sensitivity heatmaps (fuel vs food categories)
- IRF line charts (shock transmission over time)
- Elasticity comparison charts


**Statistical Libraries**
- `pandas` → data manipulation
- `numpy` → numerical operations
- `statsmodels` → econometric models (VAR, VECM, OLS)
- `matplotlib` / `seaborn` → exploratory plots



## Dataset

This project uses a structured monthly time-series dataset combining UK fuel prices, food inflation, and macroeconomic indicators.

📁 Location: `/data/`

The dataset is fully reproducible and organised into:
- Raw data (source extraction)
- Processed data (cleaned and aligned)
- Model-ready data (log-transformed for econometric analysis)



## Visualisation: 






## 📈 Key Findings

- Fuel price shocks affect UK food prices with a lag of approximately 6–9 months  
- Diesel (ULSD) has a stronger transmission effect on food inflation than petrol (ULSP)  
- Food categories such as fish, bread, and vegetables show the highest sensitivity to fuel price changes 
- Food demand decreases significantly as prices rise (negative price elasticity)  
- Strong long-run cointegration exists between fuel prices and food CPI  
- Fuel prices Granger-cause food inflation, confirming predictive causality


## Model Results Summary

| Model | Key Result |
|------|-----------|
| CCF Analysis | Peak correlation at 6–9 month lag |
| Granger Causality | Fuel → Food CPI (Highly Significant) |
| VAR Model | Strong dynamic interdependence detected |
| VECM | Long-run equilibrium confirmed |
| OLS Demand Model | Food CPI elasticity = -0.19 |
| Sensitivity Analysis | Fish & Bread most fuel-sensitive categories |




## Result Interpretation

- Rising fuel prices increase food production and logistics costs, leading to delayed but persistent food inflation
- Diesel price movements are a stronger predictor of food inflation than petrol
- Certain food categories (e.g., fish and bread) are disproportionately affected, creating targeted inflation pressure
- Households respond by reducing consumption and shifting toward cheaper substitutes during high inflation periods
