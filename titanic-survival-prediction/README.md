Titanic Survival Prediction

A beginner machine learning project predicting passenger survival on the Titanic using classification models.

Overview

This project uses the classic Titanic dataset (loaded via seaborn) to predict whether a passenger survived, based on features like class, sex, age, fare, and family size aboard.

Dataset


Source: seaborn.load_dataset('titanic')
Target variable: survived (0 = did not survive, 1 = survived)
Features used: pclass, sex, age, fare, sibsp, parch


Approach


Data loading & cleaning — handled missing values in age and fare using median imputation.
Feature encoding — converted sex to a numeric column using one-hot encoding.
Train/test split — 80/20 split with random_state=42 for reproducibility.
Baseline — calculated the accuracy of always predicting the majority class, as a benchmark.
Modeling:

Logistic Regression (primary model)
Random Forest Classifier (comparison model)



Evaluation — accuracy, confusion matrix, and precision/recall/F1 via classification report.
Interpretation — examined Logistic Regression coefficients and Random Forest feature importances to understand which factors most influenced survival.


Results

ModelAccuracyBaseline (majority class)~0.61Logistic Regressionfill in your resultRandom Forestfill in your result

Key Takeaways


Sex and passenger class were the strongest predictors of survival, consistent with historical accounts ("women and children first," and first-class passengers having better access to lifeboats).
Random Forest's added complexity did not necessarily outperform the simpler Logistic Regression model on this dataset.


Files


titanic_survival_prediction.ipynb — full notebook with code, outputs, and analysis


Tools Used


Python
pandas, numpy
seaborn (for dataset loading)
scikit-learn (LogisticRegression, RandomForestClassifier, train_test_split, metrics)
