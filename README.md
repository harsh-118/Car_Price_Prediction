# Workflow Explanation:
### 1) Data Loading and Cleaning:
Loads a dataset (Car.csv) using pandas.
Handles missing values by dropping rows with NaNs and resets the index.
### 2) Feature Engineering:
Cleans and standardizes specific columns like max_power, engine, and mileage by extracting numerical values and handling anomalies.
Transforms categorical columns (owner, transmission, seller_type, fuel, seats, name) into numerical representations for analysis.
### 3) Exploratory Data Analysis (EDA):
Analyzes distribution and relationship of categorical features (seats, transmission, seller_type, fuel, name) with selling_price using visualization techniques like violin plots.
Explores statistical summaries and correlations among numeric features (year, km_driven, mileage, engine, max_power) using heatmap visualization.
### 4) Feature Selection:
Uses ANOVA (f_classif) to select the most relevant features (SelectKBest) for modeling based on their relationship with selling_price.
### 5) Outlier Detection:
Identifies and removes outliers in numeric columns (km_driven, max_power, mileage) using Z-score method to improve model performance.
### 6) Model Building and Evaluation:
Constructs a Random Forest Regressor model (RandomForestRegressor) to predict selling_price based on selected features.
Evaluates model performance using metrics such as mean absolute error (mean_absolute_error) and coefficient of determination (r2_score).
### 7) User Input Prediction:
Implements a mechanism to take user input for car attributes (name, year, km_driven, fuel, seller_type, transmission, owner, mileage, engine, max_power, seats) and predicts the car price using the trained model.

