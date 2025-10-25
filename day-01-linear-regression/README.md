# Day 1: Linear Regression with California Housing Dataset

## Algorithm Overview

This notebook implements **Linear Regression** analysis using the California Housing dataset. Linear Regression is a statistical method that models the relationship between a dependent variable and one or more independent variables by fitting a linear equation to observed data. The algorithm finds the best-fit line by minimizing the sum of squared residuals between predicted and actual values.

## Data Usage

**Dataset:** California Housing Dataset from `sklearn.datasets`

**Features Used (8 total):**
- `MedInc` - Median Income in block group
- `HouseAge` - Median House Age in block group
- `AveRooms` - Average number of rooms per household
- `AveBedrms` - Average number of bedrooms per household
- `Population` - Block group population
- `AveOccup` - Average number of household members
- `Latitude` - Block group latitude
- `Longitude` - Block group longitude

**Target Variable:** `MedHouseVal` - Median House Value (in $100,000s)

**Data Split:** 80% training, 20% testing

## Observations

### Key Findings:

1. **Model Performance:**
   - The linear regression model provides a baseline for predicting house prices
   - R² score indicates how well the linear model explains variance in house values
   - Mean Absolute Error (MAE) and Root Mean Squared Error (RMSE) provide interpretable metrics in the original price scale

2. **Feature Importance:**
   - Median Income (`MedInc`) typically shows the strongest positive correlation with house values
   - Geographic features (Latitude, Longitude) capture location-based pricing patterns
   - Average Rooms may indicate house size and quality

3. **Model Limitations:**
   - Linear Regression assumes linear relationships between features and target
   - May underperform in areas where relationships are non-linear
   - Sensitive to outliers and multicollinearity between features

4. **Insights:**
   - The model demonstrates that socioeconomic factors (income) and location are primary drivers of housing prices
   - Simple linear models can provide interpretable baseline results for regression tasks
   - Performance metrics suggest room for improvement with more sophisticated algorithms (future days)

### Next Steps:
- Compare with polynomial regression or regularized models (Ridge/Lasso) on same dataset
- Explore feature engineering and interaction terms
- Try non-linear algorithms for better predictive performance