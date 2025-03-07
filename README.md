# **Predicting Taxi Fares in New York City**

## **Overview**
The objective of this project was to build a regression model capable of predicting taxi fares in New York City based on historical trip data. The dataset includes trips taken by yellow taxis during 2017. Four machine learning models were developed to predict the fare amount: Multiple Linear Regression, Single Tuned Decision Tree, Random Forest, and XGBoost. The best-performing model was the Random Forest, which achieved an R² score of 0.8782 and a Mean Squared Error (MSE) score of 13.2447 on the test dataset. The most influential factors in predicting taxi fares were trip duration, distance traveled, and whether the ride occurred during rush hour.

## **Data Understanding**
The dataset used in this project was sourced from the New York City Taxi and Limousine Commission (TLC), made available through [NYC.gov](https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page). The data consists of approximately 22,000 unique trips and includes 18 features. Key features include:

* Trip Duration: The duration of the taxi ride.
* Distance: The distance traveled during the trip.
* Vendor ID: The vendor providing the taxi service.
* Toll Amount: Any toll fees charged during the trip.
* Payment Type: The method of payment for the trip (e.g., cash, credit card).
* Rush Hour: An engineered feature indicating whether the ride occurred during NYC’s peak traffic hours.

Redundant columns were dropped, and all features were reformatted into the correct data types. A significant challenge was multicollinearity, particularly between the trip duration and distance, which are highly correlated.

## **Modeling and Evaluation**
Four machine learning models were trained on the data:

* Multiple Linear Regression
* Single Tuned Decision Tree
* Random Forest
* XGBoost

To evaluate model performance, the dataset is splitted into training, validation, and test sets. Models were evaluated using the R² score (coefficient of determination) and Mean Squared Error (MSE).

**Key Evaluation Metrics:**

**R² score:** Indicates the proportion of variance in the target variable (taxi fare) explained by the model.

**MSE:** Measures the average squared difference between the predicted and actual values. A lower MSE indicates better predictive accuracy.

**Best Model Performance:**
Random Forest was the best-performing model, achieving an R² score of 0.8828 and an MSE of 12.8813 on the validation set. When tested on the final test set, it produced an R² score of 0.8782 and an MSE of 13.2447.

## **Conclusion**
The Random Forest model showed strong performance in predicting taxi fares with reasonably accurate results. However, due to the high correlation between duration and distance, drawing precise statistical inferences from this model is challenging. To address this issue in future iterations, additional feature engineering can be applied to reduce multicollinearity, potentially improving model interpretability and performance.
