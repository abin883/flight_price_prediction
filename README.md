# Flight Price Prediction Project

## Overview
This project involves building a machine learning model to predict flight ticket prices based on various features such as airline, route, duration, and additional information. The dataset combines train and test data with necessary feature engineering and encoding to achieve high model performance.

## Dataset
The dataset includes flight details such as:
- **Airline**: The airline operating the flight.
- **Source**: The starting location of the flight.
- **Destination**: The destination location of the flight.
- **Route**: The path taken by the flight (intermediate stops).
- **Duration**: Total flight duration in hours and minutes.
- **Total_Stops**: Number of stops in the journey.
- **Additional_Info**: Other details about the flight.

## Feature Engineering
- Converted **Duration** to **Total Duration in Minutes**.
- Created **Route_Type** based on source-destination pairs.
- Generated **Route_Frequency** to indicate how common each route is.
- Handled missing values appropriately.
- Encoded categorical variables using label encoding and frequency encoding.

## Model Training
- Split the combined dataset into train and test sets based on the presence of the **Price** column.
- Used Random Forest Regressor for modeling.
- Performed hyperparameter tuning for optimal performance.

## Model Evaluation
- **Mean Absolute Error (MAE):** 679.99
- **R² Score:** 0.883

## Results
The model shows strong predictive power with an R² score of 0.883, indicating that 88.3% of the variance in flight prices is explained by the features.

## Files in Repository
- **flight_price_model.joblib**: Saved trained model.
- **final_submission.csv**: Final predictions on the test set.
- **flight_price_notebook.ipynb**: Jupyter notebook containing EDA, feature engineering, model training, and evaluation.

## How to Use
1. Clone the repository.
2. Load the saved model using `joblib.load()`.
3. Pass new flight data to the model for predictions.

```python
import joblib
model = joblib.load('flight_price_model.joblib')
new_data = [[...]]  # Replace with new input data
prediction = model.predict(new_data)
print(f'Predicted Price: {prediction}')
```

## Conclusion
The project demonstrates effective use of feature engineering and machine learning to predict flight prices. Future improvements could include trying other regression models and addressing outliers to enhance performance further.

