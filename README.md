# Wafer Fault Detection

This project is a machine learning solution to predict the quality of wafer sensors based on the given training data. The goal is to classify wafers as either good or bad based on sensor readings.

## Architecture

![Picture1](https://user-images.githubusercontent.com/78642104/234994604-1956dca4-c15e-470d-b333-6f67dc57f7ac.jpg)

## Functional Architecture

![Picture2](https://user-images.githubusercontent.com/78642104/234994730-fe171e39-504d-4c82-bd3f-7f62b382086a.png)

The solution is divided into two main phases: training and prediction. The training phase consists of data validation, data insertion in a database, data export, data preprocessing, clustering, and model selection. The prediction phase consists of data validation, data preprocessing, clustering assignment, and model prediction.

## Data Description

The data is in multiple sets of files in batches to a given location. Data contains wafer names and 590 columns of different sensor values for each wafer. The last column has the "Good/Bad" value for each wafer, where +1 represents a bad wafer and -1 represents a good wafer. Apart from training and prediction files, a "schema" file is required from the client. It contains all the relevant information about the files, such as the name, length of date value in the filename, length of time value in the filename, number of columns, name of the columns, and their datatype.

## Usage
To run this project, follow the steps below:

1. Clone the repository to your local machine.
2. Install the required dependencies by running pip install -r requirements.txt in your terminal.
3. Place your training data and schema files in the data folder.
4. Run the training_endpoint.py file to train the model and save it. You can do this by running "python training_endpoint.py" in your terminal.
5. Once the model is trained and saved, you can run the main.py file to make predictions. You can do this by running "python main.py" in your terminal.

Note: To run the project, you need to train the model on training data again since I have not provided my training processed data or models. The process involves taking the data and validating it, preprocessing it, clustering it, and finding the best model from each cluster. The resulting models are saved in the models folder.

To make this process easier, I have created a training_endpoint.py file which can be used to train the data and save the resulting models in a single click. Additionally, I have incorporated this file into the main.py file so that whenever you run main.py, it will first train the model and save it, and then allow you to make predictions. However, please note that this feature is not implemented on the UI part.

![Screenshot 2023-04-28 030001](https://user-images.githubusercontent.com/78642104/234997657-e326e490-d513-4ed7-8b92-31dc7ee3408c.png)

![Screenshot 2023-04-28 030107](https://user-images.githubusercontent.com/78642104/234997681-8843a7ad-8b2c-4e6a-b6aa-f49bdd72e6e5.png)
