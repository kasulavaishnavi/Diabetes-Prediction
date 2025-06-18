Diabetes Prediction using Machine Learning
A data-driven classification project to predict the likelihood of diabetes using medical features. This project uses a variety of machine learning models and includes robust data cleaning, visualization, feature selection, and model evaluation.

Problem Statement
The goal is to build a classification model that can predict whether a patient has diabetes based on diagnostic measurements. The dataset used is the Pima Indians Diabetes Database

Dataset Features
- Independent Variables:  
  `Pregnancies`, `Glucose`, `BloodPressure`, `SkinThickness`, `Insulin`, `BMI`, `DiabetesPedigreeFunction`, `Age`
  Target Variable:  
  `Outcome` — Binary classification (0 = No diabetes, 1 = Has diabetes)
Key Steps & Techniques
1.Data Preprocessing
- Dropped duplicates, handled zero values in medically impossible columns.
- Replaced missing values with mean/median based on distribution.
- Outliers treated with `QuantileTransformer`.

2. Data Visualization
- Count plots, histograms, and box plots for distribution analysis.
- Heatmap for feature correlation (used to drop weak features).

3. Feature Selection
- Correlation matrix analysis helped drop less-informative features.

4. Model Training & Tuning
Used multiple ML classifiers:
-K-Nearest Neighbors (KNN)** – Tuned using GridSearchCV  
- Naive Bayes
- Support Vector Machine (SVM) – Hyperparameter tuned  
- Decision Tree – Grid search for best depth and criterion  
- Random Forest – Tuned for max_features and estimators  
- Logistic Regression

5.Evaluation Metrics
- Used: `F1 Score`, `Precision`, `Recall`, `Confusion Matrix`, and `Classification Report`.
- Focus on Recall, due to the medical importance of minimizing false negatives.

Results
KNN        -   F1 Score :0.6666666666666666, Precision score is: 0.6976744186046512, Recall score is: 0.6382978723404256, accuracy is 0.81
Naive Bayes     -   F1 Score :0.5813953488372093, Precision score is: 0.6410256410256411, Recall score is: 0.5319148936170213, accuracy is : 0.77  
SVM         -      F1 Score : 0.6666666666666666, Precision score is: 0.6976744186046512, Recall score is: 0.6382978723404256, accuracy is : 0.82  
Decision Tree -   F1 Score: 0.5675675675675675, Precision score is: 0.7777777777777778, Recall score is: 0.44680851063829785, accuracy is : 0.79  
Random Forest -  F1 Score: 0.6666666666666666, Precision score is: 0.6976744186046512, Recall score is: 0.6382978723404256, accuracy is : 0.79  
Logistic Regression  - F1 Score :0.627906976744186, Precision score is 0.6923076923076923, Recall score is: 0.574468085106383 ,accuracy is : 0.79  
