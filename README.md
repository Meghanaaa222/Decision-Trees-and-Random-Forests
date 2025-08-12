# Decision Trees and Random Forests

##  Project Overview
This project uses **Decision Trees** and **Random Forests** for a binary classification task on the **Breast Cancer Wisconsin Dataset**, which is a built-in dataset in `scikit-learn`. The goal is to demonstrate the implementation and comparison of these tree-based machine learning models, covering everything from model training to evaluation and feature importance analysis.

---

## Dataset Information
- **Source:** `scikit-learn`'s built-in dataset
- **Task:** Binary classification to predict breast cancer as either malignant or benign.

---

##  Methodology
1. **Data Loading & Preprocessing**: The project uses the `scikit-learn` Breast Cancer dataset and splits it into training and testing sets.
2. **Decision Tree Classifier**:
   - A `DecisionTreeClassifier` is trained and evaluated for accuracy.
   - The concept of **overfitting** is explored by limiting the tree's depth using `max_depth=3`, and the resulting simplified tree is visualized.
3. **Random Forest Classifier**:
   - A `RandomForestClassifier` is trained with 100 estimators.
   - Its accuracy is compared against the Decision Tree to demonstrate the benefits of an **ensemble learning** approach.
4. **Evaluation**:
   - **Feature Importance**: The most influential features are identified and visualized using a bar chart.
   - **Cross-Validation**: A 5-fold cross-validation is performed on both models to provide a more robust and reliable measure of performance.

---

##  Results

### 1. Model Accuracy Comparison
- **Random Forest Accuracy**: 0.9708
- **Decision Tree Accuracy (limited depth)**: 0.9649

The Random Forest model shows a slightly higher accuracy, highlighting its ability to improve upon a single decision tree.

### 2. Feature Importance
**Top 10 Feature Importances:**
| feature | importance |
|---|---|
| mean concave points | 0.1419 |
| worst concave points | 0.1271 |
| worst area | 0.1182 |
| mean concavity | 0.0806 |
| worst radius | 0.0780 |
| worst perimeter | 0.0743 |
| mean perimeter | 0.0601 |
| mean area | 0.0538 |
| worst concavity | 0.0411 |
| mean radius | 0.0323 |

The results show that features related to "concave points," "area," and "radius" are the most significant for this classification task.

### 3. Cross-Validation Results
- **Decision Tree Mean Accuracy**: 0.9173
- **Random Forest Mean Accuracy**: 0.9561

The cross-validation scores confirm that the **Random Forest** is more stable and has a higher average accuracy than the individual Decision Tree, reinforcing its superiority in this task.
