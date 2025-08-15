# Global Weather Forecasting and Analysis

## Overview
This project analyzes the **Global Weather Repository** dataset and forecasts future weather trends using both basic and advanced techniques.  
The work satisfies the **PM Accelerator Technical Assessment** requirements for Data Scientists/Analysts.

## Dataset
Source: [Global Weather Repository on Kaggle](https://www.kaggle.com/datasets/nelgiriyewithana/global-weather-repository)  
Features: Daily weather observations for cities worldwide, including temperature, precipitation, air quality, sunrise/sunset, moon phase, etc.

## Project Structure
├── notebook.ipynb # Main Jupyter notebook with code and outputs
├── GlobalWeatherRepository.csv # Dataset
├── requirements.txt # Dependencies
└── README.md # Project documentation

## Steps Performed
### 1. Data Cleaning & Preprocessing
- Parsed `last_updated` into datetime.
- Filled missing numeric values with median, categorical with mode.
- Removed duplicates.
- Normalized numerical features.

### 2. Exploratory Data Analysis (EDA)
- Temperature and precipitation trends.
- Correlation matrix.
- Seasonal and geographic variations.

### 3. Forecasting Models
- **SARIMA**: For time-series forecasting.
- **Random Forest**: For regression-based forecasting.
- **Ensemble Model**: Averaging SARIMA and RF predictions.

### 4. Advanced Analyses
- **Anomaly Detection**: Using Isolation Forest.
- **Feature Importance**: Using Random Forest feature importance.
- **Spatial Analysis**: World map visualization of average temperature.
- **Environmental Impact**: Air quality vs weather correlation.

## Results
| Model       | RMSE   |
|-------------|--------|
| SARIMA      | 5.29   |
| RandomForest| 1.41   |
| Ensemble    | 2.79   |

## How to Run
1. Clone the repository:
```bash
git clone https://github.com/yourusername/global-weather-analysis.git
cd global-weather-analysis
