# Predictive-Modelling-for-Customer-Churn
The objective of this project is to build a predictive model that can predict customer churn for a given company

## REPORT
By Piyush Kumar \n
DATE: 3rd Feb 2023

**Introduction:**
This assignment aims to build a predictive model that can predict customer churn for a given company
by training different models and comparing them to choose the best out of them.

**Process:**
- After importing the data, it is analyzed thoroughly, numerical and categorical features are
identified and data is looked for missing values and duplicates.
- Univariate Exploratory Data Analysis is done separately for numerical and categorical features.
● For categorical features, Subscription% is visualized for different categories with the help
of a barplot. A clustered barplot (clustered by whether customers subscribed to a term
deposit or not) is also plotted.
● For numerical features, the histogram is plotted to see the distribution of the variable.
Also, a clustered boxplot is plotted to better visualize things in the context of the
customer’s subscription.
Data is also visually analyzed with the help of a pair plot
- Data is prepared for each of the models using feature scaling, dummy variables, one-hot
encoding, label encoding, etc wherever required.
Feature Selection for Logistic Regression is done using Recursive Feature Selection(RFE) and an
optimal number of features is decided by iteration.
- Models are fitted and evaluated on the train data first on the measures such as Precision, Recall,
F1 Score, AUC-ROC Curve, etc.
In the logistic regression case, the decision boundary is decided by analyzing the performance of
the model at different thresholds.
- Models are then applied to test data and their generalization is evaluated using the same metrics
as done with the training. (Some models are also hyperparameter tuned seeing better results)

**Results:**
The following are the metrics on the test data: (for all the models)

Logistic Regression without treating imbalanced class:
Accuracy: 0.8290346352247605
Precision: 0.3829113924050633
Recall: 0.7658227848101266
F1 Score: 0.510548523206751
Balanced Accuracy: 0.80159362760106

Logistic Regression with SMOTE:
Accuracy: 0.8496683861459101
Precision: 0.4115384615384615
Recall: 0.6772151898734177
F1 Score: 0.5119617224880382
Balanced Accuracy: 0.7748044256289524

Logistic Regression with RandomUnderSampler:
Accuracy: 0.8157700810611643
Precision: 0.3614457831325301
Recall: 0.759493670886076
F1 Score: 0.4897959183673469
Balanced Accuracy: 0.7913398296048395

Random Forest (balanced) :
Accuracy: 0.8231392778187178
Precision: 0.8866427194476038
Recall: 0.8231392778187178
F1 Score: 0.4805194805194805
Balanced Accuracy: 0.7707820863377709

**Conclusion:**
The results of the logistic regression models without treating the imbalanced class and with SMOTE and
RandomUnderSampler indicate that all models struggle to balance the accuracy and precision, with the
best results being seen in the SMOTE model with a balanced accuracy of 77.48%.
The logistic regression models show a trade-off between precision and recall, with the SMOTE model
having a higher recall (67.72%) and precision (41.15%) compared to the model without treating the
imbalanced class (38.29% precision, 76.58% recall) and the model with RandomUnderSampler (36.14%
precision, 75.95% recall).
However, the F1 score, which is a measure of the harmonic mean between precision and recall, is not
particularly high for any of the models, with the SMOTE model having the highest F1 score of 0.51.
On the other hand, the Random Forest (balanced) model has a much higher precision (88.66%) and
recall (82.31%) compared to the logistic regression models and a higher balanced accuracy (77.08%) and
F1 score (0.48) than the SMOTE logistic regression model.
These results suggest that the Random Forest (balanced) model is the best-performing model in this
evaluation.
