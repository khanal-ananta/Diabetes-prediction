# Diabetes-prediction

About DATA:

This dataset is originally from the National Institute of Diabetes and Digestive and Kidney Diseases. The objective of the dataset is to diagnostically predict whether or not a patient has diabetes, based on certain diagnostic measurements included in the dataset. Several constraints were placed on the selection of these instances from a larger database. In particular, all patients here are females at least 21 years old of Pima Indian heritage.

The datasets consists of several medical predictor variables and one target variable, Outcome. Predictor variables includes the number of pregnancies the patient has had, their BMI, insulin level, age, and so on.

Columns

    1.Pregnancies = Number of times pregnant

    2.Glucose = Plasma glucose concentration a 2 hours in an oral glucose tolerance test

    3.BloodPressure = Diastolic blood pressure (mm Hg)

    4.SkinThickness = Triceps skin fold thickness (mm)

    5.Insulin = 2-Hour serum insulin (mu U/ml)

    6.BMI = Body mass index (weight in kg/(height in m)^2)

    7.DiabetesPedigreeFunction = Diabetes pedigree function

    8.Age = Age (years)

    9.Outcome = Class variable (0 or 1) 268 of 768 are 1, the others are 0
    
    
    
 ### Description of the model buidling process

1) Data cleaning : Missing data analysis is done by replacing nan and data having 0 value with mean.

2) Data analysis and visualization : Data is analyse and visualize by using histogram, scatter plot and heatmap.

3) Handel categorical data : Categorical data is handled by using get dummy variable approach.

4) Split data set : Total data set is splited into train and test data set in the ratio 4:1.

5) Centering and scaling : Centering and scaling is done by using StandardScalar.

6) Build models : Regression is done using "Decision Tree", 
                                           "Random Forest",
                                           "Naive Bayes", 
                                           "Logistic Regression",
                                           "Support Vector Machine",
                                           "XGboost" . 
                                                                      
 7) Build pipelines of classifiers : Pipelines of above mentioned classifiers are build to achieve the following results:
 
Decision Tree
Accuracy:  0.7662337662337663
Balanced Accuracy:  0.7601908928216345
Precision/Recall/F1 score:  (array([0.87368421, 0.59322034]), array([0.77570093, 0.74468085]), array([0.82178218, 0.66037736]), array([107,  47], dtype=int64))
Confusion Matrix:  [[83 24]
 [12 35]]
AUC:  0.7601908928216345
              precision    recall  f1-score   support

           0       0.87      0.78      0.82       107
           1       0.59      0.74      0.66        47

    accuracy                           0.77       154
   macro avg       0.73      0.76      0.74       154
weighted avg       0.79      0.77      0.77       154



Random Forest
Accuracy:  0.7987012987012987
Balanced Accuracy:  0.711970570689998
Precision/Recall/F1 score:  (array([0.80645161, 0.76666667]), array([0.93457944, 0.4893617 ]), array([0.86580087, 0.5974026 ]), array([107,  47], dtype=int64))
Confusion Matrix:  [[100   7]
 [ 24  23]]
AUC:  0.7119705706899979
              precision    recall  f1-score   support

           0       0.81      0.93      0.87       107
           1       0.77      0.49      0.60        47

    accuracy                           0.80       154
   macro avg       0.79      0.71      0.73       154
weighted avg       0.79      0.80      0.78       154



Naive Bayes
Accuracy:  0.7857142857142857
Balanced Accuracy:  0.7384171803539471
Precision/Recall/F1 score:  (array([0.83636364, 0.65909091]), array([0.85981308, 0.61702128]), array([0.84792627, 0.63736264]), array([107,  47], dtype=int64))
Confusion Matrix:  [[92 15]
 [18 29]]
AUC:  0.7384171803539471
              precision    recall  f1-score   support

           0       0.84      0.86      0.85       107
           1       0.66      0.62      0.64        47

    accuracy                           0.79       154
   macro avg       0.75      0.74      0.74       154
weighted avg       0.78      0.79      0.78       154



Logistic Regression
Accuracy:  0.8181818181818182
Balanced Accuracy:  0.7558162656591767
Precision/Recall/F1 score:  (array([0.83760684, 0.75675676]), array([0.91588785, 0.59574468]), array([0.875     , 0.66666667]), array([107,  47], dtype=int64))
Confusion Matrix:  [[98  9]
 [19 28]]
AUC:  0.7558162656591767
              precision    recall  f1-score   support

           0       0.84      0.92      0.88       107
           1       0.76      0.60      0.67        47

    accuracy                           0.82       154
   macro avg       0.80      0.76      0.77       154
weighted avg       0.81      0.82      0.81       154



Support Vector Machine
Accuracy:  0.7727272727272727
Balanced Accuracy:  0.7052097832571087
Precision/Recall/F1 score:  (array([0.81034483, 0.65789474]), array([0.87850467, 0.53191489]), array([0.84304933, 0.58823529]), array([107,  47], dtype=int64))
Confusion Matrix:  [[94 13]
 [22 25]]
AUC:  0.7052097832571087
              precision    recall  f1-score   support

           0       0.81      0.88      0.84       107
           1       0.66      0.53      0.59        47

    accuracy                           0.77       154
   macro avg       0.73      0.71      0.72       154
weighted avg       0.76      0.77      0.77       154



XGboost
Accuracy:  0.8246753246753247
Balanced Accuracy:  0.8261085702923046
Precision/Recall/F1 score:  (array([0.91666667, 0.67241379]), array([0.82242991, 0.82978723]), array([0.86699507, 0.74285714]), array([107,  47], dtype=int64))
Confusion Matrix:  [[88 19]
 [ 8 39]]
AUC:  0.8261085702923046
              precision    recall  f1-score   support

           0       0.92      0.82      0.87       107
           1       0.67      0.83      0.74        47

    accuracy                           0.82       154
   macro avg       0.79      0.83      0.80       154
weighted avg       0.84      0.82      0.83       154


                 
7) Hyperparameter optimization : Randomized searchCV with 4 fold cross validation is used to find the optimum values of parameter for xgboost regression.

8) The final value of R2 we get is 0.82 which is quiet good for this project.   

