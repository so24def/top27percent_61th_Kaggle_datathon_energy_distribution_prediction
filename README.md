# Predicting the Energy Distribution using past years of data

__Problem type: Time Series Regression__

Includes solution of [__Gdz Elektrik Datathon 2023__](https://www.kaggle.com/competitions/gdz-elektrik-datathon-2023). I attended the competition solo and ranked 61th(top %27) out of 342 competitors and 234 teams. 

## Solution
* Exploratory analysis and visualization of the time series
* Testing, checking and visualizing the components of time series
* Checking the correlation of lag values with ACF-PACF and also lag plots
* Feature engineering; extracting calendar features, detecting and extracting most correlated lag features(based on a threshold), adding and fixing a few external data
* Feature selection with [Sequential Feature Selection](https://rasbt.github.io/mlxtend/user_guide/feature_selection/SequentialFeatureSelector/), [RFECV](https://scikit-learn.org/stable/modules/generated/sklearn.feature_selection.RFECV.html), [LOFO](https://github.com/aerdem4/lofo-importance) (not included in this repo)
* Model selection; CatBoostRegressor, LGBMRegressor, XGBRegressor. Continued with CatBoost-LGBM ensemble
* Hyperparameter tuning with Optuna
* Modelling and making predictions using both direct/recursive methods (I expected recursive method to improve my scores but it didn't help)

***
#### Bonus

* I also added the function that I created to recursively predict with a chosen step size, instead of directly predicting the whole set. This method can also be called as walk forward method. More detail can be found in the regarding notebook. 
***

#### External Data/Sources

* Weather data for both cities: [İzmir](https://rp5.ru/%C4%B0zmir_kentine_ait_hava_durumu_ar%C5%9Fivi), [Manisa](https://rp5.ru/Manisa_kentine_ait_hava_durumu_ar%C5%9Fivi)
* Definitions of station pressure and sea level pressure that I used to choose the right one for my problem: [1](https://www.weather.gov/bou/pressure_definitions), [2](https://kestrelinstruments.com/blog/barometric-pressure-vs-station-pressure-whats-the-difference/)
*  [Turkey COVID timeline](https://tr.wikipedia.org/wiki/T%C3%BCrkiye%27de_COVID-19_pandemisi_zaman_%C3%A7izelgesi)
* [Introduction to Time Series Forecasting With Python](https://machinelearningmastery.com/introduction-to-time-series-forecasting-with-python/) by Jason Brownlee
* [Kishan Manani's presentation](https://www.youtube.com/watch?v=9QtL7m3YS9I) about time series and recursive forecasting
***



https://www.kaggle.com/so24def

