# **BankLoan_Approval_Prediction**
## **`Goal`**
The aim of this project is to predict the likelihood of a liability customer buying personal loans. The classification tool- Logistic Regression is used to fit to the BankLoan dataset obtained from Kaggle.
## **`Business Problem`**
This case is about a bank (Thera Bank) whose management wants to explore ways of converting its liability customers to personal loan customers (while retaining them as depositors). A campaign that the bank ran last year for liability customers showed a healthy conversion rate of over 9% success.This has encouraged the retail marketing department to devise campaigns with better target marketing to increase the success ratio with minimal budget.
## **`Data`**
File contains 14 columns and 5000 rows. Description of the columns are as follows:
- ID: Customer ID
- Age : Customer Age
- Experience : Customer Experience in years
- Income : Annual Income of the Customer(in thousands)
- ZipCode: Customer's residence zipcode
- Family : No of Family members of the customer
- CCAvg: Credit Card Average Score
- Education: Education of the customer(1: Bachelor, 2: Master, 3: Advanced Degree)
- Mortgage: Mortgage taken or not taken by the customer(in thousands)
- Personal Loan: 0 = No personal loan given , 1 = personal loan given
- Securities Account : Having or not having a Securities Account
- CD Account : Having or not having a CD Account
- Online : Having or not having online banking
- Credit Card : Having or not having a credit card
## **`Tools Used`**
1. Pandas
2. Matplotlib
3. Seaborn
4. Scikit-learn
## **`What we will do:`**
1. Reading the data
2. Data Cleaning
   - Dealing with duplicates
   - Dealing with irrelevant columns   
4. Exploring columns
5. Data Visualization
6. Data Preparation
   - Splitting the data into train and test data
   - Rescaling the data 
7. Exploratory Data Analysis
8. Model building using LogisticRegression
9. Model Evaluation
## **`Terminologies`** 
1. A **`heatmap`** depicts values for a main variable of interest across two axis variables as a grid of colored squares. The axis variables are divided into ranges like a bar chart or histogram, and each cell’s color indicates the value of the main variable in the corresponding cell range. They are used to show relationships between two variables, one plotted on each axis. By observing how cell colors change across each axis, we can observe if there are any patterns in value for one or both variables.
2. **`StandardScaler`** removes the mean and scales each feature/variable to unit variance. This operation is performed feature-wise in an independent way. StandardScaler can be influenced by outliers (if they exist in the dataset) since it involves the estimation of the empirical mean and standard deviation of each feature. In Machine Learning, StandardScaler is used to resize the distribution of values so that the mean of the observed values is 0 and the standard deviation is 1.
3. **`Logistic regression`** is a supervised machine learning algorithm used for classification tasks where the goal is to predict the probability that an instance belongs to a given class or not. It uses the Logistic curve given by -\
$\sigma$ (x)=$`\frac{1}{1+e^x}`$.
4. **`Confusion Matrix`** is a matrix that summarizes the performance of a machine learning model on a set of test data. It is a means of displaying the number of accurate and inaccurate instances based on the model’s predictions. It is often used to measure the performance of classification models, which aim to predict a categorical label for each input instance. The matrix displays the number of instances produced by the model on the test data.
   - True positives (TP): occur when the model accurately predicts a positive data point.
   - True negatives (TN): occur when the model accurately predicts a negative data point.
   - False positives (FP): occur when the model predicts a positive data point incorrectly.
   - False negatives (FN): occur when the model mispredicts a negative data point.\
5. **`Accuracy`** - The base metric used for model evaluation is often Accuracy, describing the number of correct predictions over all predictions: </br> Accuracy =  $`\frac{TP+TN}{TP+TN+FP+FN}`$.
6. **`Precision`** is a measure of how many of the positive predictions made are correct (TP). </br> Precision = $`\frac{TP}{TP+FP}`$.
7. **`Recall`** is a measure of how many of the positive cases the classifier correctly predicted, over all the positive cases in the data. It is sometimes also referred to as Sensitivity. </br> Recall = $`\frac{TP}{TP+FN}`$
8. **`F1 Score`** is the weighted harmonic mean of precision and recall. The closer to 1, the better the model.</br> F1 score = $`\frac{Precision*Recall}{Precision+Recall}`$
9. **`AUC-ROC CURVE`** - In order to check the performance of a binary classification algorithm, we use the AUC (Area Under The Curve) - ROC (Receiver Operating Characteristics) curve. </br>
AUC-ROC curve is a performance measurement for the classification problems at various threshold settings. ROC is a probability curve and AUC represents the degree or measure of separability. It tells how much the model is capable of distinguishing between classes. Higher the AUC, the better the model is at predicting 0 classes as 0 and 1 classes as 1. The ROC curve is plotted with TPR against the FPR where TPR is on the y-axis and FPR is on the x-axis. An excellent model has AUC near to the 1 which means it has a good measure of separability.
10. **`Precision vs Recall Curve`** - The precision-recall curve shows the tradeoff between precision and recall for different threshold. A high area under the curve represents both high recall and high precision, where high precision relates to a low false positive rate, and high recall relates to a low false negative rate. A typical good model should have a high 
