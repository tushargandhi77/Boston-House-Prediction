


# Boston House Price Prediction

![Data Science](https://img.shields.io/badge/Data%20Science-Project-blue)
![Python](https://img.shields.io/badge/Python-3.10+-green)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-Models-orange)
![Machine Learning](https://img.shields.io/badge/Deep%20Learning-Models-red)
![Status](https://img.shields.io/badge/Status-Completed-success)

## Introduction
This project involves predicting house prices in Boston using various machine learning models. The dataset used contains information collected by the U.S Census Service concerning housing in the area of Boston, Massachusetts. The main objective is to predict the value of prices of the houses using different features available in the dataset.

## Dataset Description
The Boston housing dataset includes 506 rows and 14 columns, where each row represents a unique instance of housing data, and each column represents a specific attribute of the houses. The features included in the dataset are:

* CRIM: Per capita crime rate by town.
* ZN: Proportion of residential land zoned for lots over 25,000 sq. ft.
* INDUS: Proportion of non-retail business acres per town.
* CHAS: Charles River dummy variable (1 if tract bounds river; 0 otherwise).
* NOX: Nitric oxides concentration (parts per 10 million).
* RM: Average number of rooms per dwelling.
* AGE: Proportion of owner-occupied units built prior to 1940.
* DIS: Weighted distances to five Boston employment centers.
* RAD: Index of accessibility to radial highways.
* TAX: Full-value property tax rate per $10,000.
* PTRATIO: Pupil-teacher ratio by town.
* B: 1000(Bk - 0.63)^2 where Bk is the proportion of Black people by town.
* LSTAT: Percentage of lower status of the population.
* MEDV: Median value of owner-occupied homes in $1000s.

![image](https://github.com/user-attachments/assets/4eeae00a-27fa-496d-9fc5-2a4760ba233f)

## Data Cleaning
Duplicate Value Removal
Upon initial inspection, it was found that the dataset does not contain any duplicate entries. Hence, no action was required for removing duplicates.

![image](https://github.com/user-attachments/assets/09560a1c-560e-4445-a671-baaf06768689)


## Handling Missing Values
The dataset was checked for any missing values. Since there were no missing values in the dataset, no imputation or removal of missing data was necessary.
![image](https://github.com/user-attachments/assets/cb36cc12-7248-4e74-a2be-8dc64b736421)

## Outlier Detection and Handling
Box Plot for Outlier Detection
Box plots were utilized to detect the presence of outliers in the dataset. The box plots highlighted some outliers across various features, such as CRIM, ZN, and RM. However, considering the small size of the dataset (506 rows), we decided against removing these outliers to avoid losing valuable information that could affect model performance.

## Exploratory Data Analysis (EDA)

### Pair Plot
A pair plot was generated to visualize the relationships between different features and to understand the distribution of data. This helped in identifying patterns and correlations between the features which could be useful for model building.

![image](https://github.com/user-attachments/assets/91a63795-4d60-4128-a6e9-a6174de5b6ab)

### Correlation Heatmap
A correlation heatmap was created to analyze the correlation between different features. This visualization was crucial in identifying which features had strong positive or negative correlations with the target variable (house prices). Highly correlated features can provide significant insights and improve model performance.

![image](https://github.com/user-attachments/assets/5ae5d9fc-ae69-4b21-adb8-11b08404bc15)


## Model Building
### Linear Regression
Linear Regression was the first model applied to the dataset. This model provided a baseline performance with an R² score of approximately 71%. While the model captured some of the variance in the data, it was clear that more sophisticated models could yield better performance.
![image](https://github.com/user-attachments/assets/4272f343-b0c9-47b3-a27b-b315f967a0e8)

### Decision Tree
The Decision Tree model improved the performance significantly with an R² score of around 76%. This model was able to capture more complex patterns in the data compared to Linear Regression. However, it was also prone to overfitting, which was evident from the model's performance on the training set versus the test set.
![image](https://github.com/user-attachments/assets/ef9a84b2-58e2-4752-b908-47c35d6c3cbd)

### Random Forest
Random Forest, an ensemble learning method, was applied to further improve the prediction accuracy. This model provided the best performance with an R² score of approximately 86%. By combining the predictions of multiple decision trees, Random Forest managed to reduce overfitting and provided a more robust model.
![image](https://github.com/user-attachments/assets/4010b517-ed8b-483c-ba52-2fe5f66b7833)
## Conclusion
In this project, we explored various steps involved in building a house price prediction model using the Boston housing dataset. Starting from data cleaning and EDA, we moved on to applying different machine learning models. The Random Forest model yielded the best performance with an R² score of 86%, demonstrating its effectiveness in handling the complexities of the dataset.

### Future improvements could include:

* Feature engineering to create new meaningful features
* Hyperparameter tuning of models for better performance
* Exploring other advanced algorithms like Gradient Boosting or Neural Networks
