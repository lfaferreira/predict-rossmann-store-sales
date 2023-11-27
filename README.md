# Predict Rossmann Store Sales
Rossmann operates over 3,000 drug stores in 7 European countries. Currently, Rossmann store managers are tasked with predicting their daily sales for up to six weeks in advance. Store sales are influenced by many factors, including promotions, competition, school and state holidays, seasonality, and locality. With thousands of individual managers predicting sales based on their unique circumstances, the accuracy of results can be quite varied.


![vist Card](https://cdn.discordapp.com/attachments/1178722617440616498/1178723526706987149/news-2016-dirk-rossmann.jpg?ex=65772ed4&is=6564b9d4&hm=31eaa2b74e25bbb48fec46040dfc91f2089371f19156de5a00897af49f64f414&)


## Table of Contents

- [1 - Introduction](#1-Introduction)

- [2 - Data Understanding](#2-Data-Understanding)

- [3 - Action Plan](#3-Action-Plan)

- [4 - Exploratory Data Analysis](#4-Exploratory-Data-Analysis)

- [5 - Machine Learning Exploration](#5-Machine-Learning-Exploration)

- [6 - Submissions Results](#6-Submissions-Results)

- [7 - Models Comparison](#7-Models-Comparison)

- [8 - Conclusion](#8-Conclusion)


## 1 - Introduction
In their first Kaggle competition, Rossmann is challenging you to predict 6 weeks of daily sales for 1,115 stores located across Germany. Reliable sales forecasts enable store managers to create effective staff schedules that increase productivity and motivation. By helping Rossmann create a robust prediction model, you will help store managers stay focused on what’s most important to them: their customers and their teams! 

## 2 - Data Understanding
The **Rossmann Store Sales dataset**, available on **Kaggle**, is divided into training, store and test files. The combination of the training and store datasets corresponds to **1017209 rows and 18 columns**, where the data is divided into numerical and categorical, with the existence of missing data.

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


## 3 - Action Plan


### 3.1 - Objective


### 3.2 - Tools and Frameworks

Scope of tools used in the project:

- Python 3.11.5

- Jupyter Notebook

- Git & GitHub

- Kaggle

- Pandas

- Numpy

- Seaborn


## 4 - Exploratory Data Analysis


## 5 - Machine Learning Exploration


## 6 - Submissions Results


## 7 - Model Comparison


## 8 - Conclusion

