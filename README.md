# 🌦️ Weather Prediction using Machine Learning  
**Location:** Oakland, California (NOAA Dataset)  
**Platform:** Python (Jupyter Notebook)  

---

## 📌 Project Description

This project aims to predict **next-day maximum temperature (TMAX)** and **precipitation** using historical weather data sourced from the **[NOAA Climate Data Online](https://www.ncei.noaa.gov/cdo-web/)** portal. The dataset was specifically collected from **Oakland International Airport, CA, US**, and analyzed using machine learning techniques in **Python (Jupyter Notebook)**.

---

## 📊 Dataset Overview

- **Source:** NOAA (CSV format)
- **Location:** Oakland, CA
- **Fields Used:** `DATE`, `TMAX`, `TMIN`, `PRCP`
- **Records:** ~8,000+ daily entries
- **Time Span:** Multiple years depending on data availability

---

## 🧹 Data Preprocessing

- Converted `DATE` into:
  - `month`, `day`, `year`, `day_of_year`, `week_of_year`
- Created lag features for temporal modeling:
  - `TMAX_lag_1`, `TMIN_lag_3`, `PRCP_lag_2`, etc.
- Generated target columns for next-day predictions:
  - `next_TMAX`, `next_TMIN`, `next_PRCP`
- Missing values handled using:
  - `SimpleImputer(strategy='mean')`
- Feature scaling using:
  - `StandardScaler`
- Applied:
  - `PolynomialFeatures(degree=2)` for non-linear pattern detection

---

## 🤖 Machine Learning Models

### 🔥 Temperature Prediction (Regression):
- **Ridge Regression**
- **Random Forest Regressor**
- Metrics Used: `R² Score`, `MAE`

### 🌧️ Precipitation Prediction (Classification):
- **Ridge Classifier**
- **Random Forest Classifier**
- Metrics Used: `Accuracy`, `Confusion Matrix`, `Visual Heatmaps`

---

## 📈 Visualizations

- Line plots for:
  - Actual vs Predicted TMAX and TMIN
- Bar graph:
  - Top 20 important features (via Random Forest)
- Calendar heatmaps:
  - Day-wise accuracy of precipitation prediction
- Classification performance:
  - Correct vs incorrect prediction by date

---

## ✅ Model Accuracy Summary

| Task                     | Model               | Score         |
|--------------------------|---------------------|---------------|
| TMAX Prediction          | Ridge Regression    | **89.8%**     |
| TMAX Prediction          | Random Forest       | **89.5%**     |
| Precipitation Prediction | Ridge Classifier    | **95.4%**     |
| Precipitation Prediction | Random Forest       | **95.8%**     |

---

## ⚙️ Tools & Technologies

- **Python 3.10+**
- **Jupyter Notebook**
- **Libraries:**
  - `pandas`, `numpy`, `matplotlib`, `seaborn`
  - `scikit-learn`, `xgboost`

---

## 🏁 Conclusion

This project demonstrates how weather data from publicly available sources like NOAA can be effectively used to build accurate **next-day weather prediction models**. Using techniques like **feature engineering**, **polynomial transformations**, and **ensemble models**, the project achieves high accuracy levels—especially for precipitation forecasting (95%+). All steps were implemented in **Jupyter**
