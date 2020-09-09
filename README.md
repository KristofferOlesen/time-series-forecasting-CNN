# Bayesian Optimization of Time Lags for Time Series Forecasting with CNNs
This is a project on Bayesian Optimization of hyperparameters finalizing a 1-week course on Advanced Topics on Machine Learning from the Technical University of Denmark. The code builds on the work of drewthayer following a tutorial on using a convolutional neural net for time series forecasting. I have adapted the code into a notebook running on Google Colab, and extended with code for Bayesian Optimization using the GPyOpt library. The tutorial provides a dataset and examples of engineering the data and implementing the modeling with Keras.

Original Code: https://github.com/drewthayer/time-series-forecasting-CNN
tutorial: https://machinelearningmastery.com/how-to-develop-convolutional-neural-networks-for-multi-step-time-series-forecasting/

__Business problem:__
Given some number of prior days of total daily power consumption, predict the next standard week of daily power consumption.

__Optimization problem:__
Select the optimal number of prior days to include as the input

__Data:__ 'Household Power Consumption' dataset from UCI machine learning repository
  - household power consumption
  - units: kilowatts
  - frequency: daily
  - time range: 2006 to 2010

__strategy:__
  - Time-sequence forecasting: autoregression
      - be able to predict a forecast for y number of days into the future based on x number of days up to current (e.g. predict next week from this week)
  - Convolutional Neural Network
      - low-bias model that can learn non-linear relationships
      - implemented in Keras
~~~
