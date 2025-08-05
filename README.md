NutriClass: Automated Machine Learning Pipeline
Project Overview
This project implements an automated machine learning (AutoML) pipeline using Python and Scikit-learn to classify meal types. The pipeline is designed to be highly reproducible and easy to use, especially within a Google Colab environment.

The core functionality includes:

Data Loading and Preprocessing: Automatically loads a CSV dataset, cleans column names, handles missing values, and identifies feature types.

Feature Engineering: Uses a robust ColumnTransformer to apply appropriate preprocessing steps (e.g., scaling numerical features, one-hot encoding categorical features).

Model Comparison: Compares multiple machine learning models (Logistic Regression, Random Forest, AdaBoost, and XGBoost) using cross-validation to find the best-performing one.

Model Training and Saving: Trains the best-performing model on the full training data and saves the final, trained pipeline to a .joblib file for future use.

Features
Seamless Integration: Designed for Google Colab, but can be adapted for any Python environment.

Automated Workflow: From raw data to a saved model in a single script.

Reproducibility: Uses a fixed random_state for consistent results.

Robust Preprocessing: Automatically handles data cleaning, imputation, scaling, and encoding.

Dataset
This project requires a dataset named Dataset.csv. It is expected to have a column named Meal_Type, which is the target variable for classification. The script will automatically clean and normalize the column name and its values.

Expected Dataset Path
The script is configured to look for the file directly in the current directory, which is the standard setup for a Google Colab notebook after a direct upload.

/
├── Dataset.csv
└── your_notebook.ipynb

Models Included
The pipeline compares the following classification algorithms to determine the best fit for your data:

LogisticRegression

RandomForestClassifier

AdaBoostClassifier

XGBClassifier

The best model is selected based on its weighted F1 score from 5-fold cross-validation.

Getting Started
Follow these simple steps to run the project in Google Colab:

Open Google Colab: Go to colab.research.google.com.

Upload the Dataset: In the file browser on the left, click the "Upload to session storage" icon and upload your Dataset.csv file.

Copy the Code: Create a new code cell and paste the entire provided Python script.

Install Libraries (if needed): The code includes a commented line to install the necessary libraries. If they are not already installed, uncomment and run the following line in a separate cell:

!pip install pandas scikit-learn xgboost

Run the Script: Execute the code cell. The script will print its progress, including data loading, model comparison results, and the final classification report.

Expected Output
After the script runs, a file named nutriclass_best_model_sklearn.joblib will be saved to your Colab environment. This file contains the complete, trained machine learning pipeline that can be used to make predictions on new data.

License
This project is open-source. Please feel free to use and modify it as you see fit.
