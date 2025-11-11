# All my Data Projects

## Overview
### 1. Amazon Product Ratings and Reviews EDA
#### Description: 
This project explores Amazon product data — including product details, prices, ratings, and customer reviews — to uncover insights about consumer behavior and product performance. The dataset contains information such as product ID, name, category, discounted and actual prices, ratings, number of reviews, review text, and user information.

#### Background: 
Customer reviews and pricing strategies play a major role in how products perform on e-commerce platforms. By analyzing this data, we can better understand how discounts, ratings, and customer sentiment influence sales and product success.

#### Project Objective: 
The goal of this exploratory analysis is to identify patterns in pricing and discounting, compare performance across categories, and explore the relationship between customer reviews and overall product ratings.

#### Steps:
1. **Data Cleaning** – Loaded the Amazon product dataset, inspected the schema, and handled missing or inconsistent values to prepare for analysis.
2. **Data Wrangling** – Standardized currency and percentage columns, engineered helper fields such as discount amount, price ratio, and review length, and created summary statistics for key variables.
3. **Data Visualization** – Built visualizations to explore pricing distributions, category performance, discount patterns, and how reviews and ratings relate to each other.
4. **Model Building** – Trained and evaluated baseline and Random Forest models to predict product ratings using features like price, discount percentage, review volume, and text sentiment
   
#### Result Summary:
The model shows that customer sentiment and engagement are more predictive of overall product ratings than pricing variables. The frequency of positive words like “good” and “excellent” strongly correlates with higher ratings, while negative words such as “doesn’t” lower them. Additionally, deeper discounts and higher review counts are linked to small boosts in rating, suggesting that social proof and perceived value influence consumer perception more than price itself.

The model achieves an R² of 0.29 which explains about a third of rating variation and highlights the emotional and social dimensions of consumer decision-making. The MAE suggest that predictions are on average 0.16 stars off, which is pretty good for a 1-5 rating scale.

