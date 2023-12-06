# Instacart-Market-Basket-Analysis-

## Introduction

Instacart is an American technology company that operates as a same-day grocery delivery and pick up service in the U.S. and Canada. Customers shop for groceries through the Instacart mobile app or Instacart.com from various retailer partners. The order is shopped and delivered by an Instacart personal shopper.

### Objectives:
- Analyze the anonymized [data](https://www.kaggle.com/c/instacart-market-basket-analysis/data) of 3 million grocery orders from more than 200,000 Instacart users open sourced by Instacart 
- Find out hidden association between products for better cross-selling and upselling
- Perform customer segmentation for targeted marketing and anticipate customer behavior
- Build a Machine Learning model to predict which previously purchased product will be in user’s next order

### Project Organization
```
.
├── Plots/                                      : Contains all plots 
├── Data Description and Analysis.ipynb         : Initial analysis to understand data
├── Exploratory Data Analysis.ipynb             : EDA to analyze customer purchase pattern
├── Customers Segmentation.ipynb                : Customer Segmentation based on product aisles


## Data Description

- **aisles:** This file contains different aisles and there are total 134 unique aisles.

- **departments:** This file contains different departments and there are total 21 unique departments.

- **orders:** This file contains all the orders made by different users. From below analysis, we can conclude following:
    - There are total 3421083 orders made by total 206209 users.
    - There are three sets of orders: Prior, Train and Test. The distributions of orders in Train and Test sets are similar whereas the distribution of orders in Prior set is different.
    - The total orders per customer ranges from 0 to 100.
    - Based on the plot of 'Orders VS Day of Week' we can map 0 and 1 as Saturday and Sunday respectively based on the assumption that most of the people buy groceries on weekends.
    - Majority of the orders are made during the day time.  
    - Customers order once in a week which is supported by peaks at 7, 14, 21 and 30 in 'Orders VS Days since prior order' graph.
    - Based on the heatmap between 'Day of Week' and 'Hour of Day,' we can say that Saturday afternoons and Sunday mornings are prime time for orders.

<p align="center">
  <img width="300" height="200" src=["https://github.com/archd3sai/Instacart-Market-Basket-Analysis/blob/master/Plots/dow.png"](https://github.com/SaurabhPoman96/Instacart-Market-Basket-Analysis-/blob/main/Plots/Frequency%20of%20Day%20of%20week%20Vs%20Hour%20of%20day.png)https://github.com/SaurabhPoman96/Instacart-Market-Basket-Analysis-/blob/main/Plots/Frequency%20of%20Day%20of%20week%20Vs%20Hour%20of%20day.png>
</p>

