                                    Practical Application III: Comparing Classifiers
                                            Telemarketing of Banking Products

The Marketing activities of any organization can be carried over in different platforms however, marketing a Bank’s product requires more specific details and description. To carry out the same in a virtual platform, different methods of marketing and their practical applications were compared using the classifiers. 

To run the application, the dataset from direct marketing campaigns (phone calls) of a Portuguese banking institution was used and the objective was to predict if the client will subscribe a term deposit. The performance comparison classifiers like Logistic Regression, Decision Trees, and Support Vector Machines were carried out using the data related to marketing bank products over the telephone. After understanding the task and features, data was encoded, and the prepared data was split into a train and test set.  

  **1.	Baseline & Simple Model: Logistic Regression Performance Classifier:**
Dummy Classifier used to fine baseline model that other classifiers should aim to beat. Accuracy score to aim - Baseline Model Score: 0.8865015780529255
To build a simple model on the template data, logistic regression was used. The accuracy of the model and its inference is given below in the reference (ROC Curve Comparison)
Logistic Model Score: 0.9113862588006798
![image](https://github.com/muralikandan/aiml-assignment-17/assets/5803282/0a236dcc-c2ae-4a6c-9163-fff95198cd57)

**2.	Comparison of Models without tuning:**
The performance of default Logistic Regression model was compared to default setting of three type KNN algorithm, Decision Tree, and SVM models and the findings were done on the Data Frame comprising Model, Train Time, Train Accuracy, Test Accuracy. The Model Comparison graph is given below where the regression model was compared with other models 

![image](https://github.com/muralikandan/aiml-assignment-17/assets/5803282/3074ffdf-8455-455c-9f36-23ca434a1122)

![image](https://github.com/muralikandan/aiml-assignment-17/assets/5803282/18643b16-dcde-495b-b58c-aa46732ada06)

With default setting Logistic Regression model perform well when considering combination trailing time, train & test accuracy, and AUC metric. KNN model though fast enough to train but test accuracy and AUC are falling behind.   Decision tree test accuracy and AUC not better. Though SVM accuracies good but considering training time and slight down in AUC can be ranked as third among four models’ comparison.    

**3.	Model Comparison with tuning / improvement:**
As part of improving/tuning model and compare different algorithm to choose between which algorithm to align with for model. Used GridSearch technique for hyperparameter tuning, cross validation and metrics adjustment. Comparison of all those algorithm-based models depicted as below both AUC & performance matrix.

Grid Search results with best param for four algorithms!
Best parameters for Logistic Regression: {'clf__C': 1, 'clf__penalty': 'l2', 'clf__solver': 'liblinear'}
  Test accuracy of best model: 0.9114, Training time: 66.2672s
Best parameters for KNN: {'clf__n_neighbors': 7}
  Test accuracy of best model: 0.9042, Training time: 27.1098s
Best parameters for Decision Tree: {'clf__max_depth': 5}
  Test accuracy of best model: 0.9150, Training time: 9.1622s
Best parameters for SVM: {'clf__C': 1, 'clf__kernel': 'rbf'}
  Test accuracy of best model: 0.9118, Training time: 
![image](https://github.com/muralikandan/aiml-assignment-17/assets/5803282/d13bd989-53e9-4df8-bfb6-6f09bac65f1e)

![image](https://github.com/muralikandan/aiml-assignment-17/assets/5803282/1ec6cfc7-61e2-40f5-82f0-b8c2979933a6)

  ![image](https://github.com/muralikandan/aiml-assignment-17/assets/5803282/1fd31997-9123-4fe6-bd41-06b87a645e94)

  
  ![image](https://github.com/muralikandan/aiml-assignment-17/assets/5803282/452c7725-d43d-4558-85b2-ccb23bee0f51)


Comparing all four algorithms, Decision Tree performing in terms of training time and accuracies but little lag in AUC. Decision Trees can struggle with imbalanced classes because they tend to Favor majority classes. 

**Conclusion**
Considering training accuracy, test accuracy, and AUC, Logistic Regression would be better model to align with nominal performance. KNN has very less AUC and SVM took almost 100 X times to perform, also not meant to handle large data set.

Impactful feature standpoint, correlation matrix (refer to correlation heatmap) and description provided that’s clear that having lengthy call with client with whom previous campaign attempted. 
