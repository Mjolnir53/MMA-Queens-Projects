# Business Problem

The challenge of the data set is to use 79 explanatory variables to determine the sale price of homes in Ames, Iowa. Using advanced linear regression techniques the goal is to develop a model that and significantly link specific variables predict the sales price of the homes.
Kaggle describes this competition as:
Ask a home buyer to describe their dream house, and they probably won’t begin with the height of the basement ceiling or the proximity to an east-west railroad. But this playground competition’s dataset proves that much more influences price negotiations than the number of bedrooms or a white-picket fence.
With 79 explanatory variables describing (almost) every aspect of residential homes in Ames, Iowa, this competition challenges you to predict the final price of each home.

# Exploratory Data Analysis (EDA)

The training and testing data were assessed using the data dictionary as a guide for context on specific variables. The data was cleaned, and a simple regression model was built for a baseline. From there the model was refined using interaction variables and finally lasso and ridge regression techniques were applied to refine the model’s predictive capabilities. 

### Cleaning Missing Data

## IMAGE

I was able to isolate the 35 variables with missing values of which the SalePrice missing values match the test set. 
With the help of the data dictionary, and sorting through the variables one at a time, I was able to determine that most of the missing values are only coded as NA but that just means that the property does not have that feature. Therefore, most of the categorical variables with NAs were coded to “None” and most of the integer variables with NA were coded to 0. 
Some of the categorical variables with actual missing values were coded to the mode of the variable observations. 
Once all the missing values were dealt with, the data set was converted into factors and integers to keep all the observation types consistent. 



### Identify Important Variables

## IMAGE
## IMAGE
## IMAGE


# Conclusion

Considering the number of variables. Running a LASSO regression with all the variables  I was able to achieve an RMSE of 13136.
The data dictionary was instrumental in interpreting the data and figuring out how to fill the missing values. 
Data cleaning and interpretation is largely based on one’s own biases and perspectives. 
Even model building and variable selection can be largely dependant upon the modellers own personal views whether they try to be impartial or not. 
I found my use of interaction variables to be rudimentary at best as there was significant feature engineering I left on the table. 




