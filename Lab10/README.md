# Lab10

## What I Did in This Lab (My Steps):
1. **Loading Data:** I loaded the famous Iris dataset using Seaborn (`sns.load_dataset('iris')`).
2. **Exploratory Data Analysis (EDA):** I explored the data and created a pairplot and a KDE plot to visualize feature relationships and species separability.
3. **Data Splitting:** I separated the features and target species, then split the data into training and testing sets using `train_test_split`.
4. **Model Training:** I initialized a Support Vector Classifier (`SVC`) model and fitted it to the training data.
5. **Model Evaluation:** I generated predictions on the test set and evaluated the model using a Confusion Matrix and a Classification Report, achieving an accuracy of 98%.
6. **GridSearch Practice:** I set up a `param_grid` for `C` and `gamma` parameters and created a `GridSearchCV` object to tune the model.
7. **GridSearch Evaluation & Conclusion:** Finally, I made predictions using the grid model and evaluated it with a confusion matrix and classification report. **Were you able to improve?** No, the accuracy stayed at 98% because the Iris dataset is simple and the default SVC model already performed very well.
