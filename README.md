# Multi-Class-Prediction-of-Obesity-Risk
## Overview

The following repositry contains an analysis about the possible factors that play an important role in influencing a higher obesity risk.

![image](https://github.com/lievda01/Multi-Class-Prediction-of-Obesity-Risk/assets/137839618/7b022202-7ca2-4e96-a481-b7666dd95461)

## Data

This dataset consists in 20,758 entries about individual with certain characteristics and each one is labeled in one of the following categories:

  1. Insufficient_Weight
  2. Normal_Weight
  3. Obesity_Type_I
  4. Obesity_Type_II
  5. Obesity_Type_III
  6. Overweight_Level_I
  7. Overweight_Level_II

The variables considered are:


   1. id
   2. Gender
   3. Age
   4. Height
   5. Weight
   6. family_history_with_overweight
   7. FAVC (Frequent consumption of high caloric food)
   8. FCVC (Frequency of consumption of vegetables)
   9. NCP (Number of main meals)
   10. CAEC (Consumption of food between meals)
   11. SMOKE
   12. CH2O (Consumption of water daily)
   13. SCC (Calories consumption monitoring)
   14. FAF (Physical activity frequency)
   15. TUE (Time using technology devices)
   16. CALC (Consumption of alcohol)
   17. MTRANS (Transportation used)                                 
    

## Approach

To work with this dataset the following three models were proposed:

  1. XGBoost
  2. Logistic Regression
  3. Logistic Regression with PCA

The idea of including PCA was to analyze whether using this technique before performing a Logistic Regression could enhance the model's explanatory power and could potentially bring a higher accuracy, precision and recall.

## Solution

As we can see, among all three models, XGBoost does a better job with overall higher results for accuracy, precision and recall. In terms of the Logistic Regression, it falls behind the XGBoost in terms of the previously mentioned metrics but it is close. Interestingly, when we apply PCA and then run a Logistic Regression, the accuracy drops notably. This is happening since for all models Height, Weight and Age play an important role to determining the Obesity Risk category and PCA is not able to find good combinations to create components that can explain the variance in the data.

For this particular problem, XGBoost showed the best performance.

## References

The dataset was part of a Kaggle competition https://www.kaggle.com/competitions/playground-series-s4e2/data
