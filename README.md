# Bike_Demand_Anlaysis
This Python script implements a machine learning model to predict bike-sharing demand in Seoul based on various environmental and temporal features. It utilizes the `SeoulBikeData.csv` dataset, which includes information like date, time, temperature, humidity, wind speed, visibility, and more.

Here's a breakdown of the code's functionality:

1.  **Data Loading and Preprocessing:**
    *   Loads the data from the CSV file using pandas.
    *   Cleans up column names by replacing spaces with underscores.
    *   Categorizes the `Rented_Bike_Count` into three classes: 0 (less than 400), 1 (400-1000), and 2 (greater than 1000). This converts the problem into a classification task.
    *   Encodes categorical features (`Date`, `Seasons`, `Holiday`, `Functioning_Day`) into numerical representations using Label Encoding.

2.  **Data Splitting and Scaling:**
    *   Splits the data into training and testing sets using `train_test_split`.
    *   Scales the numerical features using `StandardScaler` to standardize the data, which is important for many machine learning algorithms.

3.  **Model Training and Evaluation:**
    *   Trains three different classification models:
        *   Random Forest Classifier (`RandomForestClassifier`)
        *   Support Vector Machine (SVM) (`SVC`) - Includes commented-out code for GridSearchCV to find the best hyperparameters.
        *   Logistic Regression (`LogisticRegression`)
    *   Evaluates the performance of each model on the test set using accuracy as the metric.

4.  **Hyperparameter Tuning:**
    *   The code includes a commented-out section showing how to use `GridSearchCV` to find the optimal hyperparameters for the SVM model.  This is an important step to improve model performance, but it can be computationally expensive, so it's left commented out by default.

5.  **Cross-Validation:**
    *   The code now includes an example of how to use `cross_val_score` with Random Forest. Cross-validation is a crucial technique for robust model evaluation and helps to prevent overfitting.


