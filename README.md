# Predict Rossmann Store Sales
The current project addresses a problem of predicting daily sales over the next 6 weeks, in order to help the managers of each of Rossmann's more than 1000 stores.

![vist Card](https://cdn.discordapp.com/attachments/1178722617440616498/1178723526706987149/news-2016-dirk-rossmann.jpg?ex=65772ed4&is=6564b9d4&hm=31eaa2b74e25bbb48fec46040dfc91f2089371f19156de5a00897af49f64f414&)


## Table of Contents

- [1. Business Proposition](#1-Business-Proposition)

- [2. Data Understanding](#2-Data-Understanding)

- [3. Action Plan](#3-Action-Plan)

- [4. Exploratory Data Analysis](#4-Exploratory-Data-Analysis)

- [5. Machine Learning Exploration](#5-Machine-Learning-Exploration)

- [6. Business Results](#6-Business-Results)

- [7. Future Work](#7-Future-Work)


## 1. Business Proposition
The dataset corresponds to a chain of pharmacies in Germany from Rossmann. Rossmann daily catalogs internal and external variables regarding the operation of each pharmacy.

The project's idea is to use a machine learning model to predict the sales quantity that each store will have in the next six weeks, assisting managers in their future decision-making.

Assumptions
For the project to be coherent, some assumptions had to be made about the company's data:

- All data related to competition in stores that were not cataloged occurred because there was no such condition or they forgot to catalog them.
- All data related to promotions in stores that were not cataloged occurred because there was no such condition or they forgot to catalog them.

## 2. Data Understanding
The **Rossmann Store Sales dataset**, available on **[Kaggle](https://www.kaggle.com/c/rossmann-store-sales)**, is divided into training, store and test files. The combination of the training and store datasets corresponds to **1,017,209 rows and 18 columns**, where the data is divided into numerical and categorical, with the existence of missing data.

The dictionary of names for the training and store files is as follows:

| Attribute                     | Definition                                     | Data Type   |
|-------------------------------|------------------------------------------------|-------------|
| store                         | Store ID                                       | int64       |
| day_of_week                   | Day of the week (1 = Monday, ..., 7 = Sunday)  | int64       |
| date                          | Date of the sales data                         | object      |
| sales                         | Sales amount                                   | int64       |
| customers                     | Number of customers                            | int64       |
| open                          | Store open status (0 = Closed, 1 = Open)       | int64       |
| promo                         | Promo status (0 = No, 1 = Yes)                 | int64       |
| state_holiday                 | State holiday status                           | object      |
| school_holiday                | School holiday status                          | int64       |
| store_type                    | Store type                                     | object      |
| assortment                    | Assortment type                                | object      |
| competition_distance          | Distance to the nearest competitor store       | float64     |
| competition_open_since_month  | Month of competition opening                   | float64     |
| competition_open_since_year   | Year of competition opening                    | float64     |
| promo2                        | Promo2 status (0 = No, 1 = Yes)                | int64       |
| promo2_since_week             | Week of Promo2 initiation                      | float64     |
| promo2_since_year             | Year of Promo2 initiation                      | float64     |
| promo_interval                | Promo interval                                 | object      |


## 3. Action Plan


### 3.1. End Goal
The final product will be the dataset in which you can check the quantity of sales made by the stores, as well as the profit that these stores generated from their sales.


### 3.2. Tools and Frameworks

Scope of tools used in the project:

- Python 3.10.0
- Jupyter Notebook
- Git & GitHub
- Kaggle
- Pandas
- Numpy
- Hyperparameter Tuning
- Feature Selection Attributes (Boruta)
- Machine Learning Regression Models


### 3.3. CRISP-DM Process
The [CRIPS-DM](https://www.ibm.com/docs/en/spss-modeler/saas?topic=dm-crisp-help-overview) methodology was applied to trace my plan of action. Here's the process, step by step:

<p align="center">
 <img src="https://cdn.discordapp.com/attachments/1181695164633329824/1181695982753304697/CRISP-DM_Flowchart_ElderResearch_Circular-1.png?ex=6581ff25&is=656f8a25&hm=978e079ffa29bbb54af68d891c7318a2bb1f9a30f3ac0c144434b96df3e2a367&"  style="zoom:65%"/>
</p>


**Step 1. Business Understanding:**
- A company seeks a predictive model to assist managers in assessing the potential sales for the stores.

**Step 2. Data Understanding:**
- The dataset was collected from Kaggle and imported into the Jupyter Notebook.
- The data was studied to understand the impact of each variable on the stores and their influence on sales.
- We have 1,115 different stores, distributed in a dataset of 1,017,209 records.

**Step 3. Data Preparation:**
- Data preparation enables efficient analysis, limits errors and inaccuracies that may occur, making all processed data more accessible to users.
- The selection of data for training and testing the model took place by separating the last 6 weeks of data for the test set and using the rest for the training set, resulting in:
  - A total of 802,942, equivalent to 95% of the database used for training.
  - A total of 41,396, equivalent to 5% of the database used for testing.
- Data modeling was carried out considering their nature, where all variables were put on a comparable scale but with individual treatments.
  - Rescaling, feature transformation, encoding, converting categorical attributes into numerical attributes and creating new attributes.


**Step 4. Exploratory Data Analysis:**
- EDA is helpful to investigate the data and summarize the key insights
- It gives basic understanding of the data, it's distribution, null values and much more
- Graphs and python functions were used to extract key insights


**Step 5. Feature Selection:**
- Feature Selection is the method of choosing relevant features for the machine learning model
- A list is created with the estimated relevance of the attributes for learning the models
- For this purpose Boruta was utilized
- Selected attributes:
    01. `store`
    02. `promo`
    03. `store_type`
    04. `assortment`
    05. `competition_distance`
    06. `competition_open_since_month`
    07. `competition_open_since_year`
    08. `promo2`
    09. `promo2_since_week`
    10. `promo2_since_year`
    11. `competition_time_month`
    12. `promo_time_week`
    13. `day_of_week_sin`
    14. `day_of_week_cos`
    15. `month_sin`
    16. `month_cos`
    17. `day_sin`
    18. `day_cos`
    19. `week_of_year_sin`
    20. `week_of_year_cos`

**Step 6. Machine Learning Modeling:**
- 5 machine learning regression models were built, in order to find the best solution to the business proposition
- Models built:
  1. Average
  2. Linear Regressor
  3. Lasso
  4. Random Forest Regressor
  5. XGBoost Regressor

**Step 7. Evaluation:**
- Evaluation metrics are useful for determining the best machine learning model, out of the 5 previously built
- The succeeding metrics were used to evaluate the models:
  1. MAE - Mean Absolute Error
  2. MAPE - Mean Absolute Percentage Error
  3. RMSE - Root Mean Squared Error
- To ensure that our models are good generalization tools, cross-validation was utilized, as well as hyperparameters tuning
- Cross-validation is useful to reduce the bias of training the data, because it utilizes the entire dataset as training data
- Hyperparameter tuning is good for extracting the best parameters, that maximize the evaluation results


## 4. Exploratory Data Analysis


## 5. Machine Learning Exploration


## 6. Business Results


## 7. Future Work


