# ClassificationExamples

A Decision Tree is a simple representation for classifying examples.
It is a Supervised Machine Learning where the data is continuously split according to a certain parameter.
To learn about it more, we have taken Social media data.

## Understanding of the data
Here we have data about Gender, Age, Salary, Purchased. Gender, Purchased being categorical variables, Age and Salary are continuous.
We need to classify if a person can purchase or not based on Gender, Age Salary
We can observe that the data is varying much on basis of age, salary.
To visualize the same we have plotted a histogram based on the age group

![AgeGroup](https://github.com/kavyapenujuru/ClassificationExamples/blob/master/AgeGroupHistogram.PNG)

## Data Preparation
Hence we use <b>Binning technique</b> to group the data based on age as ["Young", "MiddleAged", "Old"], salary as ["Low", "Medium", "High"] and make them as categorical variables from continuous.
And then, as we have Gender as Male/Femala as <b>categorical variable</b>, we use <b>Label Encode</b> to convert it to integer values as 0 and 1.
The same can be applied to Age and salary which were converted to categorical variables by using binning technique.

Our next step is to clean up all the unnessary columns, and by jest keeping integer columns we can proceed to next step.

## Data Modelling

Here we come to modeling phase. We need to differentiate train and test data.
We use <i>train_test_split</i> from <b>sklearn.model_selection</b> to do the same. I have used 30% as my test size.
We have used <i>DecisionTreeClassifier</i> from <b>sklearn.tree</b> to train our data on Decision Tree algorithm.

## Data Metrics
We have chosen Confusion matrix and Accuracy score as our measures to test our model performance.

### Confusion Matrix
A confusion matrix is a table that is often used to describe the performance of a classification model (or "classifier") on a set of test data for which the true values are known. The confusion matrix itself is relatively simple to understand, but the related terminology can be confusing. It is just a table of Actuals X Predicted score

<table><th><td>Predicted No</td><td>Predicted Yes</td></th>
<tr><td><b>Actuals No</b></td><td>62</td><td>10</td></tr>
<tr><td><b>Actuals Yes</b></td><td>11</td><td>32</td></tr></table>

Our <b>Accuracy Score</b> is <b>0.825</b>

## Decision Tree Visualization
![Decision Tree](https://github.com/kavyapenujuru/ClassificationExamples/blob/master/purchase_pred.png)
