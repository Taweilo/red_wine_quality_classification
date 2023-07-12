# 🍷 Red Wine Quality Prediction 
![Red Wine](https://learn.wineenthusiast.com/wp-content/uploads/2019/09/HeaderImage.svg)
This project will follow the BA workflow to tackle red wine business issues using data mining techniques. A red wine retailer imports wine and sells it to customers. Thus, it needs to predict the wine quality for the business when importing. Via machine learning techniques, we can classify and predict the quality in advance. By evaluating the model performance, we can further make better decisions and thus maximize the profits.

## 1. Business Understanding
The problem for the Red Wine industry is to import wine based on limited information. Applying the machine learning technique, we can a model for wine quality prediction, according to its chemical content. The merit of the machine learning method is cost-effective and simple (not much domain knowledge is required). Below is the number we make up for the profits evaluation:

Without the machine learning model, we can only buy wine at a fixed price of $75 for all wine. 
With an improved method, we can use prediction and make different offers: high-quality wine for $100, and low-quality for $50.
In addition, we sell wine at $150 for good wine but $60 for bad wine. 

For each type of wine predicted, we have the profits($) as below:<br>    
    TP = 150-100=50 (predict good wine and get one)<br>   
    FP = 60-100=-40 (predict good wine but did not correct)<br>   
    TN = 60-50=10   (predict bad wine and get one)<br>   
    FN = 150-50=100 (predict bad wine but luckily get good wine)<br>   
Therefore, in the machine learning project, we hope to develop an accurate model which can 1) predict the wine quality well and 2) maximize the profits.

## 2. Data Understanding
The credit line increase data was loaded via google collab file. Basic data analysis was performed to identify the shape of data, get column names, find missing values, and generate descriptive statistics. The Pearson correlation matrix was calculated to find the pairwise correlation of the columns in the data. All columns in the data are visually represented as histograms. A correlation heatmap figure was generated to represent the correlation matrix.

 <img src="https://github.com/Taweilo/Red_Wine_Quality_Classification_Model/blob/main/image/data%20statistics.jpg" width="700" >


##### Correlation Heatmap
 <img src="https://github.com/Taweilo/Red_Wine_Quality_Classification_Model/blob/main/image/heatmap.jpg" width="600" >

##### Quality Distribution


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
 <img src="https://github.com/Taweilo/Red_Wine_Quality_Classification_Model/blob/main/image/evaluation.jpg" width="600" >

## 6. Business Value
 <img src="https://github.com/Taweilo/Red_Wine_Quality_Classification_Model/blob/main/image/business%20value.jpg" width="600" >

## 7. Reference
