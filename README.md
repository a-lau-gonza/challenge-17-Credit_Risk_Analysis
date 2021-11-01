# Credit Risk Analysis

## Overview of the loan prediction risk analysis
Credit card risk is... *risky*! As credit becomes a necessary staple in almost every individual's lives in the United States, the number of dollars lost due to credit card risk jumps up in tandem. Using machine learning with the assistance of SMOTE, RandomOverSampler, ClusterCentroids, SMOTEENN, BalancedRandomForestClassifier and EasyEnsembleClassifier, the goal of this challenge is to navigate the large, multitrillion dollar, data world of credit card risk.

## Results
For the __Balanced Accuracy Scores__, the best results are closer to __1__ and the closer to __0__ the worse. 
For __Precision__, the scores given as True Positive will represent *truly high risk* where False Positive will represent a prediciton of high risk that doesn't truly fit into the category, the true shall be true for True and False Negatives.
For the __Recall Scores__, they will represent the sensitivity that will identify missed positive predictions. The sensitivity is True Positive / (True Positive + False Negative).

![Resampling](Write-Up_Resources/resampling1.png)

![Resampling Test, Train, Sample](Write-Up_Resources/resampling_tts.png)

With the Naive Random Oversampling the __balanced accuracy score__ that returned was a *64.6%*. __Recall scores__ are *63% for high risk and 66% for low risk*. These are dangerously close to 50/50 on determining high and low risk respectively. __Precision__ for *high risk is 1% and low risk is 100%*.
![Naive Random Oversampling](Write-Up_Resources/resampling_nr_over.png)

SMOTE again comes with again a __balanced accuracy score__ that returned was a *64.6%*. __Recall scores__ are *63% for high risk and 66% for low risk*. __Precision__ for *high risk is 1% and low risk is 100%*.
![SMOTE](Write-Up_Resources/resampling_smote.png)

For Undersampling, again the __balanced accuracy score__ that returned was a *64.6%*. However, the __recall scores__ are *59% for high risk and 43% for low risk*. These are even more ominous numbers than the previous two. __Precision__ stays at *high risk for 1% and low risk as 100%*.
![Undersampling](Write-Up_Resources/resampling_under.png)

For SMOTEENN, the __balanced accuracy score__ that returned was a *51%*. The __recall scores__ are *69% for high risk and 58% for low risk*. __Precision__ stays at *high risk for 1% and low risk as 100%*.
![SMOTEENN](Write-Up_Resources/resampling_smoteenn.png)

![Ensemble Test, Train, Sample](Write-Up_Resources/ensemble_tts.png)

For Balanced Random Forest Classifier, the __balanced accuracy score__ that returned was a *56.3%*. The __recall scores__ are *49% for high risk and 63% for low risk*. __Precision__ stays at *high risk for 1% and low risk as 100%*.
![Ensemble Balanced Random Forest Classifier](Write-Up_Resources/ensemble_brfc.png)

![Balanced Random Forest Classifier](Write-Up_Resources/ensemble_brfc2.png)

For Easy Ensemble Classifier, the __balanced accuracy score__ that returned was a *92.5%*. The __recall scores__ are *91% for high risk and 94% for low risk*. __Precision__ stays at *high risk for 7% and low risk as 100%*.
![Easy Ensemble Classifier](Write-Up_Resources/ensemble_eec.png)



## Summary
With all the learning models run through, the choice for a recommendation is clear, as the Easy Ensemble Classifier model provided the highest percentage scores, closest to 1, out of all the other models and it wasn't even close. With a __balanced accuracy score__ that returned as a *92.5%*, __recall scores__ at *91% for high risk and 94% for low risk* and __Precision__ at *high risk for 7% and low risk as 100%*, EEC far outclassed all other models who had closer figures to *50-65%*. Much too close to a coin toss for probability in the world of credit risk where billions could be lost. 
