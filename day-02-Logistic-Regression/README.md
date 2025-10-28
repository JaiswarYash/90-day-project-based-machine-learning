# Student Performance Prediction using Logistic Regression

A machine learning project that predicts student academic outcomes using logistic regression on student performance data.

## Project Description

This project analyzes student performance data to predict grades based on demographic information, educational background, and test scores. It demonstrates a complete end-to-end machine learning workflow for classification tasks.

## Objective

Predict student grade categories (A-F) using various features including:
- Demographic information (gender, race/ethnicity)
- Educational background (parental education level)
- Resources (lunch type, test preparation course)
- Academic performance (math, reading, writing scores)

## Dataset

**Source:** StudentsPerformance.csv

**Size:** 1000 students, 11 features

**Features:**
- Original: gender, race/ethnicity, parental education, lunch, test prep course, math score, reading score, writing score
- Engineered: total score, percentage, grade

## Algorithm Used

**Logistic Regression** - A statistical classification method that predicts the probability of class membership.

**Key Concepts:**
- Uses sigmoid function to map predictions to probability range [0,1]
- Decision boundary typically set at 0.5 probability
- Optimized using log loss (cross-entropy) cost function

## 🔧 Implementation Steps

1. **Data Loading & Exploration**
   - Load CSV dataset
   - Check for missing values and duplicates
   - Analyze feature distributions

2. **Feature Engineering**
   - Calculate total scores across subjects
   - Compute percentage scores
   - Assign letter grades based on performance

3. **Data Preprocessing**
   - Encode categorical variables
   - Split data into training and testing sets
   - Feature scaling if needed

4. **Model Training**
   - Train logistic regression classifier
   - Optimize model parameters

5. **Evaluation**
   - Predict on test set
   - Analyze accuracy and performance metrics

## Key Findings

- Most students fall in middle grade ranges (C, D, E)
- Strong correlation between test scores and final grades
- Multiple factors influence academic performance
- Model can identify at-risk students for early intervention

## Learning Outcomes

- Understanding logistic regression fundamentals
- Feature engineering techniques
- Complete ML workflow implementation
- Educational data analytics applications

## Use Cases

- Predicting student performance outcomes
- Educational resource allocation
- Early identification of struggling students
- Academic intervention planning

## Project Structure

```
├── StudentsPerformance.csv    # Dataset
├── analysis.ipynb             # Jupyter notebook with full analysis
├── model.py                   # Model training code
└── README.md                  # Project documentation
```

## Technologies Used

- Python
- Pandas (data manipulation)
- NumPy (numerical operations)
- Scikit-learn (machine learning)
- Matplotlib/Seaborn (visualization)

## Conclusion

This project demonstrates how simple classification algorithms like logistic regression can provide valuable insights for educational analytics and help predict student outcomes based on multiple factors.

---

**Day 2 of Machine Learning Journey** 