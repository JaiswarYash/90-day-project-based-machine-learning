# Bike Sharing Demand Prediction
```
A Decision Tree machine learning project that predicts bike rental demand using historical usage patterns and environmental factors.
```
### Dataset
```
Source: UCI Machine Learning Repository - Bike Sharing Dataset
Size: 17,379 instances with 13 features
Target: Total bike rental count (cnt)
```

### Features
[-]Temporal: season, year, month, hour, holiday, weekday, working day
[-]Weather: temperature, humidity, windspeed, weather conditions
[-]Derived: day of month, day of year

**What is a Decision Tree?**
A Decision Tree is a supervised learning algorithm that recursively partitions data into subsets by asking a series of questions about features. It creates a tree-like structure where:

Internal nodes represent feature tests
Branches represent decision outcomes
Leaf nodes contain predictions

The algorithm splits data to create the most homogeneous (pure) subsets possible.
Models Implemented
Decision Tree Regressor
Predicts continuous bike rental counts.

### Mathematical Intuition:
```
Splits data to minimize variance within subsets
Splitting Criterion: Minimize Mean Squared Error (MSE)

  MSE = Σ(y_true - y_pred)² / n
```
- At each node, selects the feature and threshold that maximizes information gain
- Predictions are the mean of target values in each leaf node


### Decision Tree Classifier
Categorizes rental demand into classes.

**Mathematical Intuition**:
- Uses impurity measures to create homogeneous subsets
- **Information Gain**: 
```
  IG = Entropy(parent) - Weighted_Average × Entropy(children)
```
- **Gini Impurity**: 
```
  Gini = 1 - Σ(p_i)²
where p_i is the probability of class i

Splits minimize impurity, maximizing class separation
```
### Key Techniques:

Feature engineering from temporal data
Hyperparameter tuning with GridSearchCV
Cross-validation for model evaluation
Tree visualization for interpretability

### Tech Stack

Python
scikit-learn
pandas, numpy
matplotlib/seaborn

### Results

Identified key demand drivers through feature importance analysis
Demonstrated temporal and weather patterns significantly impact rentals
Balanced model complexity vs. performance through hyperparameter optimization

### Skills Demonstrated
✓ Decision Tree regression & classification
✓ Feature engineering
✓ Model evaluation (MSE, R², MAE)
✓ Hyperparameter tuning
✓ Data visualizationRetryClaude can make mistakes. Please double-check responses.