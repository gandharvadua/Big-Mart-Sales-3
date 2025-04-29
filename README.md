Big Mart Sales III 
Problem Statement: The data scientists at BigMart have collected 2013 sales data for 1559 products across 10 stores in different cities. Also, certain attributes of each product and store have been defined. The aim is to build a predictive model and predict the sales of each product at a particular outlet
Objective: The goal was to predict Item_Outlet_Sales accurately using the available product and store data. The focus was on building a reliable, interpretable model without using any external datasets, ensuring everything remained within the scope of the provided information.
Step 1: Data Preparation
Missing values in Item_Weight were filled by calculating the mean weight for each Item_Identifier. Outlet_Size missing values were filled with 'Small' based on frequency.
Label encoding was done for ordinal categories, and one-hot encoding was applied for nominal features.
Dropped Item_Identifier and Outlet_Identifier from training features to avoid leakage.
Step 2: Exploratory Data Analysis
Conducted univariate and bivariate analysis.
Identified Item_MRP as a primary driver for sales.
Built hypotheses around outlet size, location tier, and visibility inconsistency.
Step 3: Model Building and Experimentation
Started with a baseline Linear Regression model to establish a minimum benchmark.
Implemented Decision Tree, Random Forest, Gradient Boosting, XGBoost, and LightGBM models.
Separate experiments were conducted where boosting models were trained only on selected important features.
Step 4: Hyperparameter Tuning
Extensive RandomizedSearchCV was used across LightGBM, XGBoost, and Random Forest.
Focused tuning on max_depth, n_estimators, learning_rate, subsample ratios, and regularization parameters.
Step 5: Ensemble Creation
Built a simple average ensemble combining LightGBM and XGBoost.
Clipped negative sales predictions to zero to align with business logic.
Ensemble RMSE improved to 1018.42, outperforming all single models.
