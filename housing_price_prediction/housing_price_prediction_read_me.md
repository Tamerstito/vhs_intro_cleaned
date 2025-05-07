Housing Price Prediction

Project Overview
I completed an end‑to‑end supervised machine‑learning workflow to predict the sale price of houses in Ames, Iowa, using the Kaggle “House Prices: Advanced Regression Techniques” data set. Over a series of Jupyter notebooks I:
Explored and cleaned the tabular data
Selected useful features and handled missing values
Trained baseline models, diagnosed under‑ and over‑fitting, and iteratively improved performance
Validated results with a hold‑out validation set and submitted predictions to Kaggle for scoring

Technologies Used
Data manipulation & EDA: pandas, numpy
Visualization: matplotlib
Modeling: scikit‑learn (RandomForestRegressor, XGBRegressor, etc.)

How I Ran the Project (Reproducible Steps)
Kaggle (original environment)
I created a new Kaggle notebook inside the competition and attached the competition data.
I uploaded the project notebooks and executed all cells in sequence; Kaggle already provided the required libraries.

Challenges Faced & How I Overcame Them
Missing values & categorical variables — Many features contained NaNs or non‑numeric labels. I used SimpleImputer, one‑hot encoding, and domain knowledge to prepare the data.
Overfitting — Early models with large random forests over‑fit. I introduced cross‑validation and early stopping to balance bias and variance.
Feature selection — With 80+ raw columns, not all improved performance. I pruned low‑importance features, which simplified the model and improved generalization.

Future Improvements
Automate hyper‑parameter tuning with GridSearchCV or Optuna.
Engineer additional composite features (e.g., house age, total bathrooms, neighborhood quality indices).
Experiment with LightGBM or CatBoost for faster training.