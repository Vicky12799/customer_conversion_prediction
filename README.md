# Report on Customer Conversion Prediction
## Introduction
The aim of this report is to analyze a dataset containing customer information and their conversion status. The dataset has been imported using pandas library, and various data analysis and visualization techniques have been used to extract insights and implement a machine learning model.

## Importing Required Libraries
The following libraries were imported at the beginning of the code:

* pandas: used for data manipulation and analysis     
* numpy: used for numerical operations        
* seaborn and matplotlib: used for data visualization     
* scipy: used for statistical operations      
## Data Cleaning and Preprocessing
The dataset contains columns such as age, job, marital status, education qualification, call type, duration, number of calls, previous outcome, and subscription status. The following steps were taken to clean and preprocess the data:

1. The dataset contains duplicate rows, which were removed using the 'drop_duplicates' function.
2. The column names were changed to more descriptive names using the 'rename' function.
3. Outliers in the 'duration' and 'num_calls' columns were removed using the 'remove_duration_outliers' and 'remove_num_calls_outliers' functions.
4. Categorical variables were encoded using the 'LabelEncoder' function from the 'sklearn' library.
## Data Analysis and Visualization
### Univariate Continuous Variables Analysis
The 'univ_cont' function was created to perform analysis on continuous variables. It displays a summary of the descriptive statistics, a histogram, a boxplot, and a chi-square test for normality.

The 'duration' column has a mean of 230 seconds and a standard deviation of 126 seconds, and its distribution is right-skewed. The chi-square test shows that it is not normally distributed. Outliers above the 97th percentile were removed.

### Categorical Variables Analysis
The 'countplot' function was used to create plots of categorical variables with respect to the 'subscribed' column.

## Machine Learning Model
A machine learning model was implemented to predict customer conversion. The dataset was split into training and testing sets using the 'train_test_split' function. Four models were tested - KNN, Decision Tree, Random Forest Classifier and Logistic Regression - with Random Forest Classifier and Logistic Regression achieved the highest accuracy. 

The results of the model testing are as follows:

* KNeighborsClassifier:     
    - Accuracy: 88.05%    
    - Log Loss: 1.09


* DecisionTreeClassifier:   
    -  Accuracy: 85.28%    
    - Log Loss: 5.31

* RandomForestClassifier:
    - Accuracy: 89.14%
    - Log Loss: 0.36

* LogisticRegression:
    - Accuracy: 88.90%
    - Log Loss: 0.28

Based on the results, the best performing model was RandomForestClassifier with an accuracy of 89.14% and a log loss of 0.36. LogisticRegression was a close second with an accuracy of 88.90% and a log loss of 0.28. KNeighborsClassifier also had a decent performance with an accuracy of 88.05%, while DecisionTreeClassifier had the lowest accuracy of 85.28%.

## Conclusion
The analysis showed that the 'duration', 'num_calls', 'job', and 'call_type' columns were the most significant predictors of customer conversion. The machine learning model achieved a high accuracy, indicating that it can be used to predict customer conversion in future campaigns.
