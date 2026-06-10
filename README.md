# economic-uncertainty-forecasting.
An empirical time series forecasting framework on the ECSU index using SARIMA, Moving Average, and WMA models to evaluate predictive accuracy under macroeconomic volatility.
# Forecasting Economic Volatility: An Empirical Comparative Analysis on the ECSU Dataset

## Project Overview
This project establishes a comprehensive econometric framework to model and forecast the **Economic Conditions and Policy Uncertainty (ECSU)** monthly index (spanning from 2006 to the present). Given that macroeconomic indicators are highly susceptible to global shocks, this research evaluates and compares the predictive performance of traditional statistical baselines against stochastic time series models under extreme market volatility.

---

## Data Description & Preparation
The ECSU dataset serves as a proxy for real-world economic uncertainty. The preprocessing and Exploratory Data Analysis (EDA) pipeline involves:
- **Outlier Preservation:** Identified 12 major structural outliers corresponding to systemic macroeconomic shocks (e.g., the 2008 Global Financial Crisis, the 2020 COVID-19 pandemic). These outliers were mathematically retained to preserve the genuine volatility signal of the economic time series.
- **Stationarity & Transformation:** Conducted data continuity checks and statistical transformations to stabilize the variance and ensure suitability for advanced time series algorithms.
- **Data Splitting:** Partitioned the data chronologically into an **80% Training Set** and a **20% Testing Set** to rigorously evaluate out-of-sample forecasting power and prevent overfitting.

---

## Econometric Methodologies & Models Deployed
Three distinct forecasting paradigms were implemented and optimized:
1. **SARIMA (Seasonal Autoregressive Integrated Moving Average):** Employed to capture long-term linear dependencies, structural trends, and complex seasonal dynamics inherent in global economic indices.
2. **Simple Moving Average (MA):** Utilized as a standard rolling baseline model to smooth out short-term random fluctuations.
3. **Weighted Moving Average (WMA):** Implemented using localized, weight-adjusted smoothing parameters to grant higher relevance to recent historical observations, accommodating rapid momentum shifts.

---

## Empirical Results & Quantitative Evaluation
Model performance was rigorously validated across four strict statistical error metrics: **Mean Squared Error (MSE)**, **Mean Absolute Deviation (MAD)**, **Root Mean Squared Error (RMSE)**, and **Mean Absolute Percentage Error (MAPE)**.

### Performance Summary Table:
| Forecasting Model | MSE | MAD | RMSE | MAPE (%) |
| :--- | :---: | :---: | :---: | :---: |
| **SARIMA (80% Train / 20% Test)** | 25123.72 | 120.90 | 158.50 | 66.17% |
| **Simple Moving Average** | 5410.34 | 53.30 | 73.56 | 41.22% |
| **Weighted Moving Average (WMA)** | **4190.03** | **46.32** | **64.73** | **35.38%** |

---

## Key Findings & Research Conclusion
- **Optimal Model Selection:** The empirical evidence demonstrates that the **Weighted Moving Average (WMA)** significantly out-performed both the simple Moving Average and the complex SARIMA model for this specific macroeconomic series, achieving the lowest error rates across all parameters (MSE: 4190.03, MAPE: 35.38%).
- **Economic Insight:** While global models like SARIMA capture long-term structural baselines well, they can exhibit rigid forecasting lags during periods of severe global instability. Conversely, weight-adjusted localized smoothing methods (WMA) possess **superior adaptive capabilities**, allowing them to respond faster to sudden structural macroeconomic shifts and transient market shocks.

---

## 📂 Project Structure
- `Economic_Uncertainty_Forecasting.ipynb` - Full Jupyter Notebook containing the end-to-end Python implementation (Data ingestion, EDA plots, Model training, Evaluation metrics, and Summary visualizations).
- `README.md` - Research overview and quantitative summary.
