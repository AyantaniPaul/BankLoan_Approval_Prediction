# **BankLoan_Approval_Prediction**
## **`Goal`**
The aim of this project is to predict the likelihood of a customer getting approved for a bank loan. Several classification tools like Logistic Regression, K-Nearest Neighbors Algorithm, Decision Tree Classifier and Random Forrest Classifier are used to fit to the BankLoan dataset which obtained from Kaggle. Then we compare the models and find out which model fits the data in the best way.
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
1. Numpy
2. Pandas
3. Matplotlib
4. Seaborn
5. Scikit-learn
## **`What we will do:`**
1. Reading the data
2. Data Cleaning
   - Dealing with duplicates
   - Dealing with irrelevant columns
   - Dealing with outliers  
4. Exploratory Data Analysis
5. Data Preparation
   - Splitting the data into train and test data
   - Rescaling the data
   - Balancing the data
6. Model building
7. Model Evaluation and Comparison  
## **`How each model works? `** 
We used four classification model namely - Logistic Regression, K-nearest Neighbors (KNN) Classifier, Decision Tree Classifier and Random Forest Classifier. We used the **Scikit-learn** library for the model building but here is a short explanation of how each model works. 
Say we have a datset with n features given by $X_{1}, X_{2}, \dots, X_{n}$ and the target variable is Y. Since we are concerned with a classification problem. So our main aim is to find the probability P[Y=1| $X_{1}, X_{2}, \dots, X_{n}$]. If we consider the threshold probablity of 0.5, then any target variable having P[Y=1| $X_{1}, X_{2}, \dots, X_{n}$] > 0.5, we classify it as class 1, otherwise we classify it as 0.
1. **`Logistic Regression`**
   We know when we have a set of n independent variables $X_{1}, X_{2}, \dots, X_{n}$ and a single dependent variable, say Y, then we use a linear regression for prediction of the target variable. However when we are concerned about only two values of Y (say 1 or 0), we use a logistic regression model. The LR model takes a linear regression equation and passes it to a sigmoid function which is given by, </br> </t> $\sigma$(x)=$`\frac{1}{1+e^x}`$. </br> The sigmoid function is s-shaped and the range of $\sigma$(x) is between 0 and 1. For a given value of $X_{1}, X_{2}, \dots, X_{n}$, $\sigma$($\tilde{x}$) yields the estimated value of P[Y=1| $X_{1}, X_{2}, \dots, X_{n}$] or $\hat{y}$.
2. **`K-Nearest Neighbors (KNN) Classifier`**
   The k-nearest neighbors (KNN) classification algorithm is a non-parametric, supervised learning classifier, which uses proximity to make classifications about the grouping of an individual data point. If we plot these points on a graph, we may be able to locate some clusters or groups. Now, given an unclassified point, we can assign it to a group by observing what group its nearest neighbors belong to. The steps involved are
   - We choose the optimum value of K by using gridsearchcv. K represents the number of nearest neighbors that needs to be considered while making prediction.
   - To measure the similarity between target and training data points, Euclidean distance is used. Distance is calculated between each of the data points in the dataset and target point.
   - The k data points with the smallest distances to the target point are the nearest neighbors.
   -  The class labels of are determined by performing majority voting. The class with the most occurrences among the neighbors becomes the predicted class for the target data point.
3. **`Decision Tree Classifier`**
   A decision tree is a flowchart-like tree structure where an internal node represents a feature(or attribute), the branch represents a decision rule, and each leaf node represents the outcome.
4. **`Random Forest Classifier`**
## **`How the models are evaluated and compared? `**
**`Confusion Matrix`** is a matrix that summarizes the performance of a machine learning model on a set of test data. It is a means of displaying the number of accurate and inaccurate instances based on the model’s predictions. It is often used to measure the performance of classification models, which aim to predict a categorical label for each input instance. The matrix displays the number of instances produced by the model on the test data.
   - True positives (TP): occur when the model accurately predicts a positive data point.
   - True negatives (TN): occur when the model accurately predicts a negative data point.
   - False positives (FP): occur when the model predicts a positive data point incorrectly.
   - False negatives (FN): occur when the model mispredicts a negative data point. </br>
   ![1_Z54JgbS4DUwWSknhDCvNTQ](https://github.com/AyantaniPaul/BankLoan_Approval_Prediction/assets/150261131/054bbb8b-eeb3-4abb-8dde-5883fc373c5c)

7. **`Accuracy`** - The base metric used for model evaluation is often Accuracy, describing the number of correct predictions over all predictions: </br> Accuracy =  $`\frac{TP+TN}{TP+TN+FP+FN}`$.
8. **`Precision`** is a measure of how many of the positive predictions made are correct (TP). </br> Precision = $`\frac{TP}{TP+FP}`$.
9. **`Recall`** is a measure of how many of the positive cases the classifier correctly predicted, over all the positive cases in the data. It is sometimes also referred to as Sensitivity. </br> Recall = $`\frac{TP}{TP+FN}`$
10. **`F1 Score`** is the weighted harmonic mean of precision and recall. The closer to 1, the better the model.</br> F1 score = $`\frac{Precision*Recall}{Precision+Recall}`$
11. **`AUC-ROC CURVE`** - In order to check the performance of a binary classification algorithm, we use the AUC (Area Under The Curve) - ROC (Receiver Operating Characteristics) curve. </br>
AUC-ROC curve is a performance measurement for the classification problems at various threshold settings. ROC is a probability curve and AUC represents the degree or measure of separability. It tells how much the model is capable of distinguishing between classes. Higher the AUC, the better the model is at predicting 0 classes as 0 and 1 classes as 1. The ROC curve is plotted with TPR against the FPR where TPR is on the y-axis and FPR is on the x-axis. An excellent model has AUC near to the 1 which means it has a good measure of separability. A comparison of models using ROC-AUC curve is shown below- </br>
![image](https://github.com/AyantaniPaul/BankLoan_Approval_Prediction/assets/150261131/e4f4ae78-ae59-44f4-86c9-f747160b4611)

13. **`Precision vs Recall Curve`** - The precision-recall curve shows the tradeoff between precision and recall for different threshold. A high area under the curve represents both high recall and high precision, where high precision relates to a low false positive rate, and high recall relates to a low false negative rate. A typical good model should have a high. A comparison of models using Precision vs Recall Curve is shown below- </br>
![image](https://github.com/AyantaniPaul/BankLoan_Approval_Prediction/assets/150261131/81f6fa2f-63f9-48e4-966d-b9e12c25f3eb)
