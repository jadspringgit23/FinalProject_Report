# FinalProject_Report

This paper emphasizes the use of modeling techniques suitable for analyzing eCommerce data, which primarily consists of categorical variables. Initially, we conducted exploratory data analysis (EDA) on the dataset without transformation. Subsequently, we applied EDA to the dataset after performing dummy variable transformations. The dataset, sourced from Kaggle, is titled 'Amazon Sales Report' and pertains to online sales from India. The primary objective of this study is to recommend the most suitable modeling technique for such data. Specifically, we aim to compare two models: linear regression and logistic regression. In the linear regression model, 'Amount' serves as the dependent variable, predicted by variables such as Qty, Fulfilment, ship-postal-code, and category. Conversely, in the logistic regression model, the binary dependent variable 'FulfilmentB' is predicted by Qty, Amount, ship-postal-code, and category.

# Executive Summary

This paper emphasizes the use of modeling techniques suitable for analyzing eCommerce data from India using the Amazon Sales Report of 2022, which dataset originally contained 128,975 observations and 24 variables ( index, Order ID , Date , Status  , Fulfilment,  Sales Channel, ship-service-level , Style , SKU, Category, Size, ASIN,  Courier Status, Qty, currency, Amount, ship-city, ship-state, ship-postal-code, ship-country, promotion-ids, B2B, fulfilled-by, and Unnamed:22) primarily consists of categorical variables (19). Initially, we conducted exploratory data analysis (EDA) on the dataset without transformation. Subsequently, we applied EDA to the dataset after performing dummy variable transformations. The dataset, sourced from Kaggle, is titled 'Amazon Sales Report' and pertains to online sales from India. The primary objective of this study is to recommend the most suitable modeling technique for such data. Specifically, we aim to compare four models: Multi linear Regression,  Logistic Regression, Random Forest, and Decision Tree models . In the multi linear regression model, 'Amount' serves as the dependent variable, predicted by variables such as Index, Status, Fulfilment, Category,  Size, Qty, and ship-postal-code. Conversely, in the logistic regression , random forest, and decision tree models, the binary dependent variable 'Fulfilment' is predicted by  Index, Status, Category,  Size, Qty, Amount, and ship-postal-code.

# Introduction
The growth of the ecommerce industry is closely tied to online selling and internet availability, which remain pivotal factors globally. Despite significant efforts to improve internet accessibility worldwide, disparities persist between developed and developing nations. Developed countries typically boast internet penetration rates exceeding 80%, whereas in poorer countries, this figure may be less than 10%. As of 2022, India has achieved a commendable internet penetration rate of over 60% for its population exceeding 1.4 billion .

The potential for online selling in India is evident, as highlighted by Forbes Advisor's report on "E-Commerce Statistics for India in 2024". According to their findings, India's ecommerce sector is projected to grow to INR 4,416.68 billion by 2024, with an annual growth rate of 11.45%, reaching INR 7,591.94 billion by 2029. By 2029, the number of ecommerce users in India is expected to reach 501.6 million, with user penetration increasing from 22.1% in 2024 to 34.0% by 2029 .

Despite India's lower internet penetration compared to developed nations, its substantial online user base forecasted for 2024 underscores its potential as a lucrative market. This study aims to leverage predictive modeling, specifically comparing multi linear regression, logistic regression, random forest, and decision tree models. The objective is to determine which of these models can provide the most insightful analysis of the dataset, facilitating informed decision-making for product development and market strategy implementation.

# Data Collection, Preparation, and Visualization
## Data Colection
The data utilized in this study were sourced from Kaggle and are described as follows: the 19 character variables listed in table1,  4 numerical variables, and  1 Boolean variable. 
Table1: List of the character variables and their levels
	![image](https://github.com/jadspringgit23/FinalProject_Report/assets/155911452/c511a698-52e5-489e-b98d-4312c37de74b)

	












