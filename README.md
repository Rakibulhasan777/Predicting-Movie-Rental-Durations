# Predicting-Movie-Rental-Durations 
Build a regression model for a DVD rental firm to predict rental duration. Evaluate models to recommend the best one. 

## Project Overview 
![dvd_image](https://github.com/Rakibulhasan777/Predicting-Movie-Rental-Durations/assets/109708414/14c29360-3287-4052-81f4-4e545e8ce668) 

This data science project aims to help a DVD rental company to make a regression model which will help predict the number of days a customer rents a DVD. The model will hopefully make their inventory planning much more efficient. I decide to help them by running some regression models and recommending the best-performing model to the company.

## The Data 
The data they provided is in the csv file `rental_info.csv`. It has the following features:
- `"rental_date"`: The date (and time) the customer rents the DVD.
- `"return_date"`: The date (and time) the customer returns the DVD.
- `"amount"`: The amount paid by the customer for renting the DVD.
- `"amount_2"`: The square of `"amount"`.
- `"rental_rate"`: The rate at which the DVD is rented for.
- `"rental_rate_2"`: The square of `"rental_rate"`.
- `"release_year"`: The year the movie being rented was released.
- `"length"`: Lenght of the movie being rented, in minuites.
- `"length_2"`: The square of `"length"`.
- `"replacement_cost"`: The amount it will cost the company to replace the DVD.
- `"special_features"`: Any special features, for example trailers/deleted scenes that the DVD also has.
- `"NC-17"`, `"PG"`, `"PG-13"`, `"R"`: These columns are dummy variables of the rating of the movie. It takes the value 1 if the move is rated as the column name and 0 otherwise. For your convinience, the reference dummy has already been dropped.

## Download and Importings 
You can install the released version of Python from [Here](https://www.python.org/downloads/) 
```r
import pandas as pd
import numpy as np 

from sklearn.model_selection import train_test_split
from sklearn.metrics import mean_squared_error 

# For lasso
from sklearn.linear_model import Lasso
from sklearn.model_selection import train_test_split
from sklearn.preprocessing import StandardScaler 

# Run OLS
from sklearn.linear_model import LinearRegression
from sklearn.metrics import mean_squared_error 

# Random forest
from sklearn.ensemble import RandomForestRegressor
from sklearn.model_selection import RandomizedSearchCV
```

## Steps to complete 
  * Getting the number of rental days.
  * Adding dummy variables using the special features column.
  * Executing a train-test split
  * Performing feature selection
  * Choosing models and performing hyperparameter tuning
  * Predicting values on test set
  * Computing mean squared error

## Results/ Findings 
|Best Model |Best MSE| 
|-----------|--------| 
|RandomForestRegressor (10, 51, 9) | 2.225667528098759|
