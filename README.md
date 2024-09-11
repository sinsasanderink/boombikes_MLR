![BoomBikes](./boombikes.png)

# boombikes_MLR
Forecasting bike-sharing demand for BoomBikes, using MLR

# Bike Sharing Assignment
> Develop a multiple linear regression model to forecast post-COVID-19 demand for BoomBikes, a US-based bike-sharing service.


## Table of Contents
* [General Info](#general-information)
* [Libraries Used](#Libraries-used)
* [Reading & understanding data](#Reading-and-understanding-the-data)
* [Data cleaning](#data-cleaning)
* [EDA](#eda)
  * [Univariate Analysis](#Univariate_Analysis)
  * [Bivariate Analysis](#Bivariate_Analysis)
  * [Multivariate Analysis](#Multivariate_Analysis)
* [Data Preparation](#data-preparation)
* [Training the model](#training-the-model)
* [Residual analysis](#residual-analysis)
* [Model evaluation](#model-evaluation)
* [Conclusions](#conclusions)


## General Information

This project involves building a multiple linear regression model to predict the demand for BoomBikes. The goal is to identify significant factors influencing bike demand, enabling BoomBikes to make informed, data-driven decisions as they navigate post-pandemic challenges.

**Background:**

BoomBikes has experienced a significant revenue decline due to the COVID-19 pandemic. To recover and grow, the company seeks to understand the specific factors influencing bike demand in the American market. They aim to identify the variables that significantly predict bike demand and how well these variables describe overall demand. To support this analysis, they have gathered a comprehensive dataset containing daily bike rental data and various predictors, such as weather conditions and user behavior.

**Business Problem:**

The insight into which variables impact bike demand, and how well those variables describe the bike demands, is crucial for BoomBikes to plan and execute a business strategy that maximizes revenue, meets customer expectations, and ensures competitiveness in the bike-sharing market. By accurately modeling daily bike demands, BoomBikes aims to prepare for post-pandemic demand, differentiate itself from competitors, and accelerate its financial recovery.

**Dataset:**

The dataset used in this project is "day.csv," which includes daily bike rental data and various independent variables, such as weather conditions, season, and user behavior, that might affect bike-sharing demand.

## Libraries Used
- Python - version 3.8
- Pandas - version 1.2
- NumPy
- Matplotlib
- Seaborn
- scikit-learn - version 0.24
- statsmodels - version 0.12
- Warnings
- Calendar

## Reading & understanding data
- Load the data and get an understanding.

### Data Cleaning
* Remove unnecessary columns.
* Handle missing values and check for any outliers in the dataset.

### EDA (Exploratory Data Analysis)
#### Univariate Analysis
#### Bivariate Analysis
#### Multivariate Analysis

### Data Preparation
* Create dummy variables for categorical data.
* Scale numerical features for uniformity in the model.
* Split the data into training and testing sets.

### Training the Model
* Use Recursive Feature Elimination (RFE) for feature selection.
* Train the model using statsmodels' OLS (Ordinary Least Squares) method.
* Analyze model statistics such as coefficients, p-values, and R² scores.

### Residual Analysis
* Visualize residuals using QQ plots and histograms to assess the assumptions of normality and independence.
* Analyze error terms to check for homoscedasticity and other model assumptions.

### Model Evaluation
* Evaluate model performance using R² and Adjusted R² on both train and test sets.
* Compare predicted vs actual values using scatter plots.
* Interpret and conclude model performance and identify improvements.

## Conclusions
- The model, with a Train R² score of 82.4% and a Test R² score of 80.7%, effectively predicts bike rentals, showing minimal overfitting with an acceptable difference between the training and test set performance. The Adjusted R² values (Train: 82%, Test: 79.7%) confirm the model's reliability.

Key inferences:
* Temperature: Temperature is the strongest predictor of bike rentals. Rentals peak at moderate temperatures (11-13°C and 26-28°C), while extreme cold (below 7°C) or heat (over 32°C) reduces demand.
* Seasonal Impact: Fall and Summer drive the highest bike rentals, with September standing out as the peak month, while January & February are the months with the least demand. 
* Year-over-Year Growth: Bike rentals increased significantly from 2018 to 2019, reflecting strong growth in the second year.
* Weather: Sunny weather boosts rentals, while rainy conditions drastically reduce them.
* Windspeed and Humidity: Although both variables have a weaker overall impact, a too high or too low windspeed or humidity do reduce bike demand.

Recommendations:

* Temperature-Driven Campaigns: Focus promotions on moderate temperature ranges, where demand is highest.

* Seasonal Pricing Adjustments: Increase prices during Fall and Summer. Offer discounts or bundles during Winter and Spring to boost demand in off-peak seasons.

* Weather-Responsive Offers: Implement dynamic pricing—lower rates for rainy or windy days, premium rates on sunny days.

* Yearly Growth Campaigns: Leverage year-over-year growth by expanding marketing efforts and introducing summer add-ons like bicycle tours or special experiences.

* Weekend and Weekday Optimization: Use weekend offers and partner with companies to encourage weekday commuting, with discounts for employees.

* Strategic Partnerships: Collaborate with organizations to integrate bike rentals into daily commutes, promoting eco-friendly transport.

* Data-Driven Adjustments: Regularly update pricing, promotions, and inventory based on real-time data to stay agile and capture growth opportunities.
