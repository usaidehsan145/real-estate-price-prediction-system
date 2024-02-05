# Real Estate Price Prediction System

## Overview

This project implements a Real Estate Price Prediction System using machine learning, specifically employing an XGBoost regressor. The system is designed to predict property prices based on various features such as property type, location, number of bedrooms, bathrooms, and total area.

## Dataset

The dataset (`Entities.csv`) serves as the foundation for this project, providing information about various properties, including type, location, size, and price.

## Data Pre-processing

- Load the dataset.
- Drop unnecessary columns.
- Filter out properties with invalid or zero values in essential features.
- Divide the dataset into separate data frames based on property types.
- Clean the data by removing outliers and ensuring properties meet specific criteria.

## Feature Engineering

- One-hot encode categorical variables (property type, city, purpose).
- Address outliers in numerical features to improve model performance.

## Model Training

The XGBoost regressor is chosen as the machine learning model for predicting property prices. The model is trained using the cleaned and pre-processed dataset, with hyperparameters tuned for optimal performance.

## Data Scaling

Numerical features are scaled using Min-Max scaling to ensure equal contribution to the model.

## Model Evaluation

The trained XGBoost model is evaluated using standard regression metrics: R-squared, Mean Squared Error (MSE), Mean Absolute Error (MAE), and Root Mean Squared Error (RMSE).

## Saving the Model

The model is saved using the Pickle library, allowing for easy retrieval and reuse without retraining.

## Prediction

To make predictions:
1. Load the saved model and Min-Max scaler.
2. Standardize user inputs representing property features.
3. Feed standardized inputs into the model for predicting the property price.

## Streamlit App

A Streamlit app (`streamlit.py`) is provided to interactively input property features and get real-time predictions. To run the app:

1. Install Streamlit using `pip install streamlit`.
2. Execute the app script using `streamlit run streamlit.py`.
3. Open the provided URL to access the Streamlit app.

## Running the Code

1. Ensure required libraries are installed: `pickle`, `pandas`, `numpy`, `xgboost`, and `streamlit`.
2. Execute the code in the provided notebook or script.
3. Adjust the input data structure in the prediction section to match the features used during training.

Feel free to explore and modify the code for your requirements or integrate it into your projects. For assistance or questions, reach out for support.
