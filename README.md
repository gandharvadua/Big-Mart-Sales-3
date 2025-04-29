Big Mart Sales III - Sales Prediction Project

Welcome to the Big Mart Sales III repository! This project focuses on predicting outlet sales based on a structured dataset of item and outlet features. It was designed to practice real-world data science workflows: data cleaning, feature engineering, modeling, tuning, interpretation, and deployment readiness.

Project Overview

The objective was to build a robust and interpretable model that predicts the Item_Outlet_Sales variable as accurately as possible. Emphasis was placed on both performance and maintainability, ensuring reproducibility without relying on external data.

Folder Structure

/notebooks/

Jupyter Notebooks for EDA, Modeling, Tuning, and Ensembling.

/data/

Train, test, and submission datasets (placeholders).

/outputs/

Model predictions and submission files.

/scripts/

Python scripts for data preprocessing, model training, and evaluation.

README.md

This document.

requirements.txt

List of Python dependencies.

Steps Followed

Data Cleaning:

Imputed missing values smartly (e.g., average weight per Item).

Standardized inconsistent category names.

Feature Engineering:

Created meaningful features like Outlet Age, Item Category, and Visibility Mean Ratio.

EDA:

Investigated feature relationships, distribution patterns, and hypotheses.

Modeling:

Built multiple models: Linear Regression, Decision Trees, Random Forest, XGBoost, LightGBM, SVR, AdaBoost.

Hyperparameter Tuning:

Applied RandomizedSearchCV for advanced boosting models.

Ensembling:

Averaged LightGBM and XGBoost outputs for final prediction.

Interpretation:

Used SHAP and feature importance plots to explain model behavior.

Submission Generation:

Created clean, ready-to-upload CSV files for evaluation.

Key Results

Best RMSE achieved: 1018.42 (Ensemble Model)

Major sales drivers: Item MRP, Outlet Type, Visibility, Outlet Age

Model interpretability and business logic were prioritized throughout.

How to Run

Clone the repository.

Install dependencies from requirements.txt.

Place the data files inside /data/.

Start with the EDA notebook, then move to the modeling notebook.

Run the final ensemble script for best prediction results.

Technologies Used

Python 3.11

Pandas, NumPy

Scikit-learn

LightGBM, XGBoost

Seaborn, Matplotlib

SHAP

Acknowledgements

Special thanks to Analytics Vidhya for providing the Big Mart Sales III dataset.

If you found this helpful or have suggestions for improvement, feel free to open an issue or contribute!
