# Day 3: L1 & L2 Regression Analysis

## Algorithm Overview

This notebook implements and compares three regression techniques on the California Housing dataset:

1. **Linear Regression** - Baseline ordinary least squares (OLS) regression without regularization
2. **Lasso Regression (L1)** - Linear regression with L1 regularization that adds penalty equal to absolute value of coefficients
3. **Ridge Regression (L2)** - Linear regression with L2 regularization that adds penalty equal to square of coefficients

Regularization techniques add a penalty term to the cost function to prevent overfitting by constraining coefficient magnitudes. L1 regularization promotes sparsity by driving some coefficients to zero, while L2 regularization shrinks all coefficients proportionally without eliminating them.

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

**Data Characteristics:**
- Total samples: 20,640
- No missing values
- Features have different scales requiring standardization
- MedInc shows highest correlation (0.688) with target variable

**Data Split:** 80% training, 20% testing

## Observations

### Key Findings:

1. **Model Performance:**
   - All three models show similar performance metrics on this dataset
   - Regularized models (Lasso and Ridge) help prevent overfitting compared to baseline Linear Regression
   - Mean Squared Error (MSE) and R² scores demonstrate effectiveness of regularization
   - Feature scaling is critical for optimal performance of regularized models

2. **Lasso Regression (L1) Characteristics:**
   - Performs automatic feature selection by setting some coefficients to exactly zero
   - Creates sparse models that are more interpretable
   - Useful for identifying most important predictive features
   - Works well when many features have little contribution to target prediction
   - **Formula:** Loss = MSE + α × Σ|β|

3. **Ridge Regression (L2) Characteristics:**
   - Maintains all features but reduces their coefficient magnitudes
   - Handles multicollinearity between features effectively
   - Provides more stable predictions when features are correlated
   - Better when all features contribute somewhat to the prediction
   - **Formula:** Loss = MSE + α × Σβ²

4. **Coefficient Analysis:**
   - Linear Regression coefficients serve as baseline for comparison
   - Lasso may eliminate less important features (coefficients = 0)
   - Ridge reduces all coefficients but keeps them non-zero
   - Coefficient comparison reveals impact of regularization on feature importance

5. **Feature Importance Insights:**
   - `MedInc` (Median Income) remains strongest predictor across all models
   - Geographic features (Latitude, Longitude) show weaker but consistent correlations
   - Regularization helps identify which features truly drive house values
   - Some features may be eliminated by Lasso, indicating redundancy

### Key Insights:

1. **Regularization Benefits:**
   - Prevents overfitting by penalizing large coefficient values
   - Improves model generalization to unseen data
   - L1 provides built-in feature selection capability
   - L2 handles multicollinearity more gracefully

2. **When to Use Each Model:**
   - **Linear Regression:** Baseline model, when interpretability is key and overfitting isn't a concern
   - **Lasso (L1):** When you need feature selection, have high-dimensional data, or believe many features are irrelevant
   - **Ridge (L2):** When all features are potentially relevant, features are correlated, or you want stable predictions

3. **Feature Scaling Importance:**
   - Regularization is sensitive to feature scales
   - Standardization (mean=0, std=1) ensures fair penalization across features
   - Without scaling, features with larger scales would be penalized more

4. **Model Selection Considerations:**
   - Choice between L1 and L2 depends on problem context and data characteristics
   - Cross-validation helps determine optimal regularization strength (alpha parameter)
   - Elastic Net (combination of L1 and L2) can be explored for best of both approaches

### Comparison with Day 1:

- Day 1 implemented basic Linear Regression as baseline
- Day 3 extends with regularization techniques to improve generalization
- Regularized models build upon linear regression fundamentals
- Performance improvements demonstrate value of addressing overfitting

### Next Steps:
- Experiment with different alpha (regularization strength) values
- Try Elastic Net regression (combines L1 and L2 penalties)
- Compare with non-linear models (Decision Trees, Random Forests)
- Explore polynomial features with regularization
- Investigate feature interactions and engineering