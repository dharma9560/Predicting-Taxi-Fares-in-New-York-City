# **Predicting Taxi Fares in New York City**

## **Overview**
The objective of this project was to build a regression model capable of predicting taxi fares in New York City based on historical trip data. The dataset includes trips taken by yellow taxis during 2017. Four machine learning models were developed to predict the fare amount: Multiple Linear Regression, Single Tuned Decision Tree, Random Forest, and XGBoost. The best-performing model was the Random Forest, which achieved an **R² score of 0.8782** and a **Mean Absolute Error (MAE) score of $2.17** on the test dataset. The most influential factors in predicting taxi fares were trip duration, distance traveled, and whether the ride occurred during rush hour.

## **Data Understanding**
The dataset (`2017_Yellow_Taxi_Trip_Data.csv`) used in this project was sourced from the New York City Taxi and Limousine Commission (TLC), made available through [NYC.gov](https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page). The data consists of approximately 22,000 unique trips and includes 18 features. Key features include:

* Trip Duration: The duration of the taxi ride.
* Distance: The distance traveled during the trip.
* Vendor ID: The vendor providing the taxi service.
* Toll Amount: Any toll fees charged during the trip.
* Payment Type: The method of payment for the trip (e.g., cash, credit card).
* Rush Hour: An engineered feature indicating whether the ride occurred during NYC’s peak traffic hours.

Refer to `meta_data_2017_Yellow_Taxi_Trip_Data.txt` for detailed meta data.

Redundant columns were dropped, and all features were reformatted into the correct data types. A significant challenge was multicollinearity, particularly between the trip duration and distance, which are highly correlated.

## **Modeling and Evaluation**
Four regression models were trained on the data:

* Multiple Linear Regression
* Single Tuned Decision Tree
* Random Forest
* XGBoost

To evaluate model performance, the dataset is splitted into training, validation, and test sets. Models were evaluated using the R² score (coefficient of determination) and Mean Squared Error (MSE).

## **Key Steps**
1. **EDA and Data Preprocessing:** The data was analyzed, cleaned, and necessary feature engineering was performed.
2. **Model Training:** Different models were trained using the preprocessed data.
3. **Evaluation:** The models were evaluated on a validation dataset and using R² as the primary metrics.
4. **Prediction:** The top-performing model was used to make predictions on the test dataset.

**Metrics:**

**R² score:** Indicates the proportion of variance in the target variable (taxi fare) explained by the model.

**MAE:** Measures the average magnitude of the errors between predicted and actual values.

**MSE:** Measures the average squared difference between the predicted and actual values. A lower MSE indicates better predictive accuracy.

## **Results**

Following are the performance scores on validation dataset.

|    | Model Name                   |     R2 |    MAE |     MSE |
|---:|:-----------------------------|-------:|-------:|--------:|
|  0 | Random Forest                | 0.8828 | 2.1654 | 12.8813 |
|  1 | XGBoost                      | 0.8801 | 2.1102 | 13.1776 |
|  2 | Decision Tree                | 0.8798 | 2.2424 | 13.2102 |
|  3 | Multiple Linear Regression_2 | 0.8781 | 2.0994 | 13.395  |
|  4 | Multiple Linear Regression_1 | 0.8781 | 2.1012 | 13.3994 |

## **Best Model Performance**
Random Forest was the best-performing model, achieving an R² score of 0.88, MAE score of $2.17, and MSE of 12.88 on the validation set. When evaluated on the test set, it produced an **R² score of 0.88** and an **MAE of \$2.17**.

## **Conclusion**
The Random Forest model showed strong performance in predicting taxi fares with reasonably accurate results. However, due to the high correlation between duration and distance, drawing precise statistical inferences from this model is challenging. To address this issue in future iterations, additional feature engineering can be applied to reduce multicollinearity, potentially improving model interpretability and performance.
