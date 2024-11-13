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
From both feature importance results above, the Carbon Monoxide amounts ('co_aqi_value') of each city has the highest influence on air quality level.


<div style="display: flex; justify-content: space-between;">
  <img src="/AQI Values Research Results/LatitudeVSAQI.png" style="width:48%; height:auto;">
  <img src="/AQI Values Research Results/LongitudeVSAQI.png" style="width:48%; height:auto;">
</div>
