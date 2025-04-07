# Sonar Dataset Classification Project

Sonar Mines vs Rocks dataset
The problem is to predict metal or rock objects from sonar return data. Each pattern is a set of 60 numbers in the range
0.0 to 1.0. Each number represents the energy within a particular frequency band, integrated over a certain period of time.
The label associated with each record contains the letter R if the object is a rock and M if it is a mine (metal cylinder).
The numbers in the labels are in increasing order of aspect angle, but they do not encode the angle directly.

## Steps in the Project

1. **Data Exploration**:
    - Loaded the dataset and examined its shape, description, and class distribution.
    - Visualized the distribution of features using histograms and correlations between columns.

2. **Data Preprocessing**:
    - Defined the target variable (`y`) and feature variables (`X`).
    - Split the data into training and validation sets (80% training, 20% validation).

3. **Modeling**:
    - Applied several classification algorithms without and with standardizing data, including:
      - Logistic Regression
      - Linear Discriminant Analysis (LDA)
      - Naive Bayes
      - Classification and Regression Trees (CART)
      - K-Nearest Neighbors (KNN)
      - Support Vector Machine (SVM)

4. **Model Evaluation**:
    - Compared the performance of the models using accuracy as the evaluation metric.
    - Found that KNN and SVM had similar performance, so hyperparameter tuning was performed on both.

5. **Hyperparameter Tuning**:
    - Tuned the SVM and KNN models, resulting in an improved accuracy of **85%** using SVM with the following parameters:
      - `'C': 1,7`
      - `'kernel': 'rbf'`

6. **Modeling ensemble methods**:
    - Applied several classification ensemble methods without and with standardizing data, including:
      - Adaptive Boosting (AB)
      - Gradient Boosting (GBM)
      - Random Forest (RF)
      - ExtraTrees (ET)

7. **Model Evaluation**:
    - Compared the performance of the ensemble methods using accuracy as the evaluation metric.
    - Found that ET wih standardizing data has the best accuracy of **87%** 

7. **Hyperparameter Tuning**:
    - Tuned ExtraTreesClassifier model, resulting in an improved accuracy of **88%** using ET with parametar:
      - `'n_extimators': 250`

6. **Final Results**:
    - Displayed the confusion matrix and classification report to assess the performance of the final model.


## Conclusion

The project demonstrates how data exploration, preprocessing, and model tuning can be used to classify the Sonar dataset effectively. The final model achieved an accuracy of **88%**, with significant improvements from the initial models.
