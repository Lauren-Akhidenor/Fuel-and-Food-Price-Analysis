# The Impact of Fuel Price Shocks on Food Inflation in the United Kingdom

---

## Table of Contents

- [Project Overview](#-project-overview)
- [Research Question](#-research-question)
- [Objectives](#-objectives)
- [📁 Datasets](#-datasets)
- [Methodology Pipeline](#️-methodology-pipeline)
- [Tools & Workflow](#-tools--workflow)
- [Dashboard Visualisations](#-dashboard-visualisations)
- [📈 Model Results Summary](#-model-results-summary)
- [🔍 Key Findings](#-key-findings)
- [Economic Interpretation](#-economic-interpretation)
- [📌 Author](#-author)

---

## Project Overview

This project investigates how fuel price shocks transmit into UK food inflation and household consumption behaviour using econometric time-series modelling and data visualisation.

It combines economic theory, statistical modelling, and data analytics to quantify:

- Transmission timing (lag effects)
- Magnitude of impact (elasticities & pass-through)
- Heterogeneity across food categories
- Consumer demand responses

The project is implemented using Python, Excel, and Power BI, forming an end-to-end analytical pipeline from raw data to interactive dashboards.

---

## Research Question

> How do fuel price shocks affect food prices and household demand in the United Kingdom?

### Sub-questions:
- How long after fuel price increases do food prices respond?
- How strong is the transmission effect?
- Which food categories are most affected?
- How do households adjust consumption behaviour?

---

## Objectives

- Model lagged transmission of fuel prices into UK food CPI  
- Identify timing and peak response of inflation effects  
- Measure fuel price pass-through intensity  
- Analyse heterogeneity across food categories  
- Estimate demand elasticity under price shocks  
- Test long-run equilibrium relationships between fuel and food prices  

---

## 📁 Datasets

### Primary Dataset (Time-Series Data)

Monthly UK macroeconomic data including:
- Fuel prices (ULSP, ULSD, Brent Crude)
- Food CPI and sub-indices
- Macroeconomic variables (income, exchange rates)

File: `Full dataset for Food and fuel price analysis(Sheet1).csv`

---

### Econometric Output Dataset

Model outputs used for analysis and visualisation:
- VAR / VECM estimates  
- Impulse Response Functions (IRFs)  
- Elasticity estimates  
- Residual diagnostics  

File: `IMPACT OF FUEL SHOCK ON FOOD PRICE ANALYSIS RESULT.xlsx`

---

## Methodology Pipeline

### 1. Exploratory Data Analysis
- Pearson correlation matrix  
- Cross-Correlation Function (CCF)  
- Lag identification (0–12 months)



### 2. Time Series Diagnostics
- Augmented Dickey-Fuller (ADF) test  
- Johansen cointegration test  



### 3. Model Specification
- AIC / BIC lag selection  
- Optimal VAR/VECM structure  



### 4. Econometric Modelling

**VAR (Vector Autoregression)**  
Captures dynamic interactions between:
- Fuel prices (ULSP, ULSD)
- Food CPI
- Income and exchange rates  

**VECM (Vector Error Correction Model)**  
Captures:
- Long-run equilibrium relationships  
- Short-run adjustments  



### 5. Sensitivity Analysis
- Log-log elasticity estimation  
- ULSP vs ULSD comparison  
- Food category response analysis  



### 6. Demand Estimation
- Log-linear OLS regression  
- Price and income elasticity estimation  

---

## Tools & Workflow

CSV / Excel → Python (Econometrics & Statistical Analysis) → Power BI (Interactive Dashboards)

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

## 📈 Model Results Summary

| Model | Key Result |
|------|-------------|
| Cross-Correlation (CCF) | Peak lag at 6–9 months |
| Granger Causality | Fuel → Food CPI (significant) |
| VAR Model | Strong dynamic interdependence |
| VECM | Long-run equilibrium confirmed |
| OLS Demand Model | Elasticity ≈ -0.19 |
| Sensitivity Analysis | Fish, bread most sensitive |

---

## 🔍 Key Findings

- Fuel price shocks affect food prices with a 6–9 month lag  
- Diesel (ULSD) has stronger transmission than petrol (ULSP)  
- Fish, bread, and vegetables are most sensitive categories  
- Food demand decreases as prices rise (negative elasticity)  
- Strong long-run cointegration exists between fuel and food inflation  
- Fuel prices are a strong predictor of food inflation  

---

## Economic Interpretation

Fuel price increases raise production and transportation costs, leading to delayed but persistent food inflation. Diesel prices have a stronger effect due to freight dependency. Households respond by reducing consumption and switching to cheaper alternatives during inflationary periods.

---


✍️ *Lauren Akhidenor*
