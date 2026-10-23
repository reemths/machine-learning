# Lab 7: Logistic Regression Assignment

## Assignment Overview
In this lab, I worked with a fake advertising dataset to build a Machine Learning model. The goal of this project was to predict whether an internet user will click on an advertisement based on their features.

## What I Did in This Lab (My Steps):
1. **Loading Data:** I imported the necessary libraries and loaded the `advertising.csv` dataset.
2. **Exploratory Data Analysis (EDA):** I used Seaborn to explore the data and recreated the required plots (Histograms, Jointplots, and Pairplot) to understand the relationships between the features.
3. **Missing Data Check:** I created a heatmap to check for missing values, and the data was clean.
4. **Data Splitting:** I chose the numerical columns as features and split the data into a training set and a testing set using `train_test_split` (with a test size of 33%).
5. **Model Training:** I initialized and trained a `LogisticRegression` model on the training set. 
6. **Model Evaluation:** Finally, I predicted the values for the test data and evaluated my model using a classification report. The model achieved a great accuracy of 97%.

## Libraries I Used:
* Pandas & NumPy (for data handling)
* Matplotlib & Seaborn (for data visualization)
* Scikit-Learn (for the machine learning model and evaluation)
