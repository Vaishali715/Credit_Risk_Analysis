# Credit_Risk_Analysis
## Overview of the analysis:
Credit risk is very tough to predict. In this project we want to take a look at how all the factors in our loan_status csv help predict whether someone is low or high risk status. One method that data scientists use for this type of issue is creating a model and then evaluate and train the models that they create. In this specific project we are using imbalanced-learn and scikit-learn libraries to build models and evalute them using a resampling method. In the first couple of models I oversampled the data using randomoversampler and smote algorithms and undersample the data with the clustercentroid algorithm. In the remaining models I used a combination approach to over and undersample the data using smoteenn. Finally, I compared two machine learning models that minimize bias, balancedrandomforestclassifier and easyensembleclassifier.

## Results:
Naive Random Oversampling results: Our balanced accuracy test it 66%, the precision for the high_risk has a very low positivity at 1% and the recall is 74%

![Image](https://github.com/Vaishali715/Credit_Risk_Analysis/blob/main/Resources/naive_random_oversampling.png)

SMOTE oversampling results: the accuracy score is 65.3%, the precision for the high_risk loans has a low positvity again at 1% and recall is 68% overall

![Image](https://github.com/Vaishali715/Credit_Risk_Analysis/blob/main/Resources/Smote_oversampling.png)

Undersampling results: balanced accuracy score is 65.3% overall, the precision is at 99% and the recall is 40%

![Image](https://github.com/Vaishali715/Credit_Risk_Analysis/blob/main/Resources/Smote_undersampling.png)

Combination(over and undersampling) results: balanced accuracy score is 54.4% the precision is 99% and the recall is 57% overall

![Image](https://github.com/Vaishali715/Credit_Risk_Analysis/blob/main/Resources/Combination_under_over_sampling.png)

Balanced Random Forest Classifier results: the accuracy score is 77.2% the precision is 99% and the recall is 88%

![Image](https://github.com/Vaishali715/Credit_Risk_Analysis/blob/main/Resources/Balanced_random_classifier.png)

Easy Ensemble AdaBoost Classifier results: the accuracy score is 91.7% the precision is 99% and the recall is 94%

![Image](https://github.com/Vaishali715/Credit_Risk_Analysis/blob/main/Resources/Ensemble_adaboost_classifier.png)

## Summary:
In the first four models we undersampled, oversampled and did a combination of both to try and determine which model is best at predicting which loans are the highest risk. The next two models we resampled the data using ensemble classifiers to try and predict which which loans are high or low risk. In our first four models our accuracy score is not as high as the ensemble classifiers and the recall in the oversampling/undersampling/mixed models is low as well. Typically in your models you want a good balance of recall and precision which is why I recommend the ensemble classifiers over the first four models. It appears that the Easy Ensemble had the best balance of all the models because of it's high accuracy score and good balance of precision and recall scores.
