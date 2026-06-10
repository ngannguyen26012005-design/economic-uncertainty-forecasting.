# Economic Uncertainty Forecasting: A Comparative Time Series Analysis of Sweden's Economic Policy Uncertainty Index

## Project Overview

This project develops a time series forecasting framework for Sweden's Economic Policy Uncertainty (EPU) Index using monthly data obtained from the Policy Uncertainty Database. The study evaluates the forecasting performance of classical smoothing methods and seasonal stochastic models under periods of heightened macroeconomic uncertainty.

The primary objective is to compare the predictive accuracy of Moving Average (MA), Weighted Moving Average (WMA), and Seasonal Autoregressive Integrated Moving Average (SARIMA) models and identify the most suitable approach for forecasting economic uncertainty.



## Dataset Description

**Data Source:** Policy Uncertainty Database

**Indicator:** Sweden Economic Policy Uncertainty (EPU) Index

**Frequency:** Monthly

**Time Span:** 2006 – Present

The EPU index measures the level of uncertainty surrounding economic policy decisions and is widely used as a proxy for macroeconomic instability, policy-related risk, and market sentiment.



## Key Skills Demonstrated

- Time Series Analysis
- Economic Forecasting
- Seasonal Decomposition
- Stationarity Assessment
- Outlier Detection
- Forecast Model Evaluation
- SARIMA Modeling
- Moving Average Techniques
- Python for Financial Analytics


## Exploratory Data Analysis (EDA)

Several exploratory analyses were conducted to understand the characteristics of the EPU series:

### Outlier Analysis

Twelve major structural outliers were identified, corresponding to significant economic events such as:

- Global Financial Crisis (2008)
- European Sovereign Debt Crisis
- COVID-19 Pandemic (2020)

Rather than removing these observations, they were retained because they represent genuine economic shocks and contain important information regarding uncertainty dynamics.

### Trend and Seasonality

- Visualized long-run movements in economic uncertainty.
- Applied seasonal decomposition techniques to separate trend, seasonal, and residual components.
- Examined the persistence of volatility across different economic periods.

### Data Partitioning

The dataset was chronologically divided into:

- Training Set: 80%
- Testing Set: 20%

This approach preserves temporal ordering and provides a realistic out-of-sample forecasting evaluation.



## Forecasting Models

### 1. Seasonal ARIMA (SARIMA)

The SARIMA model was implemented to capture:

- Autoregressive dynamics
- Moving average components
- Differencing effects
- Seasonal patterns

A grid-search procedure was employed to identify the optimal parameter specification.

### 2. Simple Moving Average (MA)

A baseline forecasting model using rolling averages to smooth short-term fluctuations in the EPU series.

### 3. Weighted Moving Average (WMA)

An enhanced smoothing approach assigning greater weight to recent observations, allowing the model to react more rapidly to changing economic conditions.

---

## Model Evaluation

Forecast accuracy was assessed using four standard performance metrics:

- Mean Squared Error (MSE)
- Mean Absolute Deviation (MAD)
- Root Mean Squared Error (RMSE)
- Mean Absolute Percentage Error (MAPE)

### Performance Comparison

| Model | MSE | MAD | RMSE | MAPE |
|--------|--------:|--------:|--------:|--------:|
| SARIMA | 25123.72 | 120.90 | 158.50 | 66.17% |
| Moving Average (MA) | 5410.34 | 53.30 | 73.56 | 41.22% |
| Weighted Moving Average (WMA) | **4190.03** | **46.32** | **64.73** | **35.38%** |



## Key Findings

### Best Performing Model

The Weighted Moving Average (WMA) achieved the strongest forecasting performance across all evaluation metrics.

- Lowest MSE: 4190.03
- Lowest MAD: 46.32
- Lowest RMSE: 64.73
- Lowest MAPE: 35.38%

### Economic Interpretation

The results suggest that localized smoothing approaches may outperform more complex stochastic models when forecasting economic uncertainty during periods of rapid structural change.

While SARIMA effectively captures long-term seasonal behavior, its forecasts may respond more slowly to sudden macroeconomic shocks. In contrast, WMA places greater emphasis on recent observations, enabling faster adaptation to changing economic conditions.



## Practical Implications

Accurate forecasting of economic policy uncertainty can support:

- Macroeconomic monitoring
- Risk management
- Financial market analysis
- Investment decision-making
- Policy evaluation

The findings indicate that adaptive forecasting methods may provide valuable short-term predictive insights during periods of elevated economic volatility.



## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Statsmodels
- Scikit-learn
- Jupyter Notebook



## Repository Structure

```text
├── Economic_Uncertainty_Forecasting.ipynb
├── Project_Report.pdf
├── README.md
└── data/
```

### File Description

**Economic_Uncertainty_Forecasting.ipynb**
- Data preprocessing
- Exploratory data analysis
- Time series decomposition
- Forecast model implementation
- Performance evaluation

**Project_Report.pdf**
- Full project report
- Methodology discussion
- Forecasting results

**README.md**
- Project overview and documentation



## Author

Nguyen Thai Ngan

Bachelor of Economic Mathematics

University of Economics and Law (UEL)

Research Interests:
- Time Series Analysis
- Financial Mathematics
- Economic Forecasting
- Machine Learning
- Risk Analytics
- Operational Research
