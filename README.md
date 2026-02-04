# Alteryx Linear Regression – Real Estate Prediction
This project implements a complete Machine Learning pipeline in Alteryx Designer to predict residential property prices using Linear Regression. The workflow covers data preparation, correlation analysis, train-test splitting, model training, prediction, and error evaluation.

The objective is to understand how property features influence house prices and to evaluate model performance on unseen data.

![Alteryx_LR](screenshots/workflow.png)

## Files
- lab_ML_Alty.yxmd – Main Alteryx workflow
- final_real_estate.csv – Dataset

## Workflow Summary
The workflow follows these steps:
```
1. Input Data
The dataset final_real_estate.csv is loaded using the Input Data tool.

2. Data Preparation (Select Tool)
- Column data types are corrected based on the data dictionary.
- The Unknown column is removed.
- Tool annotations are added for clarity.
- This ensures the dataset is clean and suitable for predictive modeling.

3. Association Analysis
The Association Analysis tool is used to study relationships between independent variables and the target variable (price).
- Target variable: price
- Predictors: all fields except price and condo

Correlation Matrix
Interactive Heatmap
This step helps identify influential features affecting house prices.

4. Train/Test Split (Create Samples)
The dataset is randomly split into:
- 80% Training 
- 20% Testing 
The training data builds the model, while the testing data evaluates performance on unseen records.

5. Linear Regression Model
A Linear Regression model is trained using the training dataset:

- Target: price
- Predictors: all relevant independent variables
The model produces coefficients and performance statistics.

6. Test Prediction
The trained model is applied to the test dataset using the Score tool, generating predicted prices (Score_fit).

7. Error Calculation (Formula Tool)
Absolute prediction error is calculated using:

_abs([Score_fit] - [price])_
This provides a clear measure of prediction accuracy for each property.
```

## Key Concepts Demonstrated
- Data type preparation using Select tool
- Correlation analysis using Association Analysis
- Train/Test split using Create Samples
- Predictive modeling with Linear Regression
- Model evaluation using Score and Formula tools

## How to Run
1. Open lab_ML_Alty.yxmd in Alteryx Designer
2. Ensure Input Data points to final_real_estate.csv
3. Run workflow
4. View predictions and error in final Browse tool
