# Bike Sharing
> The main aim of this project is to build a multiple linear regression model for the prediction of demand for shared bikes and understand the factors on which the demand for these shared bikes depends. 


## Table of Contents
* [Problem Statement](#problem-statement)
* [Problem Solving Methodology](#problem-solving-methodology)
* [Conclusions](#conclusions)
* [Technologies Used](#technologies-used)


## Problem Statement
The company wants to understand the demand for shared bikes among the people after the quarantine situation ends across the nation due to Covid-19. They have planned this to prepare themselves to cater to the people's needs once the situation gets better all around and stand out from other service providers and make huge profits.

The company wants to understand the factors on which the demand for these shared bikes depends. Specifically, they want to understand the factors affecting the demand for these shared bikes in the American market. The company wants to know:

Which variables are significant in predicting the demand for shared bikes.

How well those variables describe the bike demands


## Problem Solving Methodology
* Data Sourcing & Understanding -
> Source the dataset which contains the complete data for all bookings made during the time period 2018 t0 2019. 
> Making use of the data dictionary and understanding the columns and their domain specific uses.
* Data Cleaning -
> Remove the unnecessary columns and map the categorical values with their actual values
* EDA -
> Create box plots of continuous variables, visualize categorical variable with target variable, visualize correlation between the variables using pair plots and heat map and visualize categorical variables with target variable w.r.t. year
* Data preparation fro modelling -
> Create dummy variables, split data into training and testing set, perform feature scaling
* Model Building -
> Use RFE to find top 15 variables and then use statsmodel api to build models and remove columns based on their VIF and p-values, finally build a linear regression model by sklearn using the columns selected from the statsmodel api models
* Model predictions and Residual Analysis -
> Make predictions on the training and testing set using the linear regression model and preform residual analysis to validate the assumptions of Linear Regression. The assumptions include normality of residuals, homoscedasticity and independence of residuals.
* Model Evaluation -
> Evaluate the model by chekcing the R-squared value for training and testing set 


## Conclusions
- The equation of best fitted line according to the model is

cnt = 1336.0415 + 1998.9114 * yr + 3576.6992 * temp - 1327.6736 * season_spring + 782.9887 * season_winter - 510.5783 * mnth_dec - 422.5030 * mnth_july + 496.0487 * mnth_mar - 692.638 * mnth_nov + 427.4597 * mnth_sep + 698.7583 * weathersit_clear - 1658.8462 * weathersit_light_snowrain

- The variables on which the demand of bikes depend are

1. Year
2. Temperature
3. Season (spring, winter)
4. Month (dec, july, march, nov, sep)
5. Weather situation (clear, light snow and rain)


## Technologies Used
- Numpy        - version 1.21.6
- Pandas       - version 1.3.5
- Seaborn      - version 0.11.2
- Matplotlib   - version 3.2.2
- Scipy        - version 1.7.3
- Sklearn      - version 1.0.2
- Statsmodels  - version 0.12.2
