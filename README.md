# ⚡⚡ Red Wine Quality Prediction 🍷🍷
![Python version](https://img.shields.io/badge/Python%20version-3.10%2B-lightgrey)
![GitHub last commit](https://img.shields.io/github/last-commit/Taweilo/Red_Wine_Quality_Classification_Model)
![GitHub repo size](https://img.shields.io/github/repo-size/Taweilo/Red_Wine_Quality_Classification_Model)
![Type of ML](https://img.shields.io/badge/Type%20of%20ML-Binary%20Classification-red)
![License](https://img.shields.io/badge/License-MIT-green)

Badge [source](https://shields.io/)

![Red Wine](https://learn.wineenthusiast.com/wp-content/uploads/2019/09/HeaderImage.svg)
This project will follow the BA workflow to tackle red wine business issues using data mining techniques. A red wine retailer imports wine and sells it to customers. Thus, it needs to predict the wine quality for the business when importing. Via machine learning techniques, we can classify and predict the quality in advance. By evaluating the model performance, we can make better decisions and thus maximize profits.
Overall, the Radom Forest classification model maximizes profits the most. Considering the non-ml and ml model, ml model always performs better than the non-ml model under different true positive rate conditions. 

### Repository structure

```
├── Image
│   ├── 2.1 Data statistics.jpg                    <- data statistics summary used in the README
│   ├── 2.2 Heatmap.jpg                            <- heatmap image used in the README
│   ├── 2.3 Quality distribution.jpg               <- quality distribution image used in the README
│   ├── 5.1 Evaluation.jpg                         <- model summary table used in the README
│   ├── 6.1 Business value.jpg                     <- image used in the README                            
│
├── LICENSE.txt                                    <- license
├── Red Wine Classification Project.ipynb          <- code
├── WineQT.csv                                     <- dataset
```

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
Dataset is from Kaggle: https://www.kaggle.com/datasets/yasserh/wine-quality-dataset?resource=download (also please see WineQT.csv attached). Basic data analysis was performed to identify the shape of data, get column names, find missing values, and generate descriptive statistics. The Pearson correlation matrix was calculated to find the pairwise correlation of the columns in the data. All columns in the data are visually represented as histograms. A correlation heatmap figure was generated to represent the correlation matrix.

* Data dictionary:
  
| Name | Modeling Role | Measurement Level| Description|
| ---- | ------------- | ---------------- | ---------- |
| **Fixed Acidity** | input | float | The amount of non-volatile acids (such as tartaric, malic, and succinic acid). These acids are important for flavor and stability, and can contribute to the wine's tartness or sourness. However, too much acidity can also make the wine taste sour or unbalanced. On the other hand, low levels of fixed acidity can make the wine taste flat or dull. |
| **Volatile Acidity** | input | float | Taste measure, sign of winemaking quality. Higher – less control over taste. |
| **Citric Acid** | input | float | Not typically present in significant amounts in wine, but it can be added during winemaking to adjust the wine's acidity or enhance its flavor profile. Citric acid can contribute a bright, citrusy note to the wine, which can be desirable in some styles of white wine, rosé, or sparkling wine. |
| **Residual Sugar** | input | float | The amount of the natural grape sugars that remain in the wine after fermentation is complete. |
| **Chlorides** | input | float | The level of chlorides in wine can have an impact on the sensory characteristics of the wine, as well as its overall quality. |
| **Free Sulfur Dioxide** | input | float | A type of sulfur dioxide presents in wine. SO2 is added to wine during the winemaking process to protect the wine from oxidation and microbial spoilage. |
| **Total Sulfur Dioxide** | input | float | The sum of the free and bound forms of sulfur dioxide that are present in the wine. |
| **Density** | input | float | Density can be used to determine the alcohol content and sugar content. |
| **pH** | input | float | 	pH is an important parameter that can affect the wine's stability, color, aroma, and taste. A wine with a low pH tends to be more refreshing, and age-worthy, while a wine with a high pH may be flatter, or dull. |
| **Sulfates** | input | float | A chemical compound that occurs naturally at low levels during the process of wine fermentation. It is also added by many winemakers during the fermentation stage of winemaking to protect and preserve the wine's character, flavor, and color. |
| **Alcohol**| input | float | The average alcohol content of wine is about 12%. |
| **ID**| ID | int | The unique number of each row. |
| **Quality**| potential target | int | Categorical value: range from 3 to 8. During the Data preparation process, we transform into binary values: above 6.5 is good; quall or below 6.5 is inferior.|

* Statistics
 <img src="https://github.com/Taweilo/Red_Wine_Quality_Classification_Model/blob/main/Image/2.1 Data%20statistics.jpg" width="600" >

* Correlation Heatmap
 <img src="https://github.com/Taweilo/Red_Wine_Quality_Classification_Model/blob/main/Image/2.2 Heatmap.jpg" width="400" >

* Quality Distribution
 <img src="https://github.com/Taweilo/Red_Wine_Quality_Classification_Model/blob/main/Image/2.3 Quality%20distribution.jpg" width="400" >  

| Quality Score |   3 |   4 |   5 |   6 |   7 |   8 |
| ------------- | --- | --- | --- | --- | --- | --- |
| **Count** | 483 | 462 | 143 | 33 | 16 | 6 |

## 3. Data Preparation

1. Convert the Quality Score into binary: Good wine = 1, Bad wine = 0.
2. Split the data: The data is partitioned into training, and test sets (60% and 40% respectively) to accurately evaluate the model. Testing data which is a separate set of data is used to test the model after training. Variable composition: 
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
 <img src="https://github.com/Taweilo/Red_Wine_Quality_Classification_Model/blob/main/Image/5.1 Evaluation.jpg" width="500" >
From the summary table, we can observe that AUC is not necessary to associate with high profits.

* SVC has a low AUC score but yields the highest profits. However, AdaBoost has the highest AUC score but yields the lowest profits.
* The reason for low accuracy but high profits mainly is the inaccurate prediction. False negative yields $100, because the model predicts poor wine but it's good wine actually.
* Considering high AUC and high expected profits, Random Forest could be a good model.

## 6. Recommendation
* Business Value: <br>
From the below graph, we can easily compare the business value between the ml model (RF classifier) and the non-ml model: by considering the relationship between the true positive rate and expected profits on the two models. 
1. RF classifier performance is better than the non-ml model.
2. True positive rate has a positive relationship with expected profits because more good wine in the population yields more profits. Detail check with the information below the graph.
3. Under the extreme case where the true positive rate is 0, meaning no good wine in the population, the non-ml model suffers a loss but the ml model can still make a profit. It's because ml model can predict red wine quality and discriminate the price. However, the non-ml model only produces one and only offer which is $75. Buy high sell low incurs a loss. 
  <img src="https://github.com/Taweilo/Red_Wine_Quality_Classification_Model/blob/main/Image/6.1 Business%20value.jpg" width="600" >
  
* Limitation: <br>
1. RF classifier is neither the most accurate nor the most profitable model. We recommend the user evaluate the business needs. 
2. The dataset used may not be comprehensive or representative enough for generalization.
3. The model's ability to predict the wine quality might be limited by the quality and the scope of the data used for training.
 
