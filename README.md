# DECISION-TREE-IMPLEMENTATION

"COMPANY": CODTECH IT SOLLUTIONS

"NAME": T.SRIYANSH

"INTERN ID":CT04DM652

"DOMAIN": MACHINE LEARNING

"DURATION": 4 WEEKS

"MENTOR": NEELA SANTHOSH



 DESCRIPTION

-> Decision Tree Analysis for Predicting Student Academic Performance
Introduction
The task involved building and visualizing a decision tree model to predict student academic performance (final grade, G3) based on various demographic, social, and academic factors. The dataset contained information about students' personal backgrounds, family situations, school-related activities, and past academic records. The goal was to identify key factors influencing student success and create an interpretable machine learning model that could help educators and policymakers make data-driven decisions.

->Data Preparation and Preprocessing
The dataset included both numerical and categorical variables, such as:

Demographics: Age, sex, address (urban/rural)

Family background: Parental education, job types, family size, family relationship quality

School-related factors: School support, extra paid classes, study time, absences

Past academic performance: Grades from the first (G1) and second (G2) periods

Since G3 (final grade) was a numerical variable (ranging from 0 to 20), this was treated as a regression problem. Before modeling, the data underwent preprocessing:

Handling Categorical Variables: Features like school, sex, Mjob, and internet were encoded into numerical values using Label Encoding.

Feature Selection: Intermediate grades (G1, G2) were excluded to avoid data leakage and ensure the model predicted G3 based on non-grade factors.

Train-Test Split: The data was divided into 80% training and 20% testing sets to evaluate model performance fairly.

->Decision Tree Model Development
A Decision Tree Regressor was chosen for its interpretability and ability to capture non-linear relationships. Key hyperparameters included:

max_depth=5 (to prevent overfitting)

min_samples_split=20 (minimum samples required to split a node)

min_samples_leaf=10 (minimum samples required in a leaf node)

The model was trained on the training set and evaluated using:

Mean Squared Error (MSE)

Root Mean Squared Error (RMSE)

R-squared (R²)

->Model Evaluation & Insights
1. Performance Metrics
MSE & RMSE: Measured prediction errors (lower values indicate better accuracy).

R² Score: Indicated how well the model explained grade variations (0 to 1, where 1 is perfect prediction).

2. Key Findings from the Decision Tree
The visualized tree (limited to depth=3 for readability) revealed:

Most Important Splits: Factors like study time, absences, and family support appeared early in the tree, indicating their strong influence on grades.

Interaction Effects: For example, students with high study time and low absences tended to have higher predicted grades.

3. Feature Importance Analysis
A bar chart ranked the top 15 influential features, likely including:

Study time (directly impacts learning)

Absences (missing classes reduces performance)

Family support (encouragement improves outcomes)

Parental education level (higher education correlates with better support)

Internet access (facilitates learning resources)

->Limitations & Future Improvements
Overfitting Risk: Despite depth control, decision trees can still overfit. Future work could use Random Forests or Gradient Boosting for better generalization.

Feature Engineering: Creating composite features (e.g., "study efficiency = study time / absences") might improve predictions.

Alternative Approaches: Converting G3 into pass/fail (classification) could simplify interpretation for some applications.

->Conclusion
This project successfully built a decision tree model to predict student performance, identifying critical factors affecting grades. The model provides actionable insights for educators while maintaining interpretability. Future enhancements could involve more advanced algorithms and additional student behavioral data for even better predictions.
