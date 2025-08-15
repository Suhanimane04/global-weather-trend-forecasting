# Weather Trend Forecasting – Technical Assessment Report

## Objective
Analyze and forecast weather trends using the **Global Weather Repository** dataset.  
Tasks included:
- Data cleaning and preprocessing.
- Exploratory Data Analysis (EDA).
- Forecasting with multiple models.
- Advanced analysis (anomalies, feature importance, spatial mapping, environmental impact).

---

## 1. Dataset Summary
- **Source**: Kaggle – Global Weather Repository
- **Rows**: 88,663
- **Columns**: 41
- **Time Range**: 2024-05-16 to 2025-08-15
- **Geographic Coverage**: Global (multiple countries and cities)
- **Key Features**:  
  - Temperature (Celsius/Fahrenheit)  
  - Precipitation (mm/in)  
  - Air Quality (PM2.5, PM10, CO, Ozone, NO2, SO2)  
  - Wind, humidity, pressure, cloud cover  
  - Sunrise/Sunset, Moon phase

---

## 2. Data Cleaning & Preprocessing
- Parsed `last_updated` into datetime.
- Dropped rows with invalid or missing dates.
- Filled missing numeric values with median.
- Filled missing categorical values with mode.
- Removed duplicates.
- Normalized numeric values where required.

---

## 3. Exploratory Data Analysis (EDA)
- **Temperature Trends**: Seasonal variation observed across different continents.
- **Precipitation Trends**: Rainfall peaks in tropical regions.
- **Correlation Matrix**:  
  - Temperature inversely correlated with humidity.  
  - PM2.5 positively correlated with PM10 and NO2.
- **Visualization**:  
  - Line plots for temperature and precipitation.  
  - Heatmaps for correlations.

---

## 4. Forecasting Models
**Target Variable**: `temperature_celsius`

Models used:
1. **SARIMA** – Captures time-series trends and seasonality.
2. **Random Forest Regressor** – Captures nonlinear patterns using multiple features.
3. **Ensemble (SARIMA + RF)** – Improves accuracy by averaging predictions.

**Performance (RMSE)**:
| Model       | RMSE  |
|-------------|-------|
| SARIMA      | 5.29  |
| RandomForest| 1.41  |
| Ensemble    | 2.79  |

---

## 5. Advanced Analyses
### Anomaly Detection
- **Method**: Isolation Forest  
- Outliers detected in extremely high PM2.5 and PM10 readings.

### Feature Importance
- Most important features for temperature prediction:  
  1. Latitude  
  2. Longitude  
  3. PM2.5  
  4. Humidity  

### Spatial Analysis
- **Tool**: Plotly Choropleth  
- Created global heat map showing average temperature by country.

### Environmental Impact
- Higher PM2.5 concentrations linked with lower average temperatures in certain regions.
- Positive correlation between PM10 and industrial areas.

---

## 6. Key Insights
- Temperatures vary more by **latitude** than longitude.
- Tropical countries have more consistent high humidity.
- Air quality parameters are valuable predictors for urban temperature modeling.
- Ensemble model gave better balanced performance than single models.

---

## 7. Next Steps
- Add deep learning models (LSTM, Prophet) for better long-term forecasts.
- Incorporate external datasets (population density, industrial emissions).
- Deploy as an interactive dashboard.

---

## PM Accelerator Mission
*"Building products and insights powered by AI to solve real-world problems and make data-driven de