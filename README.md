# Red Wine Quality Prediction
![Red Wine](https://learn.wineenthusiast.com/wp-content/uploads/2019/09/HeaderImage.svg)
<img src="[https://learn.wineenthusiast.com/wp-content/uploads/2019/09/HeaderImage.svg" width="100" height="100">
This project will follow the BA workflow to tackle red wine business issues using data mining techniques. A red wine retailer imports wine and sells it to customers. Thus, it needs to predict the wine quality for the business. Via machine learning techniques, we can classify and predict the quality. By evaluating the model performance, we can further make better decisions and thus maximize the profits.

## 1. Business Understanding
Before the machine learning model, we can only buy wine at a fixed price of $75 for all wine. 
With an improved method, we can use prediction to import high-quality wine for $100, and low quality $50.
In addition, we sell wine at $150 for good wine but $60 for bad wine. 

For each type of wine predicted, we have the profits($) as below:<br>    
    TP = 150-100=50<br>   
    FP = 60-100=-40<br>   
    TN = 60-50=10<br>   
    FN = 150-50=100<br>   
Therefore, in the machine learning project, we hope to develop an accurate model which can 1) predict the wine quality well and 2) maximize the profits.

## 2. Data Understanding
The credit line increase data was loaded via google collab file. Basic data analysis was performed to identify the shape of data, get column names, find missing values, and generate descriptive statistics. The Pearson correlation matrix was calculated to find the pairwise correlation of the columns in the data. All columns in the data are visually represented as histograms. A correlation heatmap figure was generated to represent the correlation matrix.
![Statistics](https://github.com/Taweilo/Red_Wine_Quality_Classification_Model/blob/main/image/data%20statistics.jpg width="100")


##### Correlation Heatmap
![Heat Map](https://github.com/Taweilo/Red_Wine_Quality_Classification_Model/blob/main/image/heatmap.jpg)

##### Quality Distribution
![Heat Map](https://user-images.githubusercontent.com/111590512/185942386-95eece6c-45d5-483b-a582-e665e5cfa083.png| width=400)

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
![Summary table](https://github.com/Taweilo/Red_Wine_Quality_Classification_Model/blob/main/image/evaluation.jpg)

## 6. Business Value
![Business Value](https://github.com/Taweilo/Red_Wine_Quality_Classification_Model/blob/main/image/business%20value.jpg)

## 7. Reference
