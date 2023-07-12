# ⚡ Red Wine Quality Prediction 🍷🍷
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
The Wine Quality data was loaded via Jupyter Notebook. 
Dataset is from Kaggle: https://www.kaggle.com/datasets/yasserh/wine-quality-dataset?resource=download (also please see WineQT.CSV attached). Basic data analysis was performed to identify the shape of data, get column names, find missing values, and generate descriptive statistics. The Pearson correlation matrix was calculated to find the pairwise correlation of the columns in the data. All columns in the data are visually represented as histograms. A correlation heatmap figure was generated to represent the correlation matrix.

* Data dictionary: 

| Name | Modeling Role | Measurement Level| Description|
| ---- | ------------- | ---------------- | ---------- |
|**ID**| ID | int | unique row indentifier |
| **LIMIT_BAL** | input | float | amount of previously awarded credit |
| **SEX** | demographic information | int | 1 = male; 2 = female
| **RACE** | demographic information | int | 1 = hispanic; 2 = black; 3 = white; 4 = asian |
| **EDUCATION** | demographic information | int | 1 = graduate school; 2 = university; 3 = high school; 4 = others |
| **MARRIAGE** | demographic information | int | 1 = married; 2 = single; 3 = others |
| **AGE** | demographic information | int | age in years |
| **PAY_0, PAY_2 - PAY_6** | inputs | int | history of past payment; PAY_0 = the repayment status in September, 2005; PAY_2 = the repayment status in August, 2005; ...; PAY_6 = the repayment status in April, 2005. The measurement scale for the repayment status is: -1 = pay duly; 1 = payment delay for one month; 2 = payment delay for two months; ...; 8 = payment delay for eight months; 9 = payment delay for nine months and above |
| **BILL_AMT1 - BILL_AMT6** | inputs | float | amount of bill statement; BILL_AMNT1 = amount of bill statement in September, 2005; BILL_AMT2 = amount of bill statement in August, 2005; ...; BILL_AMT6 = amount of bill statement in April, 2005 |
| **PAY_AMT1 - PAY_AMT6** | inputs | float | amount of previous payment; PAY_AMT1 = amount paid in September, 2005; PAY_AMT2 = amount paid in August, 2005; ...; PAY_AMT6 = amount paid in April, 2005 |
| **DELINQ_NEXT**| target | int | whether a customer's next payment is delinquent (late), 1 = late; 0 = on-time |

##### Statistics
 <img src="https://github.com/Taweilo/Red_Wine_Quality_Classification_Model/blob/main/image/data%20statistics.jpg" width="700" >


##### Correlation Heatmap
 <img src="https://github.com/Taweilo/Red_Wine_Quality_Classification_Model/blob/main/image/heatmap.jpg" width="600" >

##### Quality Distribution


## 3. Data Preparation
The data is partitioned into training, and test sets (60% and 40% respectively) to accurately evaluate the model. Testing data which is a separate set of data is used to test the model after training. 
* Y target variable is Quality Score. It's binary.
* X independent variables include fixed acidity, volatile acidity, citric acid, residual sugar, chlorides, free sulfur dioxide, total sulfur dioxide, density, pH, sulfates, and alcohol. It's continuous.

## 4. Modeling
* SVC
* Logistic regression
* KNN
* Decision Tree
* Random Forest
* Random Forest with Tuning
* Adaboost

## 5. Evaluation
 <img src="https://github.com/Taweilo/Red_Wine_Quality_Classification_Model/blob/main/image/evaluation.jpg" width="600" >

## 6. Business Value
From the below graph, we can easily compare the business value between the ml model (RF classifier) and the non-ml model: by considering the relationship between the true positive rate and expected profits on the two models. 
* RF classifier performance is better than the non-ml model
* True positive rate has a positive relationship with expected profits because more good wine in the population yields more profits. Detail check with the information below the graph. 
  
 <img src="https://github.com/Taweilo/Red_Wine_Quality_Classification_Model/blob/main/image/business%20value.jpg" width="600" >

## 7. Reference
