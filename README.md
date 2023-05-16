# Covid-Survival-Analysis

## Problem Definition

The SARSCoV-2 coronavirus-caused COVID-19 pandemic has presented many obstacles, including controlling its spread and minimizing its detrimental effects. Mutations in the virus cause new strains with increased transmission rates and lower vaccination efficacy. The B.1617 variant's recent discovery in India and other countries and the absence of treatment information have compounded matters. Using past and present data, quantitative forecasting can predict future trends. Therefore, the issue specification is to construct a forecasting model that can accurately anticipate the number of Covid-19 cases, fatalities, and recoveries for a particular day while taking into account the pandemic's evolving variants and mutations. Exploratory data analysis and visualizations to examine data metrics across regions/countries are also necessary to understand the pandemic's dynamics and build effective mitigation plans.

## Introduction
	The SARSCoV-2 coronavirus has resulted in the Covid-19 pandemic, an infectious respiratory disease that is exhibiting exponential growth. Challenges in the field, such as mitigating the spread and minimizing the negative consequences of this phenomenon, have emerged as significant areas of concern. The government's areas of concern Several nations, including India, have encountered or are presently undergoing a subsequent surge of this lethal virus.

		Several nations, including Germany, have encountered a third wave. The virus undergoes frequent mutations. On December 14th, 2020, the United Kingdom and Northern Ireland authorities announced the emergence of a novel variant, B.1.1.7, which exhibits a higher transmission rate compared to its predecessor and marginally diminishes the efficacy of the vaccine. The B.1.617 variant, commonly referred to as the double mutant strain, was first detected in India and is considered a significant contributor to the second wave of COVID-19 infections in the country. The B.1617 variant, also known as Delta Plus, represents the latest strain that has been identified.  The emergence of a second wave in India has been observed in various states, including Tamil Nadu and Punjab, among others. Additionally, a new variant has been identified in these regions. 
		Currently, medical professionals lack knowledge regarding the appropriate course of treatment for this particular variant.	Consequently, a definitive remedy for this ailment is currently unavailable. Forecasting is a quantitative technique that facilitates the process of anticipating future trends by utilizing historical and current data. 
		
## Data set Introduction
		For this project, we are using a Kaggle data set that contains multiple CSV files, each containing different information.
full_grouped.csv - Day to day country wise no. of cases (Has County/State/Province level data)
covid_19_clean_complete.csv - Day to day country wise no. of cases (Doesn't have County/State/Province level data)
country_wise_latest.csv - The latest country-level no. of cases
day_wise.csv - Day-wise no. of cases (Doesn't have country-level data)
usa_county_wise.csv - Day-to-day county level no. of cases,
worldometer_data.csv - Latest data from https://www.worldometers.info/

For training, the day-wise data set is used. 

Problem Solution using Machine Learning
	Several models such as linear regression, polynomial regression, SVM, and Holt's linear model These models were chosen for the following reasons.

Linear Regression: Linear regression is suitable for predicting COVID cases as it assumes a linear relationship between the dependent and independent variables. In the context of COVID, the dependent variable would be the number of cases, and the independent variable would be time. The linear regression model can help us understand the trend of COVID cases over time and whether they are increasing or decreasing.

Polynomial Regression: Polynomial regression is an extension of linear regression that can model more complex relationships between the dependent and independent variables. In the context of COVID, polynomial regression can help capture the non-linear trends in COVID cases and provide better predictions.

Support Vector Machines (SVM): SVM is a supervised machine learning algorithm that can be used for regression and classification tasks. In the context of COVID, SVM can help us identify the factors that affect the number of cases, such as population density, temperature, and humidity. SVM can also help us predict the number of cases based on these factors.

Holt's Linear Model: Holt's Linear Model is a time series forecasting method that can estimate trend value and slope using a weighted average of historical observations. In the context of COVID, Holt's linear model can help us understand the trend of COVID cases over time and make predictions based on this trend.

## Project Objectives
The primary goal of this project is to develop a robust predictive model that can accurately forecast the number of COVID-19 cases, deaths, and recovered cases for a given day. To achieve this objective, we will use time series data analysis techniques such as linear regression, polynomial regression, support vector machines (SVM), and Holt's linear model to model the data and generate forecasts.

In addition to building the predictive model, we also aim to perform exploratory data analysis (EDA) on the COVID-19 dataset. This will involve exploring the data to identify patterns, trends, and relationships between various features and outcomes. We will use different visualization techniques such as histograms, heatmaps, scatter plots, and line charts to analyze the data across different regions and countries.

Furthermore, this project seeks to evaluate the performance of the predictive model using appropriate metrics. These metrics will be used to compare the accuracy of the different models we will develop and to identify the most effective model for predicting COVID-19 cases, deaths, and recoveries.

Overall, the objective of this project is to develop an effective predictive model for COVID-19 using time series analysis techniques and perform thorough exploratory data analysis to gain insights into the trends and patterns of COVID-19 across different regions and countries.

## Analysis
Data Quality Checking
The data is robust, without any duplicates or overlaps. Some data sets have some numeric values, but they are in columns that are not used much in visualizations and model training, so they are not removed.
Since we are analyzing time series data whose values, like the number of cases and deaths in a country, are exponentially increasing, outliers are neglected.
Other than that, there are no other discrepancies in the data that need to be handled.
Exploratory Data Analysis- Visualizations 

Following Visualizations and analysis are gathered from the data.

A tree map showing confirmed cases over different countries.


From this, it was analysed that US and Brazil have the highest number of confirmed cases.

tree map showing confirmed cases over different countries.


US, Brazil and India have the highest number of active cases overall.

cases over time

Both the active and Confirmed cases are increasing rapidly and July 27th 2020 has the highest number of recorded cases according to the data.

Line plots show the trend of Deaths per 100 cases and Recovered per 100 cases.


April 24 and 30 2020 had the highest number of deaths /100 cases and the number is gradually decreasing over time.
March 8th 2020 had the highest recovered/ 100 cases and the number is gradually increasing over time and again reached a peak value on July 26th 2020.

Bar plot of top 10 countries with highest confirmed cases per 1 million population

Eastern Mediterranean countries have the highest case per 1 million population and Qatar country has the highest number of cases per 1 million population.

Bar plot of top 10 countries with highest Total tests

USA has the highest number of total tests

Percentage of deaths for each day for each country (china 80%, us 17%, India 2%,....)


we can observe that china contributed over 90% of confirmed cases and deaths initially and later the cases and deaths increased in other countries like USA, France, Brazil.
Visualising different metrics over different regions and countries

USA had the most covid confirmed cases overall with 4.2 million confirmed cases

USA had the most Deaths overall after Brazil, China had the most number of confirmed cases from the start and we can observe the exponential increase in the number of confirmed cases in all other regions over time from this animation.


## Model Training

Following models are trained and compared in this project
Linear Regression predicts COVID cases because it assumes a linear connection between the dependent and independent variables. Time is the independent variable while COVID cases are the dependent variable. The linear regression model can show how COVID cases are changing over time.

Polynomial Regression, This linear regression extension can represent more complex dependent-independent connections. Polynomial regression can improve COVID forecasts by capturing non-linear trends.

SVM is a supervised machine-learning technique for regression and classification. SVM can identify COVID risk factors such as population density, temperature, and humidity. SVM can forecast case numbers based on these characteristics.

Holt's Linear Model, This weighted average of historical observations time series forecasting method estimates trend value and slope. Holt's Linear Model can assist us predict COVID trends.

The data is split into train and test set with a ratio of 75 and 25 respectively.

## Results

Out of all the models both Polynomial regression and Holts linear regression performed the best.
Following are some Visualizations that show the actual and predicted results.


Model Name
RMSE Error
Polynomial Regression
5.63 %
SVM
23.87 %
Holts Linear Model
12.65 %



 Polynomial Regression: This is a plot where the number of confirmed cases and predicted confirmed cases are plotted over time. we can see that the prediction line is following the actual line properly but overshooting a bit.

SVM:  This is a plot where the number of confirmed cases and predicted confirmed cases from SVM are plotted over time. the SVM is not performing well as there is a lot of difference between the actual and predicted values.


Holts Linear Regression: This Visualization shows the confirmed cases from the Training data (blue points), Validation data(red points) and prediction data(green points), we can observe that the model is performing well as the prediction is following the validation values only undershooting a bit. 

Discussion
The pandemic caused by COVID-19 has presented substantial obstacles on a global scale, and preventing its further spread while reducing the damage it would cause has emerged as a prominent issue of concern. Things have become even more complicated as a result of the appearance of new varieties, such as B.1617 in India. Due to the lack of particular treatment information for this variant, it has become vital to employ both historical and current data in order to construct prediction models that accurately estimate the number of COVID-19 cases, deaths, and recoveries while also taking into consideration the pandemic's developing variants and mutations. These models must be able to reliably forecast the number of COVID-19 cases, deaths, and recoveries.

Using methods of time series analysis such as linear regression, polynomial regression, support vector machines (SVM), and Holt's linear model, the purpose of this project is to find a solution to this problem by creating a reliable predictive model that can accurately forecast the number of COVID-19 cases, deaths, and recoveries that will occur on any given day. Exploratory data analysis will also be performed on the COVID-19 dataset in order to identify patterns, trends, and relationships between various features and outcomes. A number of different visualization techniques, such as histograms, heatmaps, scatter plots, and line charts, will be utilized in order to analyze the data across a variety of countries and regions.
