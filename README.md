# How Fuel Prices Drive Food Inflation in the United Kingdom

---

## Table of Contents

- [Project Overview](#project-overview)
- [Research Question](#research-question)
- [Objectives](#objectives)
- [Datasets](#datasets)
- [Methodology Pipeline](#methodology-pipeline)
- [Tools & Workflow](#tools--workflow)
- [Dashboard Visualisations](#dashboard-visualisations)
- [Model Results](#model-results)
- [Key Findings](#key-findings)
- [Policy Implications](#policy-implications)
- [Economic Interpretation](#economic-interpretation)
- [Author](#author)

---

## Project Overview

This project examines how fuel price shocks transmit into UK food inflation using time-series econometric modelling and data visualisation.

The analysis combines economic theory with empirical modelling to quantify:

- Transmission delays (lag structure)
- Magnitude of fuel-to-food price pass-through
- Structural relationships across macroeconomic variables
- Consumer demand response under inflationary pressure

The workflow integrates Python-based econometric analysis with Power BI dashboards to translate statistical results into policy-relevant insights.

---

## Research Question

> How do fuel price shocks affect food prices and household demand in the United Kingdom?

### Sub-questions
- What is the lag between fuel price shocks and food inflation responses?
- How strong is the transmission effect?
- Which food categories are most sensitive?
- How do households adjust consumption under price shocks?

---

## Objectives

- Estimate lagged transmission from fuel prices to food CPI  
- Identify short-run and long-run inflation dynamics  
- Measure pass-through intensity across fuel types  
- Analyse heterogeneity across food categories  
- Estimate demand elasticities under inflationary conditions  
- Test long-run equilibrium relationships between fuel and food prices  

---

## Datasets

### 1. Macroeconomic Time-Series Dataset
Monthly UK data including:
- Fuel prices (ULSP, ULSD, Brent Crude)
- Food CPI and sub-indices
- Income and exchange rates

📁 `Full dataset for Food and fuel price analysis(Sheet1).csv`

---

### 2. Econometric Output Dataset
Model-generated outputs used for interpretation:
- VAR/VECM estimates  
- Impulse Response Functions (IRFs)  
- Elasticity estimates  
- Diagnostic statistics  

📁 `IMPACT OF FUEL SHOCK ON FOOD PRICE ANALYSIS RESULT.xlsx`

---

## Methodology Pipeline

### 1. Exploratory Analysis
- Correlation analysis  
- Cross-correlation functions (CCF)  
- Lag structure identification (0–12 months)

---

### 2. Time-Series Diagnostics
- Stationarity testing (ADF)  
- Cointegration testing (Johansen)

---

### 3. Model Selection Strategy
- Optimal lag selection using AIC/BIC  
- Structural specification of VAR system  

---

### 4. Econometric Modelling

**VAR (Vector Autoregression)**  
Used for capturing short-run dynamic interactions between:
- Fuel prices (ULSP, ULSD)
- Food CPI
- Macroeconomic controls (income, exchange rate)

**VECM (Vector Error Correction Model)**  
Estimated after confirming cointegration to capture:
- Long-run equilibrium relationships  
- Short-run adjustment dynamics  

> **Model justification:** Johansen cointegration results indicated at least one cointegrating relationship, making VECM the appropriate specification rather than VAR in levels.

---

### 5. Sensitivity Analysis
- Log-log elasticity estimation  
- Fuel type comparison (ULSP vs ULSD)  
- Food category response differences  

---

### 6. Demand Estimation
- Log-linear OLS regression  
- Price and income elasticity estimation  

---

## Tools & Workflow

CSV / Excel → Python (Econometrics & Statistical Modelling) → Power BI (Dashboards & Visualisation)

---

## Dashboard Visualisations

### Overview
![Overview](Screenshot%20(1024).png)

### Food CPI Dynamics
![Food CPI](Screenshot%20(1030).png)

### Transmission Timing
![Timing](Screenshot%20(1027).png)

### Sensitivity Analysis
![Sensitivity](Screenshot%20(1028).png)

### Adjustment Behaviour
![Adjustment](Screenshot%20(1029).png)

---

## Model Results

> ⚠️ These results summarise previously estimated econometric outputs. Full statistical output is documented in the analysis Excel file.

| Test / Model | Key Result |
|--------------|------------|
| ADF Test | Variables non-stationary in levels, stationary in first differences |
| Johansen Cointegration | At least one cointegrating relationship detected |
| VAR Lag Selection | Optimal lag selected using AIC/BIC (see appendix file) |
| Granger Causality | Fuel prices Granger-cause food CPI |
| VECM | Significant error correction term confirming long-run adjustment |
| IRF Analysis | Peak response observed at ~6–9 month horizon |
| Demand Model | Price elasticity of food demand ≈ -0.19 |

---

## Key Findings

- Fuel price shocks affect food prices with a 6–9 month lag  
- Diesel (ULSD) has a stronger transmission effect than petrol (ULSP)  
- Fish, bread, and vegetables are the most sensitive food categories  
- Food demand falls in response to price increases (inelastic response)  
- A long-run equilibrium relationship exists between fuel and food prices  
- Fuel prices are a leading indicator of food inflation  

---

## Policy Implications

- Diesel prices should be monitored as an early warning indicator of food inflation  
- Temporary targeted subsidies may stabilise high-sensitivity food categories (e.g., bread, fish)  
- Fuel cost smoothing policies could reduce inflation volatility in food markets  
- Energy price shocks should be integrated into food security forecasting models  

---

## Economic Interpretation

Fuel price increases raise transportation and production costs across the food supply chain. This leads to delayed but persistent increases in food prices, particularly in logistics-intensive categories such as fish and bakery products. Household consumption adjusts downward due to negative demand elasticity, amplifying welfare impacts during inflationary periods.

---

## Author

✍️ Lauren Akhidenor
