# K Nearest Neighbors Project

Welcome to the KNN Project! This project applies the K-Nearest Neighbors (KNN) algorithm to classify a dataset. The objective is to build a baseline classification model, evaluate its performance, and optimize it by finding the most suitable 'K' value using the elbow method.

## Steps Completed:

### 1. Data Loading and Exploration
* **Libraries:** `pandas`, `seaborn`
* **Process:** Imported the `KNN_Project_Data` dataset using pandas and visualized the feature distributions using a seaborn pairplot colored by the `TARGET CLASS`.

### 2. Feature Standardization
* **Libraries:** `Scikit-Learn` (`sklearn.preprocessing`)
* **Process:** Scaled the dataset features using Scikit-Learn's `StandardScaler` to ensure all numerical variables have uniform importance, preventing larger numbers from skewing the distance-based KNN algorithm.

### 3. Train / Test Split
* **Libraries:** `Scikit-Learn` (`sklearn.model_selection`)
* **Process:** Divided the standardized data into training and testing sets using `train_test_split` (70% training data, 30% testing data).

### 4. Initial Model Setup
* **Libraries:** `Scikit-Learn` (`sklearn.neighbors`)
* **Process:** Initialized a baseline KNN classifier with `KNeighborsClassifier(n_neighbors=1)` and trained it on the training data using the `.fit()` method.

### 5. Initial Evaluation
* **Libraries:** `Scikit-Learn` (`sklearn.metrics`)
* **Process:** Generated test predictions using `.predict()` and evaluated the baseline performance using a `confusion_matrix` and a `classification_report`.

### 6. Optimizing the K Value (Elbow Method)
* **Libraries:** `numpy`, `matplotlib.pyplot`
* **Process:** Created a `for` loop to test K values ranging from 1 to 40, calculating the error rate (`np.mean()`) for each model. Plotted an "Error Rate vs. K Value" graph using `matplotlib` to visually identify the optimal K value (the lowest error point).

### 7. Final Retraining & Results
* **Process:** Retrained the final model using the optimal value, $K=23$. Generated a new classification report and confusion matrix to evaluate the final performance.
* **Final Result:** Tuning the K value successfully increased the model's overall accuracy from 71% (at $K=1$) to 82% (at $K=23$), significantly improving precision, recall, and f1-score across both classes.
