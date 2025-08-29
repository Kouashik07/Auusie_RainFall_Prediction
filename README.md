🌦️ Weather Prediction (RainTomorrow) (ML Project)
📌 Overview

This project predicts whether it will rain tomorrow (Yes or No) using the Australian weather dataset (weatherAUS.csv).
The goal is to analyze weather patterns and build a classification model that can estimate rainfall probability for the next day based on historical weather features.

🔧 Tech Stack

Python

Pandas, NumPy

Seaborn, Plotly, Matplotlib (for visualization)

Scikit-Learn (Random Forest, preprocessing, imputation, scaling, encoding)

🚀 Project Workflow
1. Data Exploration (EDA)

Checked missing values and distributions of weather features (temperature, humidity, wind, etc.)

Plotted relationships between features and rainfall (RainTomorrow)

Used correlation heatmaps and visualizations for feature insights

2. Data Preprocessing

Missing values handled using SimpleImputer (mean for numeric features)

Scaling applied using MinMaxScaler for numeric features

Categorical encoding done using OneHotEncoder

Split dataset into Train, Validation, Test sets (by year for realism)

3. Modeling

Implemented RandomForestClassifier with hyperparameters:

n_estimators=500 (number of trees)

max_features=7 (random subset of features per split)

max_depth=30 (limit tree depth to prevent overfitting)

class_weight={'No': 1, 'Yes': 1.5} (to handle class imbalance)

4. Prediction Function

Built a custom function predict_input() that:

Takes new weather data as input

Applies preprocessing (imputation, scaling, encoding)

Predicts rain tomorrow (Yes/No) along with probability

📈 Results

Model successfully predicts whether it will rain tomorrow.

Handles class imbalance (since "No Rain" is more common) with weighted classes.

Provides both prediction and probability confidence for each input.

📝 Conclusion

This project demonstrates the use of Ensemble Learning (Random Forest) for real-world weather forecasting tasks.
It can be extended with:

Hyperparameter tuning (GridSearch, RandomSearch)

Feature engineering (seasonal/weather patterns)

Advanced models (XGBoost, LightGBM, Neural Networks)
