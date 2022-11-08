## Using Logistic Regression vs Random Forest Classifier model in determining credit risk

### Purpose:
Commonly, banks or lending services providers may allow individual investors to partially fund newly issued personal loans or offer derivatives of previously issued loans on the secondary market. In order to limit unnecessary exposure to hazards in this vast marketplace, smart investors seek effecient and accurate models for classifying risk. 

The purpose of this project was to create two machine learning models and to compare the performance (accuracy rates) of the respective models in classifying risk level of loans.

### Prediction: 
Logistic regression will out-perform the Random Forest model because the dataset is relatively simple and contains a small sample size. 


### Results:
 As predicted, logistic regression performed with a higher average accuracy score *[0.9937 or 99.37%]* compared to the random forest classifier model, which yielded *0.9915 (99.15% accuracy rate)*. 
 Given the slim dataset, it is likely unwise to further reduce its complexity through methods such as feature selection. Doing so may increase overfitting risk and ultimately reduce the overall accuracy of the models, as attested by the values returned by <code>test_model_fs()</code>.

 The accuracy of the logistic regression model was improved *[to 0.9943 or 99.43%]* by tuning its hyper parameters with <code>test_model_param()</code>, which uses the <code>RandomizedSearchCV</code> method from scikit-learn to perform a randomized search on input hyper parameter ranges.
 
Increasing the number of estimators(trees) from 100 to 1000 in the random forest classifier model yielded slightly higher nominal scores for accuracy *(+0.015%)*: *0.99153* and *0.99169* respectively. 

### Further analysis:
A two-sample pairwise t-test could be performed to quantify the statistical significance of the differences in performance metric between the two models.
