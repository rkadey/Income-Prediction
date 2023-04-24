# Machine Learning Project using Jupyter Notebook
This is a machine learning project implemented in Jupyter Notebook. The goal of this project is to predict whether a given adult makes more than 
$50,000 a year or not using various features such as the age, workclass of the individual, occupation, level of education etc. 

![PyPI - Python Version](https://img.shields.io/pypi/pyversions/pandas?style=for-the-badge) ![PyPI - Status](https://img.shields.io/pypi/status/pandas?style=for-the-badge) [![MIT License](https://img.shields.io/badge/License-MIT-green.svg?style=for-the-badge)](https://choosealicense.com/licenses/mit/)

## Getting Started

To get started with this project, you will need to clone this repository to your local machine. You will also need to have Jupyter Notebook installed on your machine.

## Prerequisites

- Python 3.x
- Jupyter Notebook

## Installing

To install Jupyter Notebook, run the following command in your terminal:
```bash
pip install jupyter notebook
```
## Running the Project

To run the project, navigate to the project directory in your terminal and run the following command:
```bash
jupyter notebook
```
This will launch Jupyter Notebook in your web browser. From there, you can open the project notebook and run the code.

## Data

The dataset used in this project is the US Adult dataset dataset. It contains information about the individual.

## Methodology

In this project, we will be using a classification model to predict whether a given adult makes more than 
$50,000 a year or not. The following methodological approach was followed in executing our project.

- ### Exploratory Data Analysis (EDA)
In this step, we explored the dataset to understand its characteristics, identify patterns, and gain insights. We visualized the data by plotting a pairplot to understand the distribution of the variables. Our variables were not correlated that much but it revealed that over 80+ years of individuals are working 60 hours per week. Summary tol was implored to check for missing data, shape of data, deep dive into each variable considering their frequencies and central tendencies.

From our checks above, our data consists of 32,561 rows and 15 columns. The data has no missing values but with 24 diplicated records. The mean age of participantrs is 39 with 73 distinct age values. In workclass column, 1,836 representing 5.6% have unknown values, 1,843 (5.7%) are unknown under occupation columns. 583 representing 1.8% have their native countries unknown.Our target column has two labels denoting binary classification problem.

Pairplot for our data.
![image](https://github.com/rkadey/income-prediction/blob/main/screenshots/eda.png)

- ### Data Preprocessing
In this step, we will prepare the data for modeling by handling missing values, encoding categorical variables, and scaling numerical features.As indicated above, our data has no misssing values. The standard scaler was implored to scale our numerical features to a common a scale.

- ### Feature Engineering
In this step, we will create new features from the existing data to improve the predictive power of the model. Here, we added age groups to our data.

- ### Model Selection
In this step, we will select the appropriate machine learning algorithm(s) to build the predictive model. I chose Logistic Regression for our baseline model afer which I added other four models namely; KNN, SVC, Decision Tree and GaussianNB. Upon training and scoring on evaluation data, our baseline model which is the Logistic Regression came out with the best F1 Score of 0.693804. Note that due to class imbalance in our dataset, we cannot rely on accuracy for our sole metric.

In other to see how other models performed, I tried some ensemble models like Random Forest, ExtraTrees, AdaBoost, GradientBoosting and finally the XGB classifier. After training, only two models GradientBoosting and XGB recorded an F1 score greater than our baseline model. The results are 0.705 and 0.712 respectively. Our decision here is to take the best model interms of F1 score and tune parameters to see if we can improve the score.

## Results

After several playing with our models, the result are as follows:

Our best model is the XGB with hyperparameter tuned. We achieved an F1 score of 0.7241 on our validation data. This is an improvement on the previous scores hence we go with this model. When our model was predicted on our test data ie unseen data, the performance in terms of F1 score was 0.7167.

## Conclusion
In this project, we successfully implemented a machine learning model to predict whether a given adult makes more than 
$50,000 a year or not. Our model achieved an F1 score of 71.7% on the test data, which is a good result. We also identified the most important features for predicting income, which can be useful for future analysis.

Our model and data were saved as components for the development of a web app,streamlit app, for real time prediction.
