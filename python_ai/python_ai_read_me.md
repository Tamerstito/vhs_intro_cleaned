Python for AI — Intro Series

Project Overview
This learning module comprises three Jupyter notebooks that gradually build my foundational skills for data science and AI in Python:
python_ai_part1.ipynb – Core Python syntax and structures (lists, dictionaries, functions, classes) with interactive examples and quick‑sort implementation.
python_ai_part2.ipynb – Hands‑on with essential scientific libraries: NumPy arrays, pandas DataFrames, and basic matplotlib plotting.
Titanic_data_exploration.ipynb – Capstone exercise: exploratory data analysis (EDA) on the classic Titanic survival dataset, including data cleaning, summary statistics, and visual insights.

Technologies Used
Numerical arrays: NumPy
Data manipulation: pandas
Plotting: matplotlib, seaborn

How I Ran the Notebooks
Opened each .ipynb file in Google Colab via the “Open in Colab” badge.
For the Titanic notebook, I uploaded train.csv to a Google Drive folder vhs-ai-intro.

Challenges Faced & How I Solved Them
Handling missing values – The Titanic dataset includes Age, Cabin, and Embarked NaNs. I experimented with .isna().sum(), visualised gaps with seaborn’s heatmap, and imputed or dropped rows as appropriate.
Broadcasting errors in NumPy – Early array operations raised shape‑mismatch exceptions; reviewing NumPy broadcasting rules and adding reshape calls resolved them.

Future Improvements
Extend the Titanic notebook to build a classification model (e.g., RandomForestClassifier) and evaluate accuracy.
Introduce interactive widgets (ipywidgets) for dynamic EDA exploration.
Add a Dockerfile and requirements.txt for reproducible local execution.