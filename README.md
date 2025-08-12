# Decision-Trees-and-Random-Forests
This repository contains a Jupyter Notebook (decision_trees_and_random_forests.ipynb) that demonstrates the implementation and comparison of two fundamental tree-based machine learning models: Decision Trees and Random Forests.

The analysis uses scikit-learn's built-in Breast Cancer dataset to perform a binary classification task.

Objective
The main goals of this project are:

To train and evaluate a Decision Tree Classifier.

To understand and mitigate the problem of overfitting in a single Decision Tree.

To train and evaluate a Random Forest Classifier, an ensemble learning method, and compare its performance to a Decision Tree.

To visualize the decision-making process of a tree and interpret feature importance scores from the Random Forest model.

Analysis and Results
The notebook walks through the following steps, with code and explanations for each.

1. Decision Tree Analysis
A basic DecisionTreeClassifier was trained and evaluated. The output shows its initial accuracy.

The notebook then visualizes a limited-depth tree, demonstrating how the max_depth parameter can be used to control complexity and prevent overfitting.

Decision Tree (max_depth=3) Accuracy: 0.9649

2. Random Forest Analysis
A RandomForestClassifier was trained using 100 estimators. This model's accuracy was then compared against the Decision Tree.

Random Forest Accuracy: 0.9708

Decision Tree Accuracy: 0.9649

As expected, the Random Forest model achieved a slightly higher accuracy, which highlights the power of ensemble methods in improving model performance and robustness.

3. Feature Importance
The feature importances were extracted from the trained Random Forest model to understand which features were most influential in the classification task.

Top 10 Feature Importances:
                 Feature  importance
7    mean concave points    0.1419
27  worst concave points    0.1271
23            worst area    0.1182
6         mean concavity    0.0806
20          worst radius    0.0780
22       worst perimeter    0.0743
2         mean perimeter    0.0601
3              mean area    0.0538
26       worst concavity    0.0411
0            mean radius    0.0323
The visualization confirms that features related to "mean concave points" and "worst concave points" are the most significant for this specific classification problem.

4. Cross-Validation
To get a more reliable estimate of model performance, a 5-fold cross-validation was performed on both models.

Decision Tree Mean Accuracy: 0.9173

Random Forest Mean Accuracy: 0.9561

The cross-validation scores show that while the Random Forest consistently performs well across different subsets of the data, the single Decision Tree has a wider range of performance, demonstrating its instability and susceptibility to the specific data split. This reinforces why Random Forests are often preferred.
