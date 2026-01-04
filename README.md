Used Car Price Predictor: Random Forest–Based Market Valuation Model
Abstract

This project focuses on developing a Used Car Price Predictor, a machine learning system designed to estimate the fair market value of used vehicles based on structured attributes such as make, model, year, mileage, condition, fuel type, and drivetrain specifications. The primary model developed and analyzed in this project is a Random Forest regression model, selected for its ability to capture non-linear relationships and feature interactions commonly present in real-world pricing data.

The purpose of this model is to assist consumers, dealerships, and online marketplaces in determining reasonable price ranges in a volatile and increasingly expensive used car market. Using a dataset of historical vehicle listings, the project applies data preprocessing, exploratory data analysis (EDA), and tree-based regression modeling to identify the most influential factors affecting used car prices.

Introduction

The goal of this project is to design and evaluate a machine learning model that accurately predicts the market value of a used vehicle given its observable attributes. Due to economic conditions, supply chain disruptions, and shifting consumer demand, used car prices have become increasingly difficult to evaluate using traditional heuristics.

In this project, I focus specifically on developing a Random Forest regression model to address these challenges. Random Forests are well-suited for this task due to their robustness to outliers, ability to model complex non-linear patterns, and reduced risk of overfitting compared to single decision trees. By leveraging historical used car listings, the model aims to provide a data-driven pricing tool that improves transparency and supports informed decision making.

The dataset used in this project is sourced from Kaggle:
https://www.kaggle.com/datasets/taeefnajib/used-car-price-prediction-dataset

Project Overview

This project implements a supervised regression framework with an emphasis on tree-based ensemble learning.

The core contribution of this work is the design, training, and evaluation of a Random Forest regression model for used car price prediction. Supporting analyses—including feature engineering and EDA—are used to improve model performance and interpretability.

The final output of the model is a continuous price estimate for a given vehicle configuration.

Dataset Details
1. Source Data

Dataset: Used Car Price Prediction Dataset (Kaggle)

Observations: 4,000+ used car listings

Target Variable: price (continuous)

2. Feature Categories

The dataset includes:

Vehicle make and model

Model year

Mileage

Fuel type

Engine type

Transmission

Exterior and interior color

Accident history

Title status

3. Analytical Focus

The data is used to:

Identify features with the strongest influence on vehicle price.

Examine feature interactions captured by the Random Forest model.

Reduce noise through informed preprocessing and feature selection.

Methodology: Random Forest Regression
1. Data Preprocessing

Handling missing and inconsistent values

Encoding categorical variables

Scaling numerical features where appropriate

Identifying and mitigating extreme outliers

2. Exploratory Data Analysis (EDA)

EDA is conducted to:

Analyze price distributions

Study correlations between features and price

Detect multicollinearity

Motivate the use of a non-linear, ensemble-based model

3. Random Forest Model Development

The Random Forest regressor is trained using an ensemble of decision trees, each constructed on bootstrapped samples of the data with randomized feature selection. This approach:

Captures non-linear relationships between features and price

Models complex interactions without explicit feature engineering

Reduces variance compared to single decision trees

Hyperparameters such as the number of trees, maximum tree depth, and minimum samples per leaf are tuned to balance bias and variance.

4. Model Evaluation

Model performance is evaluated using Mean Squared Error (MSE) and residual analysis on held-out test data. Feature importance scores derived from the Random Forest are analyzed to interpret which vehicle attributes most strongly influence predicted prices.
