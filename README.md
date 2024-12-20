# Rusty_Bargain_Car_Value_ML_Model
Rusty Bargain has made a new app to attract new customers that will determine the market value for your vehicle. 

## Introduction

Rusty Bargain used car sales service is developing an app to attract new customers. In that app, you can quickly find out the market value of your car. We need to build the model to determine the value. 

Rusty Bargain is interested in:

- the quality of the prediction
- the speed of the prediction
- the time required for training

## Data Description

Features

- DateCrawled — date profile was downloaded from the database
- VehicleType — vehicle body type
- RegistrationYear — vehicle registration year
- Gearbox — gearbox type
- Power — power (hp)
- Model — vehicle model
- Mileage — mileage (measured in km due to dataset's regional specifics)
- RegistrationMonth — vehicle registration month
- FuelType — fuel type
- Brand — vehicle brand
- NotRepaired — vehicle repaired or not
- DateCreated — date of profile creation
- NumberOfPictures — number of vehicle pictures
- PostalCode — postal code of profile owner (user)
- LastSeen — date of the last activity of the user

Target

- Price — price (Euro)

## Conclusion

**Prediction Accuracy (RMSE):**

- The CatBoost model has the lowest RMSE (1516.65), followed closely by Random Forest (1560.81) and LightGBM (1691.06). This indicates that CatBoost offers the best prediction accuracy among the models.
- Linear Regression and Gradient Boosting have higher RMSE values (2622.53 and 1937.27, respectively), suggesting they are less accurate compared to other models.

**Training Efficiency (Training Time):**

- Linear Regression is by far the fastest model to train, taking only 9.65 seconds. This is significantly faster than all other models.
- LightGBM is also quite efficient, with a training time of 4.99 seconds.
- Random Forest, Gradient Boosting, and CatBoost take much longer, with Random Forest being the slowest (434.57 seconds).

**Prediction Efficiency (Prediction Time):**

- Linear Regression has the fastest prediction time (0.11 seconds), followed by CatBoost and Gradient Boosting (0.19 seconds).
- Random Forest has the slowest prediction time (2.68 seconds), which may be a consideration in time-sensitive applications.

Based on the above analysis, CatBoost is recommended for the highest prediction accuracy, while Linear Regression offers the quickest training and prediction times if efficiency is paramount. If the trade-off between training time and accuracy is acceptable, LightGBM would also be a strong option.
