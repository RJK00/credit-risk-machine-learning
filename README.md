## Using Logistic Regression vs Random Forest Classifier model to determine credit risk

#### Prediction: 
Logistic regression will out-perform the Random Forest model because the dataset is relatively simple and does not contain an overwhelming number of noise variables. 

#### Results:
 As predicted, logistic regression performed with a higher average accuracy score (test = 0.9937 or 99.37%) compared to the random forest classifier model, which yielded ~0.9915 (99.15% accuracy rate). Given the slim dataset, it is likely unwise to further reduce its complexity through methods such as feature selection. Doing so may increase overfitting risk and ultimately reduce the overall accuracy of the models, as attested by the values returned by <code>test_model_fs()</code>. 

Increasing the number of estimators(trees) from 100 to 1000 in the random forest classifier model yielded slightly higher nominal scores for accuracy (+0.015%): 0.99153 and 0.99169 respectively. 

#### Further analysis:
A two-sample pairwise t-test could be performed to quantify the statistical significance of the differences in performance metrics between the two models.