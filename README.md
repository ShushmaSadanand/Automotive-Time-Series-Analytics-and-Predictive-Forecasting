# Automotive Time-Series Analytics: Matrix Profile Anomaly Detection & ARIMA Forecasting

Welcome to the Time-Series Econometrics and Predictive Financial Operations division of my portfolio. This repository houses a production-grade analytics pipeline engineered to ingest raw transactional automotive ledger data, perform rigorous exploratory trend breakdowns, detect hidden operational anomalies, and deploy predictive forecasting frameworks to optimize multi-million-dollar supply chain and cash-flow horizons.

---

## Project Architecture & Business Intelligence
**Files:** `Managerial_Statistics_GrpWork.pdf` (Executive Analysis Deck) | `Car_Sales_Time_Series_Managerial_Statistics.ipynb` (Phase 1 Anomaly Pipeline) | `Car_Sales_2_Revenue_&_Cash_Flow_(ARIMA).ipynb` (Phase 2 Forecasting Script)

Volatile consumer automotive demand makes traditional static inventory management highly inefficient, leading to either capital-draining overstocking or margin-losing stockouts. This framework solves this dilemma through a dual-phase predictive architecture.

### Phase 1: Matrix Profile Anomaly & Structural Trend Diagnosis
Before fitting predictive models, the pipeline screens the historical baseline data to differentiate standard seasonal behavior from genuine systemic shocks:
* **Matrix Profile Discord Discovery:** Implemented a rolling 30-day structural window scan to pinpoint the top 5 unique transactional anomalies ("Discords") across historical sales.
* **Root-Cause Verification:** Successfully isolated major non-seasonal revenue outliers driven by systemic factors (e.g., specific high-value commercial fleet transactions, holiday closing halts, or geographic dealer region reporting shocks).
* **Stationarity Transformation Framework:** Conducted the **Augmented Dickey-Fuller (ADF)** test to diagnose non-stationary baselines. Applied first-order statistical differencing ($d=1$) to stabilize variance and remove long-term macroeconomic trends, preparing the clean data stream for linear modeling.

---

### Phase 2: Econometric ARIMA Modeling & Inventory Integration

Using cleaned daily and weekly aggregated transaction streams, the engine constructs a predictive trajectory to inform operational leadership decisions.

#### 1. Mathematical Autocorrelation Tuning
Evaluated optimal model parameters by mapping the **Autocorrelation Function (ACF)** and **Partial Autocorrelation Function (PACF)** boundaries:
* **ACF Log Interpretation:** Showed a single significant initial spike outside the 95% confidence interval before abruptly dropping off, indicating moving average behavior $\longrightarrow q=1$.
* **PACF Log Interpretation:** Exhibited sharp early structural lags before trailing off, confirming autoregressive dependence $\longrightarrow p=1$.
* **Final Configured Order:** Fitted an exact **$\text{ARIMA}(1, 1, 1)$** predictive model. Residual analysis confirmed white noise errors centered tightly at zero with no remaining serial autocorrelation.

#### 2. Managerial Inventory Strategy & Capital Forecasting
The mathematical forecasting boundaries are automatically mapped to physical capital requirements over a 30-day planning horizon:
* **Expected Base Demand:** Predicts a total demand volume of **1,812 units** ($\approx 60 \text{ units/day}$).
* **Supply Chain Safety Buffer:** Factoring in a 10% risk-mitigation safety stock, the framework provides an exact operational recommendation of **1,993 total warehouse units** to prevent stockouts while preserving optimal corporate capital liquidity.
* **Financial Cash-Flow Forecasting:** Translates unit volumes into weekly revenue expectations, giving accounting teams clear bounds to plan supplier payables, marketing allocations, and baseline cash reserves.

---

## Technical Competencies & Tooling
* **Time-Series Econometrics:** ARIMA Modeling ($\text{ARIMA}(1,1,1)$), Augmented Dickey-Fuller (ADF) Unit-Root Testing, First-Order Differencing.
* **Signal Anomaly Detection:** Matrix Profile Analytics, Window-Based Distance Profiles, Discord Extraction.
* **Mathematical Optimization Ecosystem:** Python 3, Pandas, NumPy, Statsmodels Library, SciPy Statistics.
* **Data Visualization & Diagnostics:** Custom ACF/PACF Plotting, Rolling Mean Windows, Residual Density Histograms, Outlier Spatial Projections (Matplotlib / Seaborn).
