# EDA-With-Logistic-Regression-of-Titanic-Dataset

This repository contains a Jupyter notebook that performs Exploratory Data Analysis (EDA) and applies Logistic Regression on the Titanic dataset. The analysis includes data visualization, statistical calculations, and machine learning model implementation.

Table of Contents
Introduction
Dataset
Exploratory Data Analysis (EDA)
Scatter Plot of Sepal Dimensions
Statistical Summary of Sepal Length
Histogram of Sepal Length
Box Plot of Petal Width
Logistic Regression
Results
Conclusion
Introduction
This project aims to explore the Titanic dataset from Kaggle and apply Logistic Regression to predict the survival of passengers. The notebook contains various steps to preprocess the data, visualize relationships, and build a predictive model.

Dataset
The dataset used for this analysis is the Titanic dataset, which contains information about the passengers, including whether they survived the sinking of the Titanic.

Exploratory Data Analysis (EDA)
The EDA section includes several visualizations and statistical summaries to understand the dataset better.

Scatter Plot of Sepal Dimensions
Using Pandas and Seaborn, a scatter plot is created to visualize the relationship between sepal length and sepal width, color-coded by species.

Python
import seaborn as sns
sns.scatterplot(x='sepal_length', y='sepal_width', hue='species', data=df)
Statistical Summary of Sepal Length
Using Pandas, the mean, median, and standard deviation of sepal length for each species are calculated.

Python
df['sepal_length'].groupby(df['species']).agg(['mean', 'median', 'std'])
Histogram of Sepal Length
Using NumPy and Matplotlib, a histogram of sepal length for all species combined is created.

Python
import matplotlib.pyplot as plt
plt.hist(df['sepal_length'])
Box Plot of Petal Width
Using Seaborn, a box plot is created to compare the distribution of petal width across different species.

Python
sns.boxplot(x='species', y='petal_width', data=df)
Logistic Regression
The logistic regression model is implemented to predict whether a passenger survived or not based on the features in the Titanic dataset.

Data Loading and Preprocessing
The Titanic dataset is loaded and necessary preprocessing steps are performed.

Python
import pandas as pd
train = pd.read_csv('titanic_train.csv')
train.head()
Results
The results of the logistic regression model are evaluated to understand its performance in predicting the survival of passengers.

Conclusion
The notebook demonstrates the process of EDA and logistic regression implementation on the Titanic dataset. The visualizations and statistical summaries provide insights into the data, and the logistic regression model offers a predictive solution for the classification problem.
