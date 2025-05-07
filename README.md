# StudentDepressionAnalysis

# Authors
Gavin Barro, Nathan Carter, Jack Bresnahan

# Description
Introduction
This study investigates how financial stress, work study hours, and gender are associated with depression among students. The dataset includes 27,900 observations with three variables: two quantitative (Financial.Stress and Work.Study.Hours) and one qualitative (Gender). The outcome variable Depression is binary (0 = Not Depressed, 1 = Depressed).
Goals/Hypotheses:
H₀: There is no difference in financial stress or work study hours between depressed and non-depressed students.


H₁: Depressed students experience significantly higher financial stress and work study hours than non-depressed students.


Additionally, we test if gender is associated with depression.


Model Assumptions:
 For the t-tests:
Data is approximately normally distributed (large sample size justifies use of Central Limit Theorem).


No significant outliers were assumed due to sample size smoothing effects.


Observations are independent.


Homogeneity of variance is not assumed (Welch's t-test used).


Variables tested are continuous (or treated as such).


For the logistic regression models:
Binary dependent variable.


Independence of observations.


No multicollinearity among predictors.


Logit is a linear function of predictors.


Large sample size ensures stability.


Descriptive Statistics
Quantitative Variables:
Financial Stress


Min: 1, 1st Qu.: 2, Median: 3, Mean: 3.14, 3rd Qu.: 4, Max: 5


NA's: 3


Work Study Hours


Min: 0, 1st Qu.: 4, Median: 8, Mean: 7.16, 3rd Qu.: 10, Max: 12


These distributions suggest a moderate average financial stress and work-study workload among students, with some skew toward higher values in those with depression.
Qualitative Variables:
Gender:


Female: 12,354 (44.3%), Male: 15,547 (55.7%)


Depression:


Not Depressed (0): 11,565 (41.4%)


Depressed (1): 16,336 (58.5%)


Modeling and Inferential Statistics
T-tests:
Financial Stress vs. Depression:


t = -65.08, p < 2.2e-16


Mean FS (Non-depressed): 2.52


Mean FS (Depressed): 3.58


Interpretation: Financial stress is significantly higher among depressed students.


Work Study Hours vs. Depression:


t = -34.94, p < 2.2e-16


Mean WSH (Non-depressed): 6.24


Mean WSH (Depressed): 7.81


Interpretation: Depressed students work significantly more hours per week.


Logistic Regression Models:
Model 1: Depression ~ Financial.Stress


Coefficient: 0.554, p < 2e-16


Interpretation: For each unit increase in financial stress, odds of depression increase significantly.


Pseudo R²: 0.101 (moderate explanatory power)


Model 2: Depression ~ Work.Study.Hours


Coefficient: 0.116, p < 2e-16


Interpretation: Each additional work study hour slightly increases odds of depression.


Model 3: Depression ~ Gender


GenderMale: Coefficient = 0.0073, p = 0.764


Interpretation: Gender is not significantly associated with depression in this model.


Model 4: Combined Model


Formula: Depression ~ Gender + Financial.Stress + Work.Study.Hours


Financial Stress and Work Study Hours remain significant; Gender does not.


AIC = 32,981, Residual Deviance = 32,973 (better than individual models)


Model Diagnostics
Classification Accuracy (Model 1 - Financial Stress only):


55.1% accuracy (modest performance using 0.5 threshold)


Confusion Matrix:


Shows that the model is slightly better than random guessing but not highly predictive.


Pseudo R² (Model 1):


0.101 → Indicates that 10.1% of the variability in depression is explained by financial stress alone.

Conclusion
This study provides evidence that both financial stress and work study hours are significantly associated with student depression. Gender, however, was not found to be a significant predictor. The models show statistical significance but only moderate predictive power, indicating that additional variables (such as academic or family factors) may be needed to improve accuracy.
Limitations:
Potential unmeasured confounders


Self-reported data may introduce bias


Assumptions of normality and homogeneity not formally tested


Future Improvements:
Include more psychosocial variables


Use cross-validation to improve generalizability


Explore non-linear models or machine learning methods for prediction







# Project Guidelines

1. Data: Find the data set that has at three variables (quantitative  and qualitative)- describe your data (in the intro) 

2. Goal (s) Have clear goals/hypothesis or hypotheses-state them in the intro section'

3. Model assumptions (State them in the intro section)
   
4. Descriptive Statistics  (A second section- both descriptive and numerical )
   
5. Present your model -check if your model is significant ...write it down
   
6. Model Diagnostics-- if the residual plots, confusion matrix, MSE etc (predictive ability etc)
   
7. Conclusion :  Final finding, limitations and how you can improve your model.
