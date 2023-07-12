# Red Wine Quality Prediction

## 1. Business Understanding
This project will follow the BA workflow to tackle red wine business issues using data mining techniques. A red wine retailer imports wine and sells it to customers. Thus, it needs to predict the wine quality for the business. Via machine learning techniques, we can classify and predict the quality. By evaluating the model performance, we can further make better decisions and thus maximize the profits.

## 2. Data Understanding
The credit line increase data was loaded via google collab file. Basic data analysis was performed to identify the shape of data, get column names, find missing values, and generate descriptive statistics. The Pearson correlation matrix was calculated to find the pairwise correlation of the columns in the data. All columns in the data are visually represented as histograms. A correlation heatmap figure was generated to represent the correlation matrix.

##### Correlation Heatmap
![Heat Map](https://user-images.githubusercontent.com/111590512/185942386-95eece6c-45d5-483b-a582-e665e5cfa083.png)

##### Quality Distribution
![Heat Map](https://user-images.githubusercontent.com/111590512/185942386-95eece6c-45d5-483b-a582-e665e5cfa083.png)

## 3. Data Preparation
The data is partitioned into training, validation, and test sets (50%, 25%, 25% respectively) to accurately evaluate the model. Testing data which is a separate set of data is used to test the model after training, to help us determine how the model will perform in the real world. We trained 12 different models using decision trees and calculated the ROC AUC for each model. 

## 4. Modeling
* **SVC**
* **Logistic regression**
* **KNN**
* **Decision Tree**
* **Random Forest**
* **Random Forest with Tuning**
* **Adaboost**

## 5. Evaluation
![Heat Map](https://user-images.githubusercontent.com/111590512/185942386-95eece6c-45d5-483b-a582-e665e5cfa083.png)

## 6. Reference
