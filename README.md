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

Model             F1 Score  Precision  Recall
KNN               ~0.76      ~0.74      ~0.78  
Naive Bayes        ~0.73      ~0.69     ~0.78  
SVM                ~0.75      ~0.74      ~0.76 
Decision Tree      ~0.72      ~0.70      ~0.75 
Random Forest      ~0.79      ~0.76      ~0.83 
Logistic Regression  ~0.75    ~0.72      ~0.77 
