# Analyzing Model Performance of the online selling from India:  Case study on Amazon Sales Report 2022 

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

	

## Data Preparation

The original dataset 'AmazonSale' initially consisted of 24 variables and 128,975 observations, labeled as data11. Upon inspection for missing values using the function (data11.dropna()), the dataset was reduced to 19,379 observations while retaining the same number of variables. Before conducting exploratory data analysis, we removed unnecessary variables pertinent to online selling in India. Variables such as currency, ship-state, ship-city, Order Id, Date, Style, SKU, ASIN, and promotion-ids were dropped due to issues with creating dummy variables and memory constraints, especially those with levels exceeding 90. Additionally, variables like Sales channel, Courier Status, ship-service-level, fulfilled-by, and Unnamed were irrelevant to the study's objectives and were also dropped. It's important to note that the variable "Sales Channel" presented difficulties in dropping using the function and was consequently removed using Excel, resulting in data11 having 19,379 observations with 23 variables. Following the removal of unused variables, the dataset was left with 19,379 observations and 8 variables. Before proceeding with dummy variable transformation, we converted the content of the variable "Fulfilment" to numeric values (Amazon to 1, Merchant to 0) since it served as one of the dependent variables for logistic regression, random forest, and decision tree tests. 

## Data Visualization

![image](https://github.com/jadspringgit23/FinalProject_Report/assets/155911452/bba94725-0562-4954-b51c-bda372ffe06f)
![image](https://github.com/jadspringgit23/FinalProject_Report/assets/155911452/b93efe82-32d9-49b0-9c89-237d13ded47b)
![image](https://github.com/jadspringgit23/FinalProject_Report/assets/155911452/51b88e02-6703-47a4-a38f-832829a928ed)
![image](https://github.com/jadspringgit23/FinalProject_Report/assets/155911452/94bf2816-fa75-487c-98c0-83b1d48bf8db)
![image](https://github.com/jadspringgit23/FinalProject_Report/assets/155911452/bd2c03fd-baa0-4b75-b772-beaaffa19e52)
![image](https://github.com/jadspringgit23/FinalProject_Report/assets/155911452/b00dd030-665c-44b6-8428-e9dc1985d8fb)
![image](https://github.com/jadspringgit23/FinalProject_Report/assets/155911452/72d37ff5-737b-4b2a-9162-ef6c3d368a98)

# Methodology

In this study, the data was divided into a 70% training set and a 30% test set for all four models, with a distinction in the dependent variable used. The multi linear model predicted 'Amount' as the dependent variable, while 'FulfilmentB', a dummy variable created from 'Fulfilment' (labeled as Fulfilment: Amazon and Fulfilment: Merchant), was used in logistic regression, random forest, and decision tree models. For the multi linear model, 'Amount' was predicted using predictors such as Index, Status, Fulfilment, Category, Size, Qty, and ship-postal-code.  Conversely, the logistic regression, random forest, and decision tree models predicted 'FulfilmentB' as the dependent variable. The predictors for these models included Index, Status, Category, Size, Qty, Amount, and ship-postal-code. This approach allowed us to analyze and compare the performance of different models in predicting outcomes relevant to online selling in India. Furthermore, using "Amount" as the dependent variable allows us to gain a better understanding of profitability trends in online selling in India, aiding in making informed business implementation decisions. Similarly, selecting "Fulfilment" as another dependent variable enables us to assess whether products fulfilled by Amazon or Merchant are more likely to be returned or canceled. This analysis provides valuable insights into operational efficiency and customer satisfaction within the ecommerce sector.

# Modeling

Modeling involves translating conceptual ideas into a quantifiable framework with the goal of establishing a general rule to explain a phenomenon. Models serve various purposes, from elucidating complex data to proposing hypotheses. In scientific contexts, models are often developed to predict outcomes based on interactions within cycles of data. As stated on sciencelearn.com, scientists use these models to anticipate future scenarios. In our study, the response variables of interest are "Amount," modeled using multiple linear regression with 7 predictors, and "FulfilmentB," utilized in logistic regression, random forest, and decision tree models with the same set of predictors. Mathematically, the models are described in this following:

Model1     :     Amount :  Index, Status, Fulfilment, Category,  Size, Qty, and ship-postal-code
Model2,3& 4:     FulfilmentB: Index, Status, Amount, Category,  Size, Qty, and ship-postal-code

In this section four model were tested in occurrence: Multi Linear Regression, Logistic Regression, Random Forest, and Decision Tree with ( model Entropy with and without max depth 3, Gini with and without max depth 3) adding to their respective confusion matrix, except for the Multi Linear model one. The R-squared coefficient for the Multi Linear model indicates that the model has poorly predicted the variation in the dataset, with an R-squared of 42%, suggesting that more work is needed to improve its predictive power. However, the model exhibits acceptable independence of errors, as indicated by a Durbin-Watson statistic of 1.92. Conveesely, the Logistic Regression model achieves an R-squared of 73.70%, which was a huge improvement comparing to the previous model. Therefore, its confusion matrix reveals that for the class FulfilmentB: Amazon = 1: True Positive: 6907 out of 9382 predictions, which corresponds to 74% While for the class FulfilmentB: Merchant = 0 % : False Negative: 2475 out of 9382 predictions, which accounts for 26%. However, there were no instances of True Negative or False Positive predictions recorded in the matrix, both totaling 0 out of 9382 predicted.

In regards of the Random Forest, two tests were conducted, that is, Random Forest with no max d with max depth 3. The results show that R-squared  dropped from 100% to 73.70% when limiting the maximum depth to 3. But Random Forest model still demonstrates a significant improvement compared to the Logistic Regression model. As evidenced by the results from its confusion matrix below:
The confusion matrix from the Random Forest demonstrates a clearer understanding of the data's classification. Unlike the Logistic Regression model, which showed an unbalanced confusion matrix, this model shows a more balanced and accurate classification. For example, the confusion matrix reveals that for the class FulfilmentB: Amazon = 1:

- True Positive 4995  out of 6805 predictions, which corresponds to 73%
- False Negative: 1810 out of 6805  predictions, which corresponds to 27%

While for the class FulfilmentB: Merchant = 0.
- True  Negative 197 out 701 predictions, which accounts for 28%
- False Positive: 504 out of 701 predictions, which accounts for 72%.

When it comes to the Decision Tree model, the R-squared values for the four models did not indicate any improvement compared to the Random Forest model, as their values were similar. Similarly, those from their decision matrix follow the same trend, except when using entropy and Gini with a depth of 3, where they yield results similar to the Logistic Regression in terms of unbalanced predictions. Based on these results, both the Random Forest and the Decision Tree (using entropy and Gini) seem to be suitable for the data. To determine which model is more advantageous for decision-making, the receiver Operating Characteristic Curve ( ROC) was used for further analysis. After we examined the ROC, the models showed scores ranging between 0.5 to 0.6, with the Decision Tree using the Gini model achieving the highest score of 0.54.core of 0.54, see the graph below for further details.

  ![image](https://github.com/jadspringgit23/FinalProject_Report/assets/155911452/3f41b910-f788-47b5-8578-1ae83a27a80d)




# Evaluation and Conclusion

Four models were evaluated on the dataset. The multilinear model showed less promising results with an R-squared of 42% and an R-score of less than 1%, indicating it is not a good fit for the dataset. This model was used solely for pre-testing, recognizing that its use of continuous variables could pose issues for Logistic Regression, which typically requires a binary dependent variable. Consequently, this model cannot be considered or included in this study. Therefore, the most convincing revelation is that this dataset is not suitable for multilinear regression analysis. As for determining which model performs better than another, it ultimately remains at the discretion of the reader, given that the results for both Random Forest and Decision Tree models are quite similar. For instance, the ROC score for the Decision Tree is 0.54, whereas it is 0.51 for the Random Forest. Similarly, the specificity is 28% for the Random Forest and 27% for the Decision Tree. From a statistical standpoint, however, the Random Forest holds a slight edge due to its F1-score exceeding 80%. This suggests that the Random Forest model can achieve high precision and recall simultaneously when predicting Amazon Sales status. Indeed, both Random Forest and Decision Tree models appear suitable for assessing this type of dataset.Overall, the study's results did not provide undeniable evidence favoring one model over another, indicating there is room for improvement in future analysis for this type of dataset.












