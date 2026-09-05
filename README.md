# fbi-crime-incident-forecasting

## Business Context
This project uses historical crime data from Vancouver (1999-2011) to predict the number of crime incidents per month, per crime type, for 2012-2013. The goal is to help law-enforcement agencies allocate patrol resources, staffing, and preventive measures proactively rather than reactively.

## Problem Statement
Predict monthly `Incident_Counts` for each crime `TYPE` using historical incident-level data aggregated to the month level.

## Dataset
- **Train.xlsx**: ~474,565 incident-level crime records (1999-2011) with TYPE, location, and timestamp fields.
- **Test.csv**: 162 rows requiring predicted `Incident_Counts` for YEAR/MONTH/TYPE combinations (2012-2013).

## Approach
1. Data cleaning and handling missing values (NEIGHBOURHOOD, HOUR/MINUTE)
2. Aggregating incident-level data to monthly (YEAR, MONTH, TYPE) level
3. Exploratory Data Analysis (15 charts covering temporal, spatial, and type-based patterns)
4. Hypothesis testing (t-test, chi-square, Pearson correlation)
5. Feature engineering (lag features, rolling averages, type encoding)
6. Model building: Linear Regression, Random Forest, XGBoost with hyperparameter tuning
7. Model evaluation (MAE, RMSE, R²) and feature importance analysis

## Notebooks
- [FBI Crime Investigation - EDA.ipynb](./FBI%20Crime%20Investigation%20-EDA.ipynb) - Exploratory Data Analysis
- [FBI Crime Investigation ML.ipynb](./FBI%20Crime%20Investigation%20ML.ipynb) - Feature Engineering, Modelling & Evaluation

## Key Findings
- Theft from Vehicle and Mischief are the most common crime types.
- Crime shows seasonal patterns (higher in summer, lower in winter).
- Central Business District, West End, and Mount Pleasant are the top crime hotspots.
- The tuned XGBoost model achieved the best performance, with lag-based features (previous month/year counts) being the strongest predictors.

## Tech Stack
Python, Pandas, NumPy, Scikit-learn, XGBoost, Matplotlib, Seaborn

## Colab Notebooks (View Access)
- EDA Notebook: [https://colab.research.google.com/drive/1nylBmM6x8BAAIXum7CSBPPicUi2WRM5c?usp=sharing]
- ML Notebook: [https://colab.research.google.com/drive/15liXpXBrkZeZprm-4U2IC1rwJAOvp1qB?usp=sharing]
  
