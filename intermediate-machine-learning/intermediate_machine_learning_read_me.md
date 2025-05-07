Intro to Machine Learning — Exercise Series

Project Overview
This folder contains the six hands‑on notebooks I completed while following Kaggle’s Intro to Machine Learning micro‑course. Each notebook focused on a key concept:
exercise‑introduction.ipynb – Built my first decision‑tree model and calculated Mean Absolute Error (MAE).
exercise‑missing‑values.ipynb – Compared strategies for handling missing data (drop columns vs impute).
exercise‑cross‑validation.ipynb – Implemented k‑fold CV to obtain more robust validation scores.
exercise‑data‑leakage.ipynb – Identified target leakage in the Melbourne housing dataset and fixed it.
exercise‑pipelines.ipynb – Combined preprocessing and modeling steps into a single Pipeline object.
exercise‑xgboost.ipynb – Trained an XGBoost regressor and achieved my best leaderboard MAE.

Technologies Used
Data manipulation: pandas, numpy
Modeling & validation: scikit‑learn (DecisionTreeRegressor, RandomForestRegressor, Pipeline, cross_val_score)
Gradient boosting: xgboost (XGBRegressor)
Visualisation: matplotlib
Interactive guidance: kaggle‑learntools

How I Ran the Exercises
On Kaggle (original workflow)
Opened each .ipynb inside Kaggle’s course workspace.
Stepped through every TODO cell, filled in code, and submitted for auto‑grading.

Challenges Faced & What I Learned
Target leakage surprises – Learned to inspect for columns that wouldn’t be available at prediction time and to drop them.
Imputation pitfalls – Simple mean imputation occasionally degraded performance; switching to SimpleImputer(strategy="median") and keeping categorical variables separate improved results.
Pipeline debugging – Early errors arose from mis‑matched feature names after one‑hot encoding; ColumnTransformer solved this elegantly.

Future Improvements
Re‑evaluate all notebooks with a larger, modern dataset (e.g., Ames Housing) to consolidate lessons.
Replace manual cross‑validation loops with sklearn.model_selection.GridSearchCV for hyper‑parameter tuning.