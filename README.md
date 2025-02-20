# **Predicting Taxi Fares in New York City**

## **Overview**
The goal of this project was to create a regression model to predict the taxi fares before the ride, based on data gathered. This project utilized yellow taxi trips taken in New York City during 2017. Four different models were developed: Multiple Linear Regression, Single Tuned Decision Tree, Random Forest, and XGBoost. The best performing model was Multiple Linear Regression, achieving an R² score of 0.8682 and an MSE score of 14.3312 on the test data. According to the model, the most influential factors in predicting the fare amount were duration, distance, and rush hour.

## **Data Understanding**
The NYC Taxi and Limousine Commission data came from [NYC.gov](https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page). The data consisted of approximately 22k unique trips and 18 features. The features included information on trip duration and destination, vendor used, toll information, and payment type. In connection to this, a feature was engineered to represent if a ride was taken during rush hour or not. Multiple redundant columns were dropped and reformatted into the proper data type.  

## **Modeling and Evaluation**
Four different models were developed: Multiple Linear Regression, Single Tuned Decision Tree, Random Forest, and XGBoost. The models were evaluated on a separate validation set which was randomly sampled from the main dataset. The best performing model was Multiple Linear Regression, achieving an R² score of 0.8770 and an MSE score of 13.6283 on the validation set. This model was then used to predict on the test set, achieving an R² score of 0.8682 and an MSE score of 14.3312.

Performance scores on validation data
| Model Name               | R²   | MAE  | MSE   |
|:------------------------:|:----:|:----:|:-----:|
|Multiple Linear Regression|0.8770|2.1159|13.6283|
|Random Forest             |0.8769|2.1798|13.6341|
|XGBoost                   |0.8758|2.1088|13.7602|
|Single Tuned Decision Tree|0.8725|2.2784|14.1245|

## **Conclusion**
Based on the evaluation metrics, the model is expected to make fairly accurate predictions. However, due to the high correlation between duration and distance, drawing precise statistical inferences from this model is challenging. In the future, further feature engineering can be done to mitigate the issue of multicollinearity.
