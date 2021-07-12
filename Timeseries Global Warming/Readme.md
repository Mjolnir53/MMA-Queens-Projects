# Data Analysis
To conduct our analysis, we sourced three datasets. A dataset with temperature data from NASA, UK Met, and historical temperature data for the city of Kingston. For NASA the dataset we leveraged can be found here, for the UK Met the data leveraged can be found here, and finally, the data we leveraged for Kingston can be found here. The Kingston dataset contained missing values that spanned the entirety of World War II. To create a completed dataset, we used monthly mean imputation to impute the missing data and complete our dataset. 
The Nasa and UK Met datasets provided us with temperature anomaly data from January 1880 to March 2021 and January 1850 to January 2021, respectively. To conduct our analysis, we made the decision to convert the anomaly data into absolute temperatures in Celsius. Through converting to Celsius, it allowed us to create two datasets with only positive values. Ultimately, this allowed us to test how multiplicative models would forecast temperatures in 2100. 
To create an accurate forecast of global average temperatures in the year 2100, we needed to test and compare various time series models to find the most appropriate model to use. To ensure that we understood our data before modeling, we conducted some fundamental data analysis in Tableau.

### Image 1



This analysis allowed us to quickly understand the trend and evaluate if there might be any seasonality in our data. It also allowed us to evaluate how each dataset compared to the other. We can see that the global average temperatures are steadily increasing for both the NASA and UK Met datasets from our analysis. We have also noticed that there does not appear to be any significant material differences between the NASA and UK Met data. Based on both data sets' decomposition, we can see the rising trend of temperatures, and we observe a very complex seasonal pattern.

### Image 2



We also investigated the ACF and PACF plots for both NASA and UK Met. We can see from both ACF plots that there appears to be significant autocorrelation as the lag period increases. The autocorrelation appears to be more significant for the seasonal lags than the other lags. We are observing a “scalloped” shape every ten years as a result of seasonality. 

### Image 3


Overall, we were able to conclude that both datasets were similar and displayed seasonality and multiple seasonality.   
We began our modeling of both the NASA and UK Met datasets by constructing various exponential smoothing (ETS) and Trigonometric box-cox autoregressive trend seasonality (TBATS) models. These models led to similar MAPE’s however, the forecasts they were producing were not capturing the seasonality that existed in our datasets. We then shifted our focus to Auto-Regressive Integrated Moving Average (ARIMA) models, specifically, Auto ARIMA models with multiple seasonality. Once we started working with models that captured multiple seasonality, the model forecasts displayed a pattern that we would typically expect with modeling global temperatures. Ultimately, the Auto ARIMA models with multiple seasonality were the models we decided to forecast temperatures in 2100. We decided to use the Auto ARIMA model because it could inform us on which parameters should be included in our model and allowed us not to include our own biases. To validate our model, we separated our data into test and train datasets. We decided to proceed with this approach since we did not have enough computing power to run the rolling horizons cross-validation method. As a result, our model may be overfitted. 
The Auto ARIMA models provided us with the lowest MAPES of all the models that we tested and captured the seasonality that we saw in the data and thus decided to select this model to provide our forecasts. We received MAPES of 0.02158156 for the NASA dataset and 0.0121885 for the UK Met dataset. Please refer to table 1 and table 2 in our appendix for a consolidated view of our MAPE results from each model we built.
