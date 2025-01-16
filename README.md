# Sandika's Portfolio
#Energy-Consumption-in-Steel-Industry (https://github.com/Sandikadata/Energy-Consumption-in-Steel-Industry.git)

- **Data Taken**: 
  The data consists of hourly electricity consumption by the steel industry for an entire year (2018). It includes timestamps and corresponding energy usage (kWh) values, loaded from a CSV file from kaggle. 

- **Model Used**:  
  The analysis utilizes the **XGBoost Regressor** (`xgb.XGBRegressor`), a gradient-boosting algorithm specifically effective for time series and tabular data.

- **Algorithm Used**:  
  - Time series data is split into training (data before August 2018) and testing (data from August 2018 onward).  
  - **Features Created**: Time-based features such as hour, day of the week, month, quarter, and day of the year. These features provide temporal granularity for predictions.  
  - The XGBoost model is trained using these features to predict electricity consumption.  

- **Optimization**:  
  - The model is optimized with **1000 estimators** and a **learning rate of 0.01**.  
  - Early stopping is implemented with a patience of 50 rounds during evaluation.  
  - Feature importance analysis highlights the contribution of each feature.  

### Visualizations and Insights
- The energy usage peaks during morning hours (8 AM) and after lunch till 9 PM, while consumption drops around lunchtime.  
- Monthly and quarterly consumption trends were visualized, indicating seasonal energy demands.  
- Predictions are compared with actual values for both the entire year and specific date ranges.  

### Outcome  
- The model effectively forecasts energy consumption with an emphasis on understanding temporal patterns, which is visually validated against the test dataset.

