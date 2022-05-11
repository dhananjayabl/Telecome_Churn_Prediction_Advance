# Project Name
> Telecom Churn Prediction


## Table of Contents
* [General Info](#general-information)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)
* [Acknowledgements](#acknowledgements)

<!-- You can include any other section that is pertinent to your problem -->

## General Information

**Overview**
Telecome is a very competitive market, exit barriers for customer are low. Loyalty depends on user experince and attractive offers. Industry experiences an average of 15-25% annual churn rate. Given the fact that it costs 5-10 times more to acquire a new customer than to retain an existing one, customer retention has now become even more important than customer acquisition. Retaining high profitable customers is the number one business goal.
 

**Problem Statement**
To reduce customer churn, telecom companies need to predict which customers are at high risk of churn. 
- The goal is to build a predictive model that can predict the chrun propensity for a customer accurately.
- Identify key features that indicates the customer behaviour to churn

**Approach**

- Data understanding from data dictionary 
- Loading the selecting the relevent data for analysis
- Data sanity check - check for duplicates, cardinality, format mismatch and missing values
- Data cleaning - Use of appropriate strategy for imputing missing values and extreme/outlier values
- EDA - Univariate, Segmented and Bi-variate analysis with Visualization
- Feature Engineering - Using the termporal behavioural data creating new features to capture the change in behaviours like Rate of Change and Direction of Change, extrating features from date-time features
- Data Preparation - Scaling of data
- Model development experiments - 2 modeling approaches 
    - Model development to understand the important features wrt target variable
        - Obtain Top K Feature Importance using Random Forest Mode
        - Use Logistic Regression to develop explinability using Feature Importance 

    - Model development for accurate prediction
        - PCA is used for dimentionality reduction 
        - Various algorithms will be fitted - Logistic Regression, Random Forest, XGBoost, LightGBM and Ensemble with Hyper-paramter Tuning 
- Conclusion

<!-- You don't have to answer all the questions - just the ones relevant to your project. -->

## Conclusions
 - With good feature engineering of the temporal data the model prediction can be further imporved
 - Using Principal Componets for prediction has not resulted in higher prediction performance of the model even after hyper-parameter tuning compared to using raw features as is.
 - As for the explainablity concerned;
     - There is a clear pattern across last 3 months (month 6, 7, and 8) with respect to the call usage, data usage and recharge behaviour of the customer with higher probaility to churn
     - The customer with higher probability to churn exhibit following behaviour as per the data;
         - have reduced recharge amount and total recharge from month 6 to month 8
         - The Average Revenue Per User has significant drop from month 6 to 8
         - The customer with higher median Roaming calls (both incoming and outgoing) MOU has higher tendency to churn
         - Total outgoing call MOU also has significant drop from month 6 to 8
         - Customer who are with network for longer than 1000 days has low tendancy to churn
- These features can be a good indicator for probability to churn

- **Recommendations**

    - Offering discounts on Roaming Charges or special Roaming packages may prevent customer have high roaming usage
    - Offering special discounts on Month 7 and 8 on every recharge could help retaining the customer 
    - Offering special packages to customer who are less than 1000 days old 

<!-- You don't have to answer all the questions - just the ones relevant to your project. -->


## Technologies Used
- python - 3.10.1
- pandas - 1.4.2
- numpy - 1.21.5
- matplotlib - 3.5.1
- seaborn - 0.11.2
- scikit-learn - 1.0.2
- scipy - 1.7.3
- statmodels - 0.13.1
- imbalanced-learn - 0.9.0
- xgboost - 2.0
- lightgbm - 3.3.1

<!-- As the libraries versions keep on changing, it is recommended to mention the version of library used in this project -->

## Acknowledgements
Give credit here.
- This project was inspired by...
- References if any...
- This project was based on [this tutorial](https://www.example.com).


## Contact
Created by [@githubusername] - feel free to contact me!


<!-- Optional -->
<!-- ## License -->
<!-- This project is open source and available under the [... License](). -->

<!-- You don't have to include all sections - just the one's relevant to your project -->