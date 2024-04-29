# Day 25 - Diabetes Challange
# 26.04.2024
# Meme of the day
![Data Fun]([FRhzEK1X0AMeAJi.jpegg](https://imgflip.com/i/8o4o54))
---
##  Schedule

|Time|Content|
|---|---|
|09:00 - 10:00|Daily review |
|10:00 - 10:30|Pipelines |
|10:30 - 11:00|Presentation of Gropu Challenge |
|12:00 - 13:00|Lunch break |
|13:00 - 16:00|Group Challenge |
|16:00 - 16:30|Daily standup |

---
## Daily review

- Discuss protocol of Day 24 

---
## Pipelines
**Pipeline** 
Can be used to chain multiple estimators into one. This is useful as there is often a fixed sequence of steps in processing the data, for example feature selection, normalization and classification. Pipeline serves multiple purposes here:

- Convenience and encapsulation
    You only have to call fit and predict once on your data to fit a whole sequence of estimators.

- Joint parameter selection
    You can grid search over parameters of all estimators in the pipeline at once.

- Safety
    Pipelines help avoid leaking statistics from your test data into the trained model in cross-validation, by ensuring that the same samples are used to train the transformers and predictors.

All estimators in a pipeline, except the last one, must be transformers (i.e. must have a transform method). The last estimator may be any type (transformer, classifier, etc.).

**GridSearchCV vs RandomizedSearchCV**
GridSearchCV exhaustively searches through a specified parameter grid to find the optimal combination of hyperparameters, making it suitable for smaller parameter spaces but use a lot of computer resources.

RandomizedSearchCV randomly samples hyperparameter combinations, making it more efficient for larger spaces and often faster at finding good solutions.

---
## Presentation of Gropu Challenge

**Diabetes Challenge**

Our task was is to analyze the Kaggle "Pima Indians Diabetes Database" and  predict whether a patient has Diabetes or not.

**Task**
During the task:

-Data was loaded from the diabetes schema in the database using the .env file provided.
-The database was explored to understand the relationships between tables (1-1, 1-N, N-M).
-The data was examined to determine its relevance and coherence.
-Appropriate JOINs were identified based on the relationships between tables.
-Two classification algorithms were applied to predict diabetes patients.
-Evaluation metrics were discussed before modeling to choose the most suitable one.
-GridSearchCV or RandomizedSearchCV was utilized to tune hyperparameters.
-As an optional step, sklearn's Pipeline module was explored to encapsulate all steps into a pipeline.
-Additionally, the data was split into training and test sets to analyze the final model's performance on unseen data. Scaling was considered to potentially enhance model performance.

## Group Challenge

During the task, we need to deal with data corruption and we also need to address a large amount of missing data.

To handle data corruption or missing values in data:

-Identify where they occur.
-Fill them with appropriate replacements like mean, median, or mode, or delete the rows/columns.
-Use predictive methods or domain knowledge when necessary.
-If necessary, mark missing values to separate them from actual data.

## Daily standup
- Review Challenge results
