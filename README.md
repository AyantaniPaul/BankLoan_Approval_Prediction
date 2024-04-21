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
3. **`Logistic regression`** is a supervised machine learning algorithm used for classification tasks where the goal is to predict the probability that an instance belongs to a given class or not. 
