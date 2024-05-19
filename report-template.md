**Overview of the Analysis**

**Purpose**
* The purpose of this activity is to train and evaluate machine learning models based on loan risk. The activity use a dataset of historical lending activity from a peer-to-peer lending services company to build a model that can identify the creditworthiness of borrowers and classify the credit risk predictions.

**Target**
* The target financial information in the data is the loan status. The features in the financial data that are used to predict the loan status are loan size, interest rate, borrower income, debt to income ratio, number of accounts, derogatory marks and total debt.
 
* For the target values of loan_status there are two variables which I have tried to predict. The first set of variables have a value of '0' (value count of 75036) and these indicate that the loan is healthy. The second set of variables have a value of '1' (value count of 2500) and it means that the loan has a high risk of defaulting.

**Process**
* The machine learning process used to perform the analysis has following stages:

   Create label sets and feature Dataframe from the provided dataset.
   Split the data into training and testing datasets by using train_test_split.
   Create a logistic regression model and fit our original data into the model.
   Make predictions on testing data labels by using the testing feature data and the fitted model.
   Evaluate the model's performance by calculating accuracy scores, confusion matrix, and       
   classification report.

* scikit-learn library is used. 
* Method train_test_split is used to split the data to training and testing datasets 
* Method used in this case is the LogisticRegression model on the original fitted data
* Save the predictions on the testing data labels by using the testing feature data (X_test) and the fitted model
* Get accuracy score of the 2 models using balanced_accuracy_score
* confusion_matrix is used to create the confusion matrix
* classification_report is used to get details on the 2 models for accuracy, recall and precision

**Results**

Using bulleted lists, describe the accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Training Model :
    * Description of Training Model  Accuracy, Precision, and Recall scores.

Training Model (refer image- training)

 


* This model does a good job in predicting both the healthy and the high-risk loans as can be inferred from the high accuracy score of 99% . However, we have to take into consideration that the data is imbalanced as 96.77% of the target values (75036 out of 77536) are for the healthy loans.
	
* This model has a precision score of 100% (Precision = 1.00 ) for the healthy loans and 85% (Precision = 0.85 ) for the high-risk loans. This again can be attributed to the imbalance in the data. The precision scores imply that the healthy loans were classified correctly as positive 100% of the times. However, for the high-risk loans, the classification was correct only 85% of the times.
	
* This model has a recall score of 99% for the healthy loans and 90% for the high-risk loans. The scores imply that for all the instances where the loans were actually healthy, 99% of the times they were classified correctly. However, for all the instances where the loans were actually high-risk, they were classified correctly 90% of the time.









Testing Model(refer image -testing)

 
* This model also does a good job in predicting both the healthy and the high-risk loans as can be inferred from the high accuracy score of 99% . 

* This model has a precision score of 100% (Precision = 1.00 ) for the healthy loans and 87% (Precision = 0.87) for the high-risk loans. The precision scores imply that the healthy loans were classified correctly as positive 100% of the times. However, for the high-risk loans, the classification was correct only 87% of the times.

*This model has a recall score of 100% for the healthy loans and 92% for the high-risk loans. The scores imply that for all the instances where the loans were actually healthy 100 % of the time or when they were high-risk, 92% of the times they were classified correctly.

**Summary**

The testing model had 95% balanced accuracy score at predicting the healthy vs high-risk loan labels. The training model is at 94% so the model will learn and get better with more data.
The testing model has a 100% recall for healthy and 92% for high-risk loans. 

For any lending service company or credit grantor, the correct identification of a high-risk loan is much more important as it reduces the probability of defaulters by placing importance on correct analysis of their creditworthiness, thereby impacting the overall profitability of the company. The testing model does a way better job classification of the high-risk loans(92%) when they were actually positive by catching the incorrect labelling of high-risk loans as healthy.  
This method gives better accuracy and recall scores which are crucial decision metrics for a lending service company.

I would recommend this model.




