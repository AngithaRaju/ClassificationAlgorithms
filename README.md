**Objective**

The objective is to train and compare five supervised classification algorithms on the Breast Cancer Wisconsin dataset available in Scikit-learn. The models predict whether a tumor is malignant or benign from numerical measurements of cell nuclei.

**Dataset and preprocessing**
The dataset contains 569 samples, 30 numerical features, and two target classes.
Preprocessing steps:
- Missing values: Check for missing values.
- Feature scaling: StandardScaler standardizes features. This is important for Logistic Regression, SVM, and k-NN because they are sensitive to feature magnitudes. Tree-based models do not generally require scaling, but using the same preprocessing approach makes the workflow easier to compare.
- Train-test split: Use an 80:20 split and stratify by target to preserve the class proportions.

**Classification algorithms**
1. Logistic Regression: Estimates class probabilities using a logistic function. It is a useful baseline for binary classification and works well when class separation can be represented reasonably by a linear boundary.
2. Decision Tree: Learns a sequence of feature-based rules. It is interpretable and can model nonlinear relationships, though a deep tree can overfit.
3. Random Forest: Combines predictions from many decision trees trained on bootstrapped samples and feature subsets. This often improves robustness and reduces overfitting compared with a single tree.
4. Support Vector Machine (SVM): Finds a decision boundary that maximizes the margin between classes. An RBF kernel can model nonlinear boundaries; scaling is important.
5. k-Nearest Neighbors (k-NN): Predicts a class based on the labels of nearby training samples. It can capture local patterns, but distance calculations are sensitive to feature scales.

**Evaluation**
The models are compared using accuracy, precision, recall, F1-score, and ROC-AUC. 
