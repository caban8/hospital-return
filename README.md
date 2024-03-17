
# Likelihood of being readmitted to hospital - Exploration and Prediction Modeling

## Overview
This analysis attempts to identify the factors behind the likelihood of a patient's readmission to the hospital within 30 days. 
It employs a combination of exploratory analyses, theoretical thinking, and statistical modelling through logistic regression and decision tree models. 
The applied approach builds upon the analysis previously carried by
[`ALIA107`](https://www.kaggle.com/code/bvc5283/healthcare-prediction/notebook). 
The dataset was obtained from https://github.com/HannahHan3/758T_PredictiveModeling

Guided by the following objectives, I aimed:

-   To refine the code for increased efficiency,
-   To conduct a more detailed exploratory data analysis (EDA),
-   To identify possible interaction effects that could impact the model's predictions,
-   To compare models in terms of classification error rate.

More emphasis was put on the *interpretability* aspect than *prediction*.

## Contents
- **Data Import and Preprocessing**: Data cleaning, variables' recoding, and preparation for modeling.
- **Exploratory Data Analysis (EDA)**: Bar plots, histograms, and density plots for univariate and bivariate exploration. Mosaic plots for 2-way interactions.
- **Modeling**: Implementation of logistic regression and decision tree models, including variations of logistic regression with different coefficient constraints and interaction effects.
- **Evaluation**: Comparison of model performance based on classification error rate.

## Key Findings
- **Feature engineering**: Simple transformations were applied, reducing the number of time-variables levels and including missing data as separate levels in the case of categorical predictors.
- **EDA Insights**: Among the more interesting observations were that early-morning hours of admission, smaller charges for the treatment, and being between 50 and 60 years old were associated with higher rates of returns.
- **Interaction Effects**: Out of many - among those who were sent to home or self-care, having a diagnosis was not associated with rates of return. In contrast, for patients discharged to other types of care, being diagnosed was associated with odds of return that were three times lower.
- **Performance Comparison**: Both gradient-boosted trees and random forests achieved the best classification accuracy, identifying age and charges for the treatment as the most important predictors. However, they differed in the ranking of the predictors that followed.


## Conclusions
The gradient-boosted tree and random forest models achieved the highest classification accuracies, with 77.8% and 77.6% respectively.
Therefore, for objectives focused solely on prediction, they should be preferred over logistic regression models. 
However, a deeper theoretical analysis of interactions could yield a better overall understanding of the factors affecting a patient's return to the hospital.
This, in turn, could motivate more targeted research aimed at addressing specific questions. For example, examining the differences in diagnoses between patients discharged to home versus those discharged to other types of care could elucidate why a diagnosis in the latter group reduces the likelihood of return.

