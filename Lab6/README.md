# Lab 6: Ecommerce Customer Analysis & Linear Regression

This repository documents the steps and results for analyzing the Ecommerce Customers dataset and building a predictive linear regression model.

---

## Lab Steps & Implementation

### 1. Load the dataset into a DataFrame
* Loaded the "Ecommerce Customers.csv" dataset into a pandas DataFrame and displayed the first 10 rows using `df.head(10)` to get an initial look at the data[cite: 2].

### 2. Explore the data (head, info, describe)
* Used `df.info()` to check the data types and confirm that there were 500 entries across 8 columns[cite: 3].
* Used `df.describe()` to review the statistical summary (mean, standard deviation, min, max, and percentiles) for all numerical columns[cite: 3].

### 3. Perform basic data cleaning if needed
* Verified the dataset's integrity by checking for missing values (`df.isna().sum()`) and duplicate rows (`df.duplicated().sum()`)[cite: 3, 4].
* Found that the dataset was perfectly clean with 0 missing values and 0 duplicates[cite: 4].

### 4. Apply feature engineering (if applicable)
* Extracted the `Email_Provider` from the email addresses and the `State` from the physical addresses to create new categorical columns[cite: 4].
* Created a new numerical feature called `App_Loyalty_Index` by multiplying 'Time on App' by 'Length of Membership'[cite: 4].

### 5. Prepare the data for modeling
* Defined the independent variables (`X`) using four numerical features: 'Avg. Session Length', 'Time on App', 'Time on Website', and 'Length of Membership'[cite: 6].
* Defined the target variable (`y`) as 'Yearly Amount Spent'[cite: 6].
* Split the dataset into training and testing sets using `train_test_split` with a 60/40 split (`test_size=0.4`)[cite: 6].

### 6. Train a model
* Imported `LinearRegression` from `sklearn.linear_model`[cite: 6].
* Instantiated the model and trained (fitted) it on the training data (`X_train`, `y_train`)[cite: 6].

### 7. Evaluate the model performance
* Extracted and interpreted the model's coefficients, revealing that 'Length of Membership' is the strongest predictor of yearly spend, while 'Time on Website' has almost zero impact[cite: 6].
* Generated predictions on the test set and visualized the results using a scatter plot (Actual vs. Predicted) and a histogram of the residuals to ensure a normal distribution of errors[cite: 7, 8].
* Calculated the final performance metrics: Mean Absolute Error (MAE) of ~7.74, Root Mean Squared Error (RMSE) of ~9.68, and an excellent R-squared score of ~0.985 (indicating the model explains 98.5% of the variance)[cite: 8].
