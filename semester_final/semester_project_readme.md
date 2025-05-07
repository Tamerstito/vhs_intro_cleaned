AI Semester Project – Video Game Sales Prediction

Project Overview
For my semester‑long AI course project I built a supervised machine‑learning pipeline to predict global unit sales of video games using the public “Video Game Sales with Ratings” dataset. The notebook documents how I:
Cleaned and pre‑processed the raw CSV (removed post‑launch features to avoid leakage, handled missing publishers, and parsed release years).
Explored categorical distributions (platform, genre, publisher) through bar charts and box plots.
Created two alternative feature sets: one using Ordinal Encoding and another using One‑Hot Encoding for genre and platform.
Trained and compared Random Forest and XGBoost regressors on each feature set.
Evaluated models with MAE/R² on a held‑out test split and analysed feature importances.

Technologies Used
Data manipulation: pandas, numpy
Visualisation: matplotlib
Modeling: scikit‑learn (RandomForestRegressor), xgboost (XGBRegressor)

How I Ran the Notebook
Opened ai-semester-project.ipynb in Google Colab
Uploaded vgsales.csv to the Colab working directory.

Challenges Faced & Resolutions
Data leakage – The original CSV included regional sales figures (NA_Sales, EU_Sales, etc.) that directly summed to Global_Sales. I dropped these columns to ensure the model learned from pre‑launch attributes only.
High‑cardinality categories – Publisher contained 500+ unique values. I experimented with grouping infrequent publishers under “Other” and compared One‑Hot vs Ordinal encoding; One‑Hot with grouped categories yielded the best generalisation.
Class imbalance – A few blockbuster titles dominated sales. I log‑transformed the target variable to stabilise variance and improve MAE.

Future Improvements
Perform hyper‑parameter tuning with Optuna or GridSearchCV for XGBoost parameters (learning rate, subsample, etc.).
Incorporate text features (game descriptions) using TF‑IDF + gradient boosting.
Update the dataset with 2024‑2025 releases and re‑train to keep predictions current.