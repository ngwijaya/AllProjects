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

### 2. Breast Cancer Coimbra Data Set Analysis
#### Description:
This notebook explores the Breast Cancer Coimbra Data Set, focusing on classification tasks using the k-Nearest Neighbors (kNN) algorithm. It investigates different distance metrics and weighting schemes to identify the best model parameters for predicting breast cancer classification.

#### Background:
The Breast Cancer Coimbra Data Set contains features derived from blood analysis that can be used to predict breast cancer status. Machine learning models like kNN can be applied to classify patients based on these features, aiding in early diagnosis or risk assessment.

#### Project Objective:
The objective of this project is to apply the kNN algorithm to classify breast cancer status using the provided dataset. This involves loading and exploring the data, splitting it into training and test sets, and then evaluating kNN performance with various configurations (Euclidean vs. Minkowski distance, uniform vs. distance weights) to find the optimal parameters (k and p values).

#### Steps:
1. **Load Dataset** – Loaded the dataR2.csv file into a pandas DataFrame and examined its structure and basic statistics.
2. **Exploratory Data Analysis** – Visualized feature distributions using a scatter matrix, colored by class, and divided the dataset into training and test sets based on classification labels.
3. **kNN Classification (Euclidean Metric, Uniform Weights)** – Trained a kNN model using Euclidean distance and uniform weights. Computed and plotted misclassification rates for a range of 'k' values to determine the best 'k'.
4. **kNN Classification (Minkowski Metric, Uniform Weights)** – Trained a kNN model using Minkowski distance and uniform weights. Performed a grid search over 'k' and 'p' values to identify the optimal (k, p) pair.
5. **kNN Classification (Minkowski Metric, Distance Weights)** – Trained a kNN model using Minkowski distance and 'distance' weights. Conducted another grid search over 'k' and 'p' values to find the optimal (k, p) pair for this configuration.
   
#### Result Summary:
With Euclidean distance and uniform weights, the most suitable k was found to be 46.
When using Minkowski distance with uniform weights, the optimal k was 52 and the optimal p was 1.
Using Minkowski distance with 'distance' weights, the optimal k was 12 and the optimal p was 1. Different configurations of the kNN algorithm (distance metric and weights) yielded varying optimal hyperparameters, highlighting the importance of thorough parameter tuning for predictive performance.

### 3. Loan Prediction Project
#### Description: 
This project analyzes a bank’s loan dataset to predict how much loan an applicant is eligible to take based on their background and financial profile. The dataset includes attributes such as dependents, education level, employment type, income, credit history, property area, and loan term, all of which are used to build predictive models that estimate loan amount.

#### Background: 
Without sufficient information indicating the willingness and ability of borrowers to return the loan borrowed, banks are unable to decide the appropriate amount to lend to borrowers.

#### Project Objective: 
Examine a set of data acquired from a bank to decide how much loan a borrower is eligible to take out based on the borrower's background. The data will be analyzed to explore existing trends and correlations between the dependent variable and the independent variables.

#### Steps:
1. **Data Wrangling** – Cleaned and transformed the dataset by handling missing values, encoding categorical variables, and standardizing numerical features for consistency.
2. **Exploratory Data Analysis (EDA)** – Visualized correlations between applicant information (income, dependents, credit history, etc.) and loan amount to identify key drivers of loan eligibility.
3. **Machine Learning** – Trained multiple regression models with different feature combinations and compared their performance using MAE (Mean Absolute Error), MSE (Mean Squared Error), and RMSE (Root Mean Squared Error).

#### Result Summary:
After comparing all models, Model 3—which includes Dependents, Education, Self-Employed, Applicant Income, Co-applicant Income, Credit History, Property Area, and Loan Amount Term—performed the best. It achieved the lowest MAE (indicating the smallest average prediction error) and competitive MSE and RMSE values. While Model 6 had slightly lower MSE and RMSE, Model 3 was chosen because MAE better reflects accuracy on real loan predictions by focusing on absolute error rather than squared deviations.

Overall, the project highlights how combining demographic and financial indicators can effectively predict loan amounts, supporting data-driven decision-making for fair and efficient lending processes.
