# Evaluating the Impact of Latitude and Longitude on Air Quality Prediction: A Comparison Between Random Forest and Gradient Boosting Regressors

This research compares the effectiveness of Random Forest Regressor and Gradient Boosting Regressor models in predicting Air Quality Index (AQI), focusing on the role of geographical factors like latitude and longitude as predictive features. The study aims to determine the most accurate model for AQI prediction by evaluating performance metrics such as Mean Squared Error (MSE) and R² score. Results highlight the predictive value of adding geographical features, offering insights for improving AQI forecasting accuracy and model selection in environmental data analysis.

## Dataset
The Weather Dataset : https://www.kaggle.com/datasets/guillemservera/global-daily-climate-data?select=cities.csv
<br>
Global Air Pollution Data : https://www.kaggle.com/datasets/sazidthe1/global-air-pollution-data/data

## Features
- latitude = Latitude coordinate of the city (horizontal line / Equator)<br>
- longitude = Longitude coordinate of the city (vertical line / Prime Meridian)<br>
- aqi_value = Overall AQI value of the city (target prediction)<br>
- co_aqi_value = AQI value of Carbon Monoxide of the city <br>
- ozone_aqi_value = AQI value of Ozone of the city <br>
- no2_aqi_value = AQI value of Nitrogen Dioxide of the city

## Research Results
<div style="display: flex; justify-content: space-between;">
  <img src="/AQI Values Research Results/FI_RandomForest.png" style="width:48%; height:auto;">
  <img src="/AQI Values Research Results/FI_GradientBoosting.png" style="width:48%; height:auto;">
</div>
From both feature importance results above, the Carbon Monoxide amounts ('co_aqi_value') of each city has the highest influence on air quality level. But the latitude & longitude factors both have different 
percentages of influence between the two models. In the Random Forest model, latitude and longitude have an influence percentage of about 30% when summed. But in the Gradient Boosting Model, they have an
influence percentage around 34% when summed.
<br><br>

- <b>Mean Squared Error (MSE)</b> is a metric used to measure how much error there is between the model's predicted value and the actual value. Because MSE works by squaring each error,
it becomes very sensitive to outliers.
- <b>Coefficient of Determination (R²)</b> is a metric that shows how well the model explains the variability in the data. The value ranges from 0 to 1, the closer the R² is to 1,
the better the model is at explaining the variation in the data.
<img src="/AQI Values Research Results/ModelComparisonTable.png" style="width:50%; height:auto;">
In the comparison table, it is shown that the Random Forest model has a slightly lower prediction error rate than Gradient Boosting. But the Random Forest model has a lower R² value than the Gradient Boosting model. This means that the Gradient Boosting model can account for slightly more variation in the data compared to the Random Forest model.
<br><br>

<div style="display: flex; justify-content: space-between;">
  <img src="/AQI Values Research Results/LatitudeVSAQI.png" style="width:48%; height:auto;">
  <img src="/AQI Values Research Results/LongitudeVSAQI.png" style="width:48%; height:auto;">
</div>
In the Scatterplot above, the plot shows a fairly wide distribution of AQI values, with most AQI values below 100, but there are some outliers that even reach above 300.
<img src="/AQI Values Research Results/BoxPlotAQI.png" style="width:50%; height:auto;">
The Box Plot above can give the conclusion that the high Mean Squared Error (MSE) value is most likely due to a large number of outliers and a relatively small dataset. Because most of the AQI values have 
very high values, so the distribution of data is very varied.

## Conclusions
- In this dataset, the Random Forest Regressor model is slightly better at predicting actual values than the Gradient Boosting Regressor model
- The Gradient Boosting Regressor shows that it can account for slightly more variation in data compared to Random Forest Regressor
- Latitude and longitude have only a small degree of influence on air quality. Meanwhile, the level of Carbon Monoxide has the highest influence on air quality in each city
