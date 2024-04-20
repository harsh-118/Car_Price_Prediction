# Libraries Used:
* **Pandas (import pandas as pd):** Used for data manipulation and analysis, especially with DataFrame structures.
*  **NumPy (import numpy as np):** Essential for numerical operations and array manipulations.
* **Matplotlib (from matplotlib import pyplot as plt):** Used for creating visualizations like plots and charts.
* **Scikit-learn (from sklearn...):** Comprehensive library for machine learning tasks including preprocessing, modeling, and evaluation.
    * **LabelEncoder:** Used for encoding categorical variables into numeric format.
    * **ColumnTransformer:** Helps with column-specific transformations (e.g., one-hot encoding).
    * **MinMaxScaler, StandardScaler:** Used for scaling numerical data to a specified range or standardizing them.
    * **SelectKBest, f_classif:** Feature selection based on statistical tests.
    * **NearestNeighbors, DBSCAN:** Utilized for outlier detection and clustering tasks.
    * **RandomForestRegressor:** A machine learning model for regression tasks.
* **Seaborn (import seaborn):** Enhances the visual aesthetics of Matplotlib plots and provides additional plot types.



# Workflow Explanation:
### 1. Data Loading and Cleaning:
Loads a dataset (Car.csv) using pandas.
Handles missing values by dropping rows with NaNs and resets the index.
### 2. Feature Engineering:
Cleans and standardizes specific columns like max_power, engine, and mileage by extracting numerical values and handling anomalies.
Transforms categorical columns (owner, transmission, seller_type, fuel, seats, name) into numerical representations for analysis.
### 3. Exploratory Data Analysis (EDA):
Analyzes distribution and relationship of categorical features (seats, transmission, seller_type, fuel, name) with selling_price using visualization techniques like violin plots.
Explores statistical summaries and correlations among numeric features (year, km_driven, mileage, engine, max_power) using heatmap visualization.
### 4. Feature Selection:
Uses ANOVA (f_classif) to select the most relevant features (SelectKBest) for modeling based on their relationship with selling_price.
### 5. Outlier Detection:
Identifies and removes outliers in numeric columns (km_driven, max_power, mileage) using Z-score method to improve model performance.
### 6. Model Building and Evaluation:
Constructs a Random Forest Regressor model (RandomForestRegressor) to predict selling_price based on selected features.
Evaluates model performance using metrics such as mean absolute error (mean_absolute_error) and coefficient of determination (r2_score).
### 7. User Input Prediction:
Implements a mechanism to take user input for car attributes (name, year, km_driven, fuel, seller_type, transmission, owner, mileage, engine, max_power, seats) and predicts the car price using the trained model.

