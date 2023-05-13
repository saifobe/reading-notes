# Linear Regression in Python
## What is Linear Regression?
Linear regression is a statistical method that allows us to summarize and study relationships between two continuous (quantitative) variables:
* One variable, denoted x, is regarded as the predictor, explanatory, or independent variable.
* The other variable, denoted y, is regarded as the response, outcome, or dependent variable.


Because the other terms are used less frequently today, we'll use the "predictor" and "response" terms to refer to the variables encountered in this course. The other terms are mentioned only to make you aware of them should you encounter them.

We're interested in predicting the response variable based on the predictor variable. In other words, we're interested in using the predictor variable to explain variability in the response variable.

## Simple Linear Regression

Simple linear regression is a statistical method that allows us to summarize and study relationships between two continuous (quantitative) variables:

* One variable, denoted x, is regarded as the predictor, explanatory, or independent variable.
* The other variable, denoted y, is regarded as the response, outcome, or dependent variable.

Because the other terms are used less frequently today, we'll use the "predictor" and "response" terms to refer to the variables encountered in this course. The other terms are mentioned only to make you aware of them should you encounter them.

We're interested in predicting the response variable based on the predictor variable. In other words, we're interested in using the predictor variable to explain variability in the response variable.

## Linear Regression in Python
### Importing Libraries
```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
%matplotlib inline
```
### Reading the Data
```python
USAhousing = pd.read_csv('USA_Housing.csv')
```
### Exploring the Data
```python
USAhousing.head()
USAhousing.info()
USAhousing.describe()
USAhousing.columns
```
### Visualizing the Data
```python
sns.pairplot(USAhousing)
sns.distplot(USAhousing['Price'])
sns.heatmap(USAhousing.corr())
```
### Training a Linear Regression Model
```python
X = USAhousing[['Avg. Area Income', 'Avg. Area House Age', 'Avg. Area Number of Rooms',
       'Avg. Area Number of Bedrooms', 'Area Population']]
y = USAhousing['Price']
```
### Train Test Split
```python
from sklearn.model_selection import train_test_split
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.4, random_state=101)
```
### Creating and Training the Model
```python
from sklearn.linear_model import LinearRegression
lm = LinearRegression()
lm.fit(X_train,y_train)
```
### Model Evaluation
```python
# print the intercept
print(lm.intercept_)
coeff_df = pd.DataFrame(lm.coef_,X.columns,columns=['Coefficient'])
coeff_df
```
### Predictions from our Model
```python
predictions = lm.predict(X_test)
plt.scatter(y_test,predictions)
sns.distplot((y_test-predictions),bins=50);
```
