# M5 Forecasting Project

## Project Overview
The M5 Forecasting project aims to develop accurate forecasting models to predict future sales of products sold by Walmart stores in the USA. This involves predicting sales at various levels of aggregation, from individual products to categories, stores, and regions. The project leverages historical sales data, calendar information, and price data to build and evaluate forecasting models.

## Table of Contents
1. [Introduction](#introduction)
2. [Dataset Description](#dataset-description)
3. [Data Preprocessing](#data-preprocessing)
4. [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
5. [Feature Engineering](#feature-engineering)
6. [Modelling](#modelling)
7. [Code Files](#code-files)

## Introduction
The objective of the M5 forecasting competition is to predict daily sales for various products sold by Walmart stores in California, Texas, and Wisconsin over a 28-day period. Accurate forecasting at different aggregation levels is crucial for effective inventory management and supply chain optimization.

## Dataset Description
The dataset consists of the following components:
- **calendar**: Provides information on the sale dates for products.
- **sell_prices**: Contains pricing details of products sold by each store on specific dates.
- **sales_train_validation**: Extends the sales data to include days 1 through 1913 for public leaderboard evaluation.
- **sales_train_evaluation**: Extends the sales data to include days 1 through 1941.

### Data Considered for Analysis
- **States**: California (CA 1, CA 2, CA 3, CA 4), Texas (TX 1, TX 2, TX 3), Wisconsin (WI 1, WI 2, WI 3)
- **Categories**: Hobbies (Hobbies 1, Hobbies 2), Food (Food 1, Food 2, Food 3), Household (Household 1, Household 2)

## Data Preprocessing
Data preprocessing involves the following steps:
1. **Melting Dataframes**: Transforming columns that represent days into rows for each unique item.
2. **Merging Dataframes**: Combining calendar, selling price, and training datasets into a single dataframe for EDA and modeling.
3. **Label Encoding**: Converting categorical variables into numeric variables for modeling.

## Exploratory Data Analysis (EDA)
Key insights from the EDA include:
- **Sales Trends**: California exhibits the highest overall sales, followed by Texas and Wisconsin.
- **Department Sales**: The Food department has the highest sales, with notable peaks in specific months and states.
- **Price Analysis**: Hobbies_1 has the highest mean price, while Food_3 has the lowest.

## Feature Engineering
Feature engineering includes creating features to capture weekly, seasonal, and yearly sales patterns, such as:
- **Week Number**: Tracks weekly sales patterns.
- **Season**: Accounts for seasonal fluctuations.
- **Quarter Start/End Flags**: Highlights quarterly sales trends.
- **Month Start/End Flags**: Captures monthly sales dynamics.
- **Year Start/End Flags**: Indicates annual sales cycles.
- **Rolling Mean and Standard Deviation for Sales**: Smoothens sales data for trend analysis.
- **Lagged Sales**: Incorporates historical sales for forecasting.

## Modelling
The modeling approach utilizes Long Short-Term Memory (LSTM) networks. Key components include:
- **Input Layers**: Handling different types of features.
- **Embedding Layers**: Transforming categorical inputs into dense representations.
- **LSTM Layers**: Capturing temporal dependencies in the data.
- **Flatten Layers**: Reshaping LSTM outputs.
- **Concatenation and Batch Normalization**: Stabilizing and accelerating learning.
- **Dense Layers**: Learning non-linear combinations of inputs.

## Code Files
The project includes several Jupyter Notebooks and a presentation file:

1. **M5_Data_Prep.ipynb**:
   - This notebook covers data preprocessing steps, including melting dataframes, merging dataframes, and label encoding.
   - Key functions include data transformation, merging different data sources, and preparing the final dataset for analysis.

2. **M5_EDA.ipynb**:
   - This notebook contains exploratory data analysis, providing insights into sales trends, price analysis, and sales distribution across different categories and states.
   - Key visualizations and statistical analyses are presented to understand the underlying patterns in the data.

3. **M5_LSTM_Model.ipynb**:
   - This notebook focuses on building and training the LSTM model.
   - It includes data preparation for modeling, defining the LSTM architecture, training the model, and evaluating its performance using the WRMSSE metric.

4. **ML Final Project Presentation - Yukti Sanjay Jain, Karan Karnik 1.pdf**:
   - This presentation provides an overview of the project, including the problem statement, dataset description, preprocessing steps, EDA, feature engineering, modeling approach, results, and conclusions.
   - It serves as a comprehensive summary of the project for presentation purposes.

## Thank You
Thank you for your interest in the M5 Forecasting project. For further information or inquiries, please refer to the project documentation and the references listed above.
