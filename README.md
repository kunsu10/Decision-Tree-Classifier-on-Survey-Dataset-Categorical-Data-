# Decision-Tree-Classifier-on-Survey-Dataset-Categorical-Data-

## Project Overview - 
This project builds a Decision Tree Classifier using a survey dataset with only categorical features. Unlike usual workflows that convert categories into numbers, it shows how to work directly with categorical columns in scikit-learn’s DecisionTreeClassifier for classification tasks.


**Why this dataset:** 

* Real-world categorical survey data, ideal for classification tasks.

* Helps understand how decision trees work with non-numeric data.

* Great for practicing preprocessing, splitting, model building, and tuning.

### 1) Data Understanding (Exploratory Data Analysis)

Why we did this step:
* Before training any model, it’s essential to understand the dataset structure, identify the target variable, inspect missing values, and analyze the distribution of categorical features.

What we did:

* Loaded the dataset and inspected its shape and columns.

* Identified categorical columns and checked for unique values in each.

* Looked for missing or inconsistent entries in the survey responses.

* Explored relationships between features and the target variable using frequency counts and groupby operations.

Key findings:

* All columns were categorical (e.g., occupation, education, satisfaction level).

* Some columns had missing or “unknown” values that required cleaning.

* The target column was identified based on the classification goal (e.g., predicting satisfaction category).

### 2) Data Preprocessing

Why we did this step:
* Models require clean and consistent data. Even when working with categorical data, we must handle missing values, select relevant columns, and split the data properly for evaluation.

What we did:

* Filled or dropped missing values depending on the column’s importance.

* Ensured no numerical conversion (no label encoding or one-hot encoding).

* Split the data into training and testing sets (80/20) to evaluate model performance on unseen data.

Impact:

* Ensured the dataset was clean and ready for modeling.

* Prevented data leakage by splitting before model training.

### 3) Baseline Model: Decision Tree Classifier

Why we did this step:
* A Decision Tree is easy to interpret and works well on categorical data for classification problems. It’s a good starting point to understand model behavior before hyperparameter tuning.

What we did:

* Trained a DecisionTreeClassifier using criterion='entropy' to measure information gain.

* Used max_depth to prevent overfitting.

* Fitted the model on the training data and evaluated it on the test data.

Key insights:

* The model provided an initial baseline accuracy.

* By examining the tree structure, we could see how different categorical responses led to specific classifications.

### 4) Model Evaluation & Interpretation

Why we did this step:
* Evaluating model performance helps understand where the model performs well and where it fails. Interpretation is essential for survey data to explain outcomes clearly.

What we did:

* Calculated accuracy, precision, recall, and F1-score using a classification report.

* Generated a confusion matrix to visualize correct vs. incorrect predictions.

* Interpreted the top decision rules from the tree to see which categorical features were most influential.

Impact:

* Identified key survey features that most affected the target classification.

* Gained transparent, human-readable insights from the tree structure.

### 5) Hyperparameter Tuning

Why we did this step:
* Tuning hyperparameters helps improve model generalization and avoid overfitting, especially in decision trees which can grow very deep.

What we did:

* Used GridSearchCV to tune parameters such as max_depth, min_samples_split, and criterion.

* Evaluated the model using cross-validation to pick the best parameter set.

Result:

* The tuned model achieved better performance than the baseline.

* Reduced overfitting while improving test accuracy and stability.

### 6) Insights & Conclusion

* Decision trees can work effectively with purely categorical data without numeric transformations.

* Survey features like occupation, satisfaction, or demographic information played a major role in classification.

* Hyperparameter tuning improved the model’s performance, making it suitable for real-world categorical prediction tasks.

* This project demonstrates a clean, simple, and interpretable pipeline for categorical classification using Decision Trees.
