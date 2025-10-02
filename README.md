Machine Data Analysis (Time Series)

This repository contains a comprehensive pipeline for analyzing industrial machine data using time series techniques. It demonstrates practical applications of data preprocessing, exploratory analysis, clustering, anomaly detection, and short-term forecasting on high-frequency sensor data.

Key Features

Data Loading and Preprocessing

Handles large time series datasets (hundreds of thousands of rows).

Resamples to a strict time grid (e.g., 5-minute intervals).

Cleans and handles missing values.

Generates summary statistics and visualizations.

Shutdown and Idle Period Detection

Detects periods where machines are shut down or idle based on sensor thresholds.

Computes total downtime and duration statistics.

Visualizes shutdowns over time.

Machine State Segmentation (Clustering)

Excludes shutdown periods and clusters operational data using KMeans (or other clustering algorithms).

Assigns interpretable states (e.g., Normal, High Load, Startup/Shutdown).

Provides cluster-level summary statistics and typical behavior.

Contextual Anomaly Detection

Detects anomalies conditioned on machine state clusters using Isolation Forest or statistical methods.

Produces detailed anomalous event reports including time, duration, and implicated variables.

Supports root-cause analysis by correlating anomalies with machine state and sensor data.

Short-Horizon Forecasting

Forecasts key machine variables (e.g., Cyclone_Inlet_Gas_Temp) for the next 1 hour using multiple approaches:

Persistence baseline

ARIMA model

RandomForest or LSTM on lag features

Evaluates forecasts with RMSE and MAE.

Handles challenges such as regime changes, shutdowns, and non-stationarity.

Outputs and Visualization

Saves CSV reports for shutdown periods, clusters summary, anomalies, and forecasts.

Generates visualizations for correlations, shutdown timelines, cluster behavior, and forecasting results.

Technologies and Libraries

Python 3.x

Data manipulation: pandas, numpy

Time series models: statsmodels (ARIMA), scikit-learn (RandomForest, KMeans, IsolationForest)

Visualization: matplotlib, seaborn

Excel input/output: openpyxl

Usage

Load your machine data (Excel/CSV) with a timestamp column and sensor variables.

Run the pipeline step by step: preprocessing → shutdown detection → clustering → anomaly detection → forecasting.

Inspect CSV outputs and visualizations for operational insights.

Applications

Predictive maintenance

Industrial process monitoring

Sensor-based anomaly detection

Time series forecasting for operational optimization# Machine-Data-Analysis-Time-Series-
Time series analysis of industrial machine data, including shutdown detection, operational state clustering, contextual anomaly detection, and short-term forecasting. Provides visualizations, summary stats, and CSV reports to support predictive maintenance and process optimization.
