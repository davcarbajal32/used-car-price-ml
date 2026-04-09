# Used Car Price Predictor

A Random Forest regression model that estimates the fair market value of used vehicles based on attributes like make, model, year, mileage, condition, fuel type, and drivetrain. Built to support pricing transparency in a volatile used car market.

## Results

- **$12.8K RMSE** on held-out test set (R² = 0.64)
- **Over 90% reduction** in prediction error from baseline (~$176K RMSE)
- Top predictive features: model year, mileage, make, and transmission type
- Trained on 4,009 vehicle listings from Kaggle

## Tech Stack

Python, Pandas, NumPy, scikit-learn, Matplotlib

## Dataset

[Used Car Price Prediction Dataset](https://www.kaggle.com/datasets/taeefnajib/used-car-price-prediction-dataset) from Kaggle. Includes 4,000+ listings with features covering make, model, year, mileage, fuel type, engine, transmission, color, accident history, and title status.

## Methodology

The core challenge is capturing the non-linear relationships between vehicle attributes and price. A Random Forest regressor was chosen for its robustness to outliers and ability to model complex feature interactions without heavy manual engineering.

Key steps included handling missing values, encoding categorical variables, mitigating extreme outliers, and applying log transformation to the target variable to reduce skew and improve model performance. Hyperparameters such as tree count, max depth, and minimum samples per leaf were tuned to balance bias and variance.

Feature importance scores from the trained model were used to interpret which attributes most strongly influence predicted prices.

For the full analysis, see [Presentation.pdf](Presentation.pdf).

## How to Run

1. Clone the repository
2. Install dependencies: `pip install pandas numpy scikit-learn matplotlib`
3. Run data cleaning: `python src/cleandata.py`
4. Run the model: `python src/randomforest.py`
