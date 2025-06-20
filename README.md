##🌦️ Weather Prediction using Machine Learning
Location: Oakland, California (NOAA Dataset)
Platform: Python (Jupyter Notebook)

📌 Project Description
This project aims to predict next-day maximum temperature (TMAX) and precipitation using historical weather data sourced from the NOAA Climate Data Online portal. The data was collected specifically from Oakland International Airport, CA, US, and analyzed using machine learning models in Python (Jupyter Notebook).

📊 Dataset Overview
Source: NOAA (CSV format)

Location: Oakland, CA

Columns Used:

DATE, TMAX, TMIN, PRCP

Records: ~8,000+ daily entries

Time Span: Multiple years (depends on file)

🧹 Data Preprocessing Highlights
Converted DATE into:

month, day, year, day_of_year, week_of_year

Created lag features:

TMAX_lag_1, TMAX_lag_2, PRCP_lag_3, etc.

Generated target columns for next-day prediction:

next_TMAX, next_TMIN, next_PRCP

Handled missing data using:

SimpleImputer(strategy='mean')

Scaled features using:

StandardScaler

Applied Polynomial Feature Expansion (degree=2)

🤖 Machine Learning Models
🔥 Temperature (Regression):
Ridge Regression

Random Forest Regressor

Evaluated using:

R² Score, Mean Absolute Error (MAE)

🌧️ Precipitation (Binary Classification):
Ridge Classifier

Random Forest Classifier

Evaluated using:

Accuracy Score, Confusion Matrix, Day-wise Heatmaps

📈 Graphs & Visualizations
✅ Actual vs Predicted plots for TMAX and TMIN

🔢 Feature Importance (Top 20) bar graph

📅 Heatmaps of precipitation prediction accuracy by month and day

✅ Correct vs Incorrect prediction visualization

✅ Model Accuracy Summary
Prediction Task	Model	Accuracy / R²
Temperature (TMAX)	Ridge Regression	89.8%
Temperature (TMAX)	Random Forest	89.5%
Precipitation	Ridge Classifier	95.4%
Precipitation	Random Forest	95.8%

⚙️ Technologies Used
Python 3.10+

Jupyter Notebook

Libraries:
pandas, numpy, matplotlib, seaborn,
scikit-learn, xgboost

🏁 Conclusion
This end-to-end weather forecasting project showcases how public weather data (NOAA) can be used to build accurate next-day predictions for temperature and precipitation using modern regression and classification algorithms. The project was implemented in Python using Jupyter Notebook, and achieved over 95% classification accuracy using Random Forest.
