# Instacart-Market-Basket-Analysis-

## Introduction

Instacart is an American technology company that operates as a same-day grocery delivery and pick up service in the U.S. and Canada. Customers shop for groceries through the Instacart mobile app or Instacart.com from various retailer partners. The order is shopped and delivered by an Instacart personal shopper.

### Objectives:
- Analyze the anonymized [data](https://www.kaggle.com/c/instacart-market-basket-analysis/data) of 3 million grocery orders from more than 200,000 Instacart users open sourced by Instacart 
- Find out hidden association between products for better cross-selling and upselling
- Perform customer segmentation for targeted marketing and anticipate customer behavior

### Project Organization
```
.
├── Plots/                                      : Contains all plots 
├── Data Description and Analysis.ipynb         : Initial analysis to understand data
├── Exploratory Data Analysis.ipynb             : EDA to analyze customer purchase pattern
├── Customers Segmentation.ipynb                : Customer Segmentation based on product aisles
```
<br />

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
  <img width="300" height="200" src="["https:Plots/Frequency of Day of week Vs Hour of day.png"]">
</p>

## Customer Segmentation

Customer segmentation is the process of dividing customers into groups based on common characteristics so companies can market to each group effectively and appropriately. We can perform segmentation using the data of which products users buy. Since there are thousonds of products and also thousands of customers, I utilized aisles which represent categories of products. 

I then performed Principal component analysis to reduce dimensions as KMeans does not produce good results on higher dimensions. Using 10 principal components I carried out KMeans clustering. I chose optimal number of clusters as 5 using Elbow method shown below.

The clustering results into 5 neat clusters and after checking most frequent products in them, we can conclude following:
- Cluster 1 results into 5428 consumers having a very strong preference for water seltzer sparkling water aisle.
- Cluster 2 results into 55784 consumers who mostly order fresh vegetables followed by fruits.
- Cluster 3 results into 7948 consumers who buy packaged produce and fresh fruits mostly.
- Cluster 4 results into 37949 consumers who have a very strong preference for fruits followed by fresh vegetables.
- Cluster 5 results into 99100 consumers who orders products from many aisles. Their mean orders are low compared to other clusters which tells us that either they are not frequent users of Instacart or they are new users and do not have many orders yet. 
