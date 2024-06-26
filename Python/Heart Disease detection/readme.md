Modelling occurence of heart desease 

Executive Summary:

Aim of the project was to create an classification algorithm to assess whether patient in hospital has occurinng heart problem. Two algorithms
has been used to tackle the problem: Logit Regression and Decision Tree. Both models showcased signs of good capability of correctly classifying
patients, with the decision tree having having higher accuracy metrics. Both models correctly classified over 80% of patients.


Data: 

Data was extracted from  https://www.kaggle.com/datasets/johnsmith88/heart-disease-dataset

The data used in the model are:
1) age - age in years
2) sex - 1:male, 0:female
3) cp - type of chest pain (from 0: least significant to 3: significant)
4) trestbps - resting blood pressure (in mm Hg on admission to the hospital)
5) chol - serum cholestoral in mg/dl
6) fbs - (fasting blood sugar &gt; 120 mg/dl) (1 = true; 0 = false)
7) restecg - resting electrocardiographic results
8) thalach - maximum heart rate achieved
9) exang - exercise induced angina (1 = yes; 0 = no)
10) oldpeak - ST depression induced by exercise relative to rest
11) slope - the slope of the peak exercise ST segment
12) ca - number of major vessels (0-3) colored by flourosopy
13) thal - hemoglobin production (1 = normal; 2 = fixed defect; 3 = reversable defect)
14) target - occurennce of heart disease ( 0 = no; 1 = yes)

For the purpose of logit model, we will use first 13 variables as explanatory (X) and 'target' variable as Y.


Logit Regression:

The first ml technique used for the analysis purpose is logit model. We will first split
the dataset to training and testing sets in 80:20 proportion. Then model will be fitted and evaluated
on its accuracy, specificity, sensitivity. Moreover, ROC Curve for the model will be created. Lastly model will be cross-validated.

Model accuracy is at 0.79 level, which indicates that 79% of all observations were classified correctly.

Model sensitivity is at 0.85 level, meaning that 85% of all observations in which heart disease occured were
classified correctly.

Model Specificity is at 0.72 level, which means that 72% of all observations in which heart disease did not occure were classified correctly.

Based on that information, we can assume that the model is reliable, as all metrics exceed 70% level.

Area under the curve is set at 0.88, which means that a randomly selected observation with heart disease is ranked higher than a randomly selected observation with no heart disease based on the predicted probabilities.

With area under the curve 0.88 we can assume that model has good classifying capabilities.

Cross validation shows us that based on the data split model accuracy can go up to 0.88 level, or drop do sub 0.8 level. However, on average model accuracy is at 0.85 level.


DECISION TREE:

The second part of the analysis is to create a decision tree to predict the occurence of heart disease.
Later, the model will be evaluated based on the same metrics as the logit model.

Decision tree is created. However, the window size makes it hard to correctly verify.
Therefore we will use the same evaluation metrics as in the logit model.

Model accuracy is at 0.99 level, which indicates that 99% of all observations were classified correctly.

Model sensitivity is at 0.97 level, meaning that 97% of all observations in which heart disease occured were
classified correctly.

Model Specificity is at 1.0 level, which means that 100% of all observations in which heart disease did not occure were classified correctly.

Based on that information, we can assume that the model is reliable, as all metrics exceed 95% level.

Area under the curve is set at 0.99, which means that a randomly selected observation with heart disease is ranked higher than a randomly selected observation with no heart disease based on the predicted probabilities.

With area under the curve 0.99 we can assume that model has great classifying capabilities.

Cross validation shows us that based on the data split model accuracy can go up to 1.0 level, or drop do sub 0.945 level. However, on average model accuracy is at 0.97 level.


KEY BUSINESS INSIGHTS:

Both algorithms can be used to classify whether patient has heart disease, with the decision tree showcasing higher accuracy. These models
can be used to assess heart problem occurence based on variety of symptons, which are used in the algorithms. As cross-validation analysis
has shown, model accuracy can be improved based on which set of data is used for training. Therefore, hospitals can use those models to
decrease the time of diagnosing patients with heart problems.

FINAL THOUGHTS 

The main goal of the project was creating a classification model to correctly classify patients with heart disease. To approach that, two model were created and later evaluated.

All metrics that were used: accuracy, sensitivity, specifity, area under ROC Curve and cross-validation metrics
indicate that decision tree model is better at correctly classifying patients with heart disease.

What further steps could be undertaken?

First of all, both model showcased good classification capabilities, and have their strengths and weaknesses.
To increase the usability of logit model we could add more explanatory variables, and check for their statistical significance. 
As for the decision tree, the plot of it is hard to read, therefore performing pruning might result in better plot as well as quicker execution time.
