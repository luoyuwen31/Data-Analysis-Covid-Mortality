# Data Mining on Factors of Covid 19 Mortality
## Dataset Description
1.	Data Source: The COVID Tracking Project (https://covidtracking.com/data)    
2.	Data size: 2.7MB  
3.	Variables Information: 
- date (YYYY/MM/DD)<br>
- state(name of state in the United States)<br>
-	death cases (Confirmed, Increased, Probable )<br>
-	hospitalized cases (Total, Cumulative,Currently, Increase)<br>
-	In ICU (Cumulative, Currently)<br>
-	Negative (Total negative cases, Increased cases)<br>
-	NegativeTests (Antibody,PeopleAntibody,Viral)<br>
-	Ventilator (Currently, Cumulative)<br>
-	Positive (Total, CasesViral,Increase, Score)<br>
-	Positive Test (Antibody, Antigen, PeopleAntibody, PeopleAntigen, Viral)<br>
-	Recovered<br>
-	Total Test (EncountersViral, EncountersViralIncrease, Results, ResultsIncrease, Antibody, Antigen, PeopleAntibody, PeopleAntigen, PeopleViral, PeopleViralIncrease, Viral, ViralIncrease)<br>

## Problem of Interest
In this project, we aim to select influencial factors of Covid 19 death. 

## Methodology
There are two types of predictors in the project, numerical predictor 'deathIncrease' and categorical predictor 'variable death direction'.<br>
In each predictors, we apply three steps, features selection(BIC/Stepwise/Randomforest), model fitting(KNN/SVM/Logistic Regression/LDA/QDA) and coefficient score(Ridge/Lasso/Elastic Net)

1. In Categorical Part
-	Transformed linear variables into classification type and converted Time Series Dataset into a proper format for data mining process <br>
-	Applied classification (Logistic/LDA/QDA) models on the train set<br>
-	Compared AIC, ROC on the test set, increase accuracy from 40% to 60%
-	Reduced model variables from 16 to 4 to fit the best model <br>

2. In Numerical Part
-	Applied linear regression (KNN/SVM) on the train set<br>
-	Compared AIC, ROC on the test set , increase accuracy from 40% to 78%
-	Reduced model variables from 16 to 4 to fit the best model <br>
  
  
