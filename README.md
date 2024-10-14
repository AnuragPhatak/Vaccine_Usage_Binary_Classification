## H1N1 Flu Vaccine Prediction using Logistic Regression 🧪💉

### Problem Statement
📊 The objective of this project is to predict whether individuals will take the H1N1 flu vaccine or not, using various personal and demographic features. The problem is solved using Logistic Regression.

### Data Preprocessing and Cleaning 🧹
- **Categorical Data Cleaning:** Simplified categories for columns like 'age_bracket' and 'qualification'.
- **Exploratory Data Analysis (EDA):** 📈 Visualizations were created to understand the distribution of categorical features and their relationship with the target variable (h1n1_vaccine).
- **Missing Values Handling:** 🛠 Filled missing values using the mode of each column. Dropped the `has_health_insur` column as it was irrelevant.

### Encoding:
- **Ordinal Encoding:** Columns like 'age_bracket', 'qualification', and 'income_level'.
- **One-Hot Encoding:** Categorical columns like 'race', 'sex', 'employment', etc.
- **Scaling:** ⚖️ Used StandardScaler to normalize features, excluding boolean and target columns.

### Feature Importance 🌟
- Used **RandomForestClassifier** to determine the most important features. The top 34 features were selected for training the logistic regression model.

### Model Building and Tuning 🏗️
- **Base Model Building:** Logistic Regression was used to classify whether an individual would take the vaccine or not.
- **Hyperparameter Tuning:** 🔍 Used **GridSearchCV** to find the best parameters (`C`, `penalty`, `l1_ratio`, `solver`) for the model.
- **Class Balancing:** ⚖️ Used **SMOTE** to handle class imbalance by oversampling the minority class and retrained the model.

### Model Evaluation 📊
- **Metrics used:** precision, recall, f1-score, and accuracy.
- After using SMOTE, **recall improved** for the minority class, though precision decreased slightly.
- Evaluated the final model on the original test set using the best parameters.

### Future Improvements 🚀
- 🔄 Experiment with other algorithms like **Random Forest** or **XGBoost** to potentially improve model performance.
- 🛠️ Perform **feature engineering** to create more meaningful features that may enhance model accuracy.
- 🤖 Use **ensemble methods** to combine predictions from multiple models for better results.
