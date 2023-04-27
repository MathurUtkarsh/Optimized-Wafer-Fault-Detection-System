# Wafer Fault Detection

This project is a machine learning solution to predict the quality of wafer sensors based on the given training data. The goal is to classify wafers as either good or bad based on sensor readings.

## Architecture

![Picture1](https://user-images.githubusercontent.com/78642104/234994604-1956dca4-c15e-470d-b333-6f67dc57f7ac.jpg)

## Functional Architecture

![Picture2](https://user-images.githubusercontent.com/78642104/234994730-fe171e39-504d-4c82-bd3f-7f62b382086a.png)

The solution is divided into two main phases: training and prediction. The training phase consists of data validation, data insertion in a database, data export, data preprocessing, clustering, and model selection. The prediction phase consists of data validation, data preprocessing, clustering assignment, and model prediction.

## Data Description

The data is in multiple sets of files in batches to a given location. Data contains wafer names and 590 columns of different sensor values for each wafer. The last column has the "Good/Bad" value for each wafer, where +1 represents a bad wafer and -1 represents a good wafer. Apart from training and prediction files, a "schema" file is required from the client. It contains all the relevant information about the files, such as the name, length of date value in the filename, length of time value in the filename, number of columns, name of the columns, and their datatype.


