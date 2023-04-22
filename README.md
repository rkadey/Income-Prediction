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

From our checks above, our data consists of 32,561 rows and 15 columns. The data has no missing values but with 24 diplicated records. The mean age of participantrs is 39 with 73 distinct age values. In workclass column, 1,836 representing 5.6% have unknown values, 1,843 (5.7%) are unknown under occupation columns. 583 representing 1.8% have their native countries unknown.Our target column has two labels denoting binary classification problem

- ### Data Preprocessing
In this step, we will prepare the data for modeling by handling missing values, encoding categorical variables, and scaling numerical features.As indicated above, our data has no misssing values. The standard scaler was implored to scale our numerical features to a common a scale.

- ### Feature Engineering
In this step, we will create new features from the existing data to improve the predictive power of the model. Here, we added age groups to our data.

- ### Model Selection
In this step, we will select the appropriate machine learning algorithm(s) to build the predictive model. 

## Results

The results of our analysis are as follows:

Our model achieved an accuracy of 85% on the test data.
The most important features for predicting house prices were the size of the house and the number of rooms.
## Conclusion
In this project, we successfully implemented a machine learning model to predict the price of houses in a particular city. Our model achieved an accuracy of 85% on the test data, which is a good result. We also identified the most important features for predicting house prices, which can be useful for future analysis.
