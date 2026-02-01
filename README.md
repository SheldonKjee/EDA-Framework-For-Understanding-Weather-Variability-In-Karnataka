# 🌦️ EDA Framework: Weather Variability in Karnataka

**Author:** Sheldon Khongjee  
**GitHub:** [SheldonKjee/EDA-Framework-For-Understanding-Weather-Variability-In-Karnataka](https://github.com/SheldonKjee/EDA-Framework-For-Understanding-Weather-Variability-In-Karnataka)  
**Email:** sheldonkjee216@gmail.com

---

## 📌 Overview

This comprehensive framework analyzes and predicts weather patterns in Karnataka using machine learning and time series forecasting. It performs end-to-end exploratory data analysis (EDA), feature engineering, clustering, and forecasting on historical weather data.

**What it does:**
- Analyzes 30+ years of weather data (1990-2023)
- Predicts average temperature with 97% accuracy
- Identifies weather clusters and seasonal patterns
- Forecasts future temperature trends using SARIMA
- Discovers extreme weather indicators

---

## 📊 Key Findings

### 📦 Dataset Summary
- **Time Period:** 1990-2023 (30+ years)
- **Total Records:** ~35,000 daily observations
- **Geographic Coverage:** Karnataka State, India
- **Features:** Temperature, Precipitation, Seasonal patterns
- **Data Points:** Tavg, Tmin, Tmax, Precipitation

### 🌡️ Temperature Insights
- **Average Temperature Range:** 20.8°C - 28.4°C
- **Seasonal Variation:**
  - Winter (Dec-Feb): ~20.8°C
  - Summer (Apr-Jun): ~28.4°C
  - Monsoon (Jul-Sep): Cooler with high precipitation
  - Post-Monsoon (Oct-Nov): Moderate temperatures

- **Temperature Deviation (Seasonal):**
  - Max deviation: ±5°C from seasonal mean
  - Most values: ±0.8°C range

### 🎯 Model Performance Comparison

#### Random Forest Regressor (Best)
| Metric | Value |
|--------|-------|
| 🥇 **R² Score** | **0.97** (97% accuracy) |
| **MAE** | 0.23°C |
| **RMSE** | 0.38°C |
| **CV Mean** | 0.982 |
| **CV Std** | 0.001 |

#### Gradient Boosting Regressor
| Metric | Value |
|--------|-------|
| **R² Score** | 0.92 |
| **MAE** | 0.50°C |
| **RMSE** | 0.67°C |
| **CV Mean** | 0.919 |
| **CV Std** | 0.007 |

**Key Inference:** Random Forest provides exceptional accuracy with minimal error - **±0.23°C MAE** for temperature prediction.

### 📈 Feature Importance (Top Features)
- Temperature lags (previous day patterns)
- 7-day rolling averages
- Seasonal indicators (month_sin, month_cos)
- Extreme weather flags
- Precipitation interactions
- Temperature range metrics

### 🔄 Time Series Forecasting
- **Model:** SARIMA(1,1,1)×(1,1,1,12)
- **Purpose:** Long-term temperature trend forecasting
- **Seasonal Component:** 12-month cycles captured
- **Diagnostic Plots:** Residuals, ACF/PACF analyzed

---

## 📈 Visualizations Generated

The analysis produces comprehensive visualizations revealing weather patterns:

### 1. **Time Series Plots**
- Yearly temperature trends (1990-2023)
- Monthly average heatmaps
- Seasonal decomposition plots
- Daily, weekly, and monthly patterns

### 2. **Statistical Distributions**
- Temperature histograms and boxplots
- Precipitation distributions
- Outlier detection plots
- Seasonal comparison charts

### 3. **Feature Analysis**
- Correlation heatmaps between temperature and features
- Feature importance bar charts
- Lag effect visualizations
- Rolling average trends

### 4. **Clustering Visualizations**
- K-Means clusters in 2D space
- 3D cluster scatter plots
- Cluster centers and boundaries
- Weather pattern groupings

### 5. **Model Performance Plots**
- Actual vs Predicted temperature
- Residual analysis plots
- Cross-validation score distributions
- Model comparison charts

### 6. **Extreme Weather Indicators**
- Heat wave event timeline
- Cold snap occurrences
- Heavy rainfall events
- Seasonal extreme weather distribution

### 7. **Seasonal Pattern Analysis**
- Month-wise temperature patterns
- Seasonal precipitation boxplots
- Temperature range by season
- Year-over-year comparisons

---

## 🚀 Quick Demo

### Installation & Setup
```bash
# Navigate to project directory
cd EDA-Framework-For-Understanding-Weather-Variability-In-Karnataka

# Install dependencies
pip install pandas numpy matplotlib seaborn plotly scikit-learn statsmodels pymongo

# Ensure MongoDB is running (for data storage)
# mongod --dbpath C:\data\db  (Windows)
# or run MongoDB Atlas if using cloud

# Launch Jupyter notebook
jupyter notebook Code.ipynb
```

### Expected Output
The notebook will generate:
✅ Data ingestion into MongoDB  
✅ Statistical summary of 30+ years of data  
✅ 7+ high-quality EDA visualizations  
✅ Feature engineering with 25+ features  
✅ Clustering analysis with visual plots  
✅ Two ML models with 97% and 92% accuracy  
✅ SARIMA time series forecasts  
✅ Cross-validation stability metrics  
✅ Model evaluation and comparison  

### Step-by-Step Workflow
1. **Data Ingestion** → Load CSV, store in MongoDB
2. **Data Preprocessing** → Handle missing values, interpolation
3. **Feature Engineering** → 25+ features including lags, rolling averages, cyclical
4. **EDA** → Statistical analysis, outlier detection, time series plots
5. **Clustering** → K-Means on weather patterns (2D/3D visualization)
6. **Model Training** → Random Forest & Gradient Boosting
7. **Cross-Validation** → 5-fold CV for stability (0.982 R²)
8. **Time Series Forecasting** → SARIMA model
9. **Evaluation** → Compare metrics, residual analysis
10. **Visualization** → Generate 7+ comprehensive plots

---

## 🛠️ Technology Stack

### 📚 Core Data Processing
- **Pandas** - Data manipulation and time series handling
- **NumPy** - Numerical computing
- **Scikit-learn** - Machine learning models and preprocessing

### 📊 Visualization Libraries
- **Matplotlib** - Base plotting and time series plots
- **Seaborn** - Statistical visualizations and heatmaps
- **Plotly** - Interactive visualizations

### 🤖 Machine Learning Components
- **Random Forest Regressor** - Temperature prediction (97% accuracy)
- **Gradient Boosting Regressor** - Alternative model (92% accuracy)
- **StandardScaler** - Feature normalization
- **LabelEncoder** - Categorical encoding
- **train_test_split** - Data splitting for validation

### 📡 Time Series & Forecasting
- **Statsmodels** - SARIMA time series model
- **Seasonal decomposition** - Pattern extraction
- **Cross-validation** - Model stability assessment

### 🗄️ Database & Storage
- **MongoDB** - NoSQL database for weather data storage
- **Pymongo** - Python MongoDB driver
- **Tabulate** - Data table formatting

### 🐍 Language & Environment
- **Python 3.x** - Programming language
- **Jupyter Notebook** - Interactive analysis environment
- **Pip** - Package management

---

## 📁 Project Structure

```
EDA-Framework-For-Understanding-Weather-Variability-In-Karnataka/
├── Code.ipynb              # Main analysis notebook (All code + visualizations)
├── README.md               # This file
├── LICENSE                 # Project license
└── Dataset/
    └── weather.csv         # ~35,000 daily records (1990-2023)
```

### Dataset Features

| Category | Features |
|----------|----------|
| **Temperature** | Tavg (Average), Tmin (Minimum), Tmax (Maximum) |
| **Precipitation** | Prcp (Daily rainfall in mm) |
| **Temporal** | Year, Month, Season, Day of Year |
| **Engineered** | Temperature Range, Temp Category, Precipitation Category |
| **Lag Features** | Tavg_lag1, Prcp_lag1 (Previous day values) |
| **Rolling Averages** | 7-day, 30-day averages for temp & precip |
| **Cyclical** | month_sin, month_cos, day_sin, day_cos |
| **Extremes** | Extreme Heat, Extreme Cold, Heavy Rain indicators |
| **Interactions** | Temp-Precipitation interaction, Tavg squared |

---

## 📊 Results Summary

### Analysis Results
✅ **30+ years of weather data analyzed** with complete EDA  
✅ **Seasonal patterns identified** with visual confirmation  
✅ **7+ visualizations generated** from inferred patterns  
✅ **25+ engineered features** for ML models  
✅ **Extreme weather events identified** and tracked  
✅ **Clustering revealed 3-5 distinct weather patterns**  

### Model Results
✅ **Random Forest achieves 97% accuracy** (R² = 0.97)  
✅ **Temperature prediction error: ±0.23°C**  
✅ **Cross-validation consistent** (0.982 mean, 0.001 std)  
✅ **Gradient Boosting alternative** with 92% accuracy  
✅ **SARIMA forecasting** captures seasonal trends  
✅ **Stable predictions** across 5-fold validation  

### Key Inferences
1. **Predictability is High:** 97% R² shows temperature is highly predictable
2. **Seasonal Patterns are Strong:** SARIMA (1,1,1)×(1,1,1,12) seasonal component essential
3. **Lag Features are Valuable:** Previous day patterns significantly influence prediction
4. **Feature Engineering Matters:** 25+ engineered features drive model accuracy
5. **Random Forest Superior:** Outperforms Gradient Boosting on this dataset
6. **Extreme Weather is Rare:** <2% of days have extreme conditions

---

## 📈 Model Comparison

| Metric | Random Forest | Gradient Boosting |
|--------|---------------|-------------------|
| **R² Score** | 0.97 ⭐ | 0.92 |
| **MAE** | 0.23°C ⭐ | 0.50°C |
| **RMSE** | 0.38°C ⭐ | 0.67°C |
| **CV Mean** | 0.982 ⭐ | 0.919 |
| **CV Std** | 0.001 ⭐ | 0.007 |
| **Interpretation** | Best overall | Good alternative |

---

## 📞 Contact

📧 **Email:** sheldonkjee216@gmail.com  
🔗 **GitHub:** https://github.com/SheldonKjee  
📱 **Repository:** https://github.com/SheldonKjee/EDA-Framework-For-Understanding-Weather-Variability-In-Karnataka
