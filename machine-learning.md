# Machine Learning

### Python

+ Set up environment<br>

Download and Install Anaconda <br>https://www.anaconda.com/

+ Clone this repository and open `Python Crash Course Exercises.ipynb` in Jupyter Notebook

Now let's learn some libraries for working with data in python

Let's start working on Numpy library

+ Read Numpy Docs https://numpy.org/doc/stable/user/absolute_beginners.html

+ Now open `Numpy Exercises.ipynb` file in jupyter notebook and solve the given exercise

Let's start working with pandas library

Pandas is a Python library used for working with data sets. It has functions for analyzing, cleaning, exploring, and manipulating data.

+ Read Docs: https://www.w3schools.com/python/pandas/default.asp

+ Now open `Pandas Exercise.ipynb` file in jupyter notebook and solve the given exercise


Machine learning

Exercise 1: Solution

Import Libraries numpy and pandas
`import pandas as pd`
`import numpy as np`

Read and Check out the Data using pandas
`USAhousing = pd.read_csv('USA_Housing.csv')`
`USAhousing.head()`
`USAhousing.describe()`
`USAhousing.info()`
`USAhousing.columns`

Training a Linear Regression Model
X and y arrays
`X = USAhousing[['Avg. Area Income', 'Avg. Area House Age', 'Avg. Area Number of Rooms',
               'Avg. Area Number of Bedrooms', 'Area Population']]`
`y = USAhousing['Price']`

Train Test Split
`from sklearn.model_selection import train_test_split`
`X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.4, random_state=101)`

Creating and Training the Model
`from sklearn.linear_model import LinearRegression`
`lm = LinearRegression()`
`lm.fit(X_train,y_train)`

Model Evaluation
`print(lm.intercept_)`
`coeff_df = pd.DataFrame(lm.coef_,X.columns,columns=['Coefficient'])`
`coeff_df`


