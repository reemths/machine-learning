# Random Forest Project

Welcome to the **Random Forest Project**! This project applies Decision Tree and Random Forest algorithms to classify a dataset from LendingClub.com. The objective is to build classification models to predict whether a borrower will pay back their loan in full, evaluate their performance, and compare the effectiveness of a single tree versus an ensemble of trees.

## Steps Completed:

### 1. Data Loading and Exploration
* **Libraries:** `pandas`, `seaborn`, `matplotlib.pyplot`
* **Process:** Imported the `loan_data.csv` dataset using pandas and explored it using `.info()` and `.describe()`. Visualized feature distributions and relationships using seaborn and matplotlib (including histograms, countplots, jointplots, and lmplots) colored by outcomes like `credit.policy` and `not.fully.paid`.

### 2. Categorical Features Handling
* **Libraries:** `pandas`
* **Process:** Transformed the categorical `purpose` column into dummy variables using pandas' `pd.get_dummies(drop_first=True)` to ensure the machine learning algorithms can correctly interpret and process the data.

### 3. Train / Test Split
* **Libraries:** Scikit-Learn (`sklearn.model_selection`)
* **Process:** Divided the preprocessed data into training and testing sets using `train_test_split` (70% training data, 30% testing data).

### 4. Decision Tree Model Setup & Evaluation
* **Libraries:** Scikit-Learn (`sklearn.tree`, `sklearn.metrics`)
* **Process:** Initialized a single `DecisionTreeClassifier` and trained it on the training data using the `.fit()` method. Generated test predictions using `.predict()` and evaluated the performance using a `confusion_matrix` and a `classification_report`.

### 5. Random Forest Model Setup & Evaluation
* **Libraries:** Scikit-Learn (`sklearn.ensemble`, `sklearn.metrics`)
* **Process:** Initialized a `RandomForestClassifier` with `n_estimators=600` and trained it on the training data. Generated test predictions and evaluated the performance using a new `confusion_matrix` and `classification_report`.

### 6. Final Comparison & Results
* **Process:** Compared the evaluation metrics of both models to determine which algorithm performed better for this specific, imbalanced dataset.
* **Final Result:** The **Random Forest** achieved a higher overall accuracy (85%) compared to the **Decision Tree** (73%). However, the **Decision Tree** performed significantly better at the crucial task of identifying risky borrowers (Class 1), achieving a recall of 0.24 (107 cases correctly identified) compared to the Random Forest's poor recall of 0.02 (only 8 cases correctly identified).
