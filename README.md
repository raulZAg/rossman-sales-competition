# Rossmann Store Sales Prediction: Kaggle Competition

## Project Overview

This project involves the development of a predictive model for forecasting the sales of Rossmann, a German-based drugstore, as part of a Kaggle competition. The aim of the project was to utilize historical sales data across multiple stores and use various machine learning techniques to predict future sales accurately.

## Files Included in the Repository

data/: This directory contains all relevant datasets used in this project.
notebooks/: This directory contains the Jupyter notebook for the exploratory data analysis, data cleaning, and modeling.
model/: This directory contains the saved trained model
README.md: This file provides an overview of the project.

Technologies Used

· Python

· Pandas

· Scikit-Learn

· Tensorflow

· Jupyter Notebook

## Model

After doing the exploratory analysis and have taken a look at the data, I decided to use a Long Short Term Memory Neural Network (LSTM) to try to solve this problem. LSTM Models are good for processing sequential data prediction. Data that is good for using LSTM Models such as Audio, Text, Stock Price or any time- series data. 

For this network the structure I used was:

·1 hidden layer consisting of 50 units with 10 percent dropout

·2 hidden layers with 50 units each, followinng a 20 percent dropout

·2 dense layers, consisting of 8 and 1 unit respectively

·Adam is the optimizer and MSE is the loss function and target 

Before training the model I put together the data and train sets to use it to obtain the variables which will train the model. This is using a lookback to see how back we use the data to predict the new data. 
Then I trained the model with the structure shown before. This was used as an autoregressive model and it is used for predicting the correct data based on some data of the train set and then moving along to the test set. That is why we concatenate both of the datasets. We first filled the dates so it didn't had any missingvalues and then use the date and the store to infere the new sales based on previous sales of the same store and day. 

## Results and conclusion 

After inputing the final predicted csv file on the Keggle website. I obtained a score of .21. It wasn't the best but it is a good try. 

This project had a lot of data and the solution wasn't very straight forward therefore it was a challenging and interesting project. 
