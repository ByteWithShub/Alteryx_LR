# Alteryx Linear Regression – Real Estate Prediction

## Files
- lab_ML_Alty.yxmd – Main Alteryx workflow
- final_real_estate.csv – Dataset

## Workflow Summary
- Data types corrected using Select tool
- Association Analysis used to study correlations with price
- Data split 80/20 using Create Samples
- Linear Regression trained on training set
- Test data scored using Score tool
- Absolute error calculated using Formula tool

## How to Run
1. Open lab_ML_Alty.yxmd in Alteryx Designer
2. Ensure Input Data points to final_real_estate.csv
3. Run workflow
4. View predictions and error in final Browse tool
