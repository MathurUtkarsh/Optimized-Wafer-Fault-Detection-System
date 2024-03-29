# Wafer Fault Detection

This project is a machine learning solution to predict the quality of wafer sensors based on the given training data. The goal is to classify wafers as either good or bad based on sensor readings.

## Architecture

![Picture1](https://user-images.githubusercontent.com/78642104/234994604-1956dca4-c15e-470d-b333-6f67dc57f7ac.jpg)

## Data Description

The data is in multiple sets of files in batches to a given location. Data contains wafer names and 590 columns of different sensor values for each wafer. The last column has the "Good/Bad" value for each wafer, where +1 represents a bad wafer and -1 represents a good wafer. Apart from training and prediction files, a "schema" file is required from the client. It contains all the relevant information about the files, such as the name, length of date value in the filename, length of time value in the filename, number of columns, name of the columns, and their datatype.

## Functional Architecture

![Picture2](https://user-images.githubusercontent.com/78642104/234994730-fe171e39-504d-4c82-bd3f-7f62b382086a.png)

The solution is divided into two main phases: training and prediction. The training phase consists of data validation, data insertion in a database, data export, data preprocessing, clustering, and model selection. The prediction phase consists of data validation, data preprocessing, clustering assignment, and model prediction.

## Requirements

1. attrs==19.3.0
2. certifi==2019.11.28
3. Click==7.0
4. cycler==0.10.0
5. Flask==1.1.1
6. Flask-Cors==3.0.8
7. importlib-metadata==1.4.0
8. Flask-MonitoringDashboard==3.0.6
9. itsdangerous==1.1.0
10. Jinja2==2.11.0
11. joblib==0.14.1
12. jsonschema==3.2.0
13. kiwisolver==1.1.0
14. kneed==0.5.1
15. MarkupSafe==1.1.1
16. matplotlib==3.1.2
17. more-itertools==8.1.0
18. 1numpy==1.18.1
19. pandas==0.25.3
20. pyparsing==2.4.6
21. pyrsistent==0.15.7
22. python-dateutil==2.8.1
23. pytz==2019.3
24. PyYAML==5.3
25. regexp==0.1
26. scikit-learn==0.22.1
27. six==1.14.0
28. sklearn==0.0
29. Werkzeug==0.16.1
30. wincertstore==0.2
31. xgboost==0.90
32. zipp==2.0.1


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
 
 
This is how main.py looks like:

![Screenshot 2023-04-28 030107](https://user-images.githubusercontent.com/78642104/234997681-8843a7ad-8b2c-4e6a-b6aa-f49bdd72e6e5.png)


This is how train_endpoint.py looks like 

![Screenshot 2023-04-28 030138](https://user-images.githubusercontent.com/78642104/234997885-c029fc05-ed27-4bbf-9d7b-d441332daa88.png)

## Conclusion

In conclusion, the wafer fault detection project aims to detect faulty wafers in semiconductor manufacturing processes. The project uses machine learning algorithms to classify wafers into fault and non-fault categories. Here various data pre-processing techniques, including oversampling and undersampling, were applied to the data. The performance of several machine learning models, including SVM, Random Forest, and XGBoost, was evaluated on the pre-processed data. 

Finally, a web application was built using Flask to demonstrate the model's performance on new, unseen data. The application takes a CSV file of wafer sensor data as input and predicts whether the wafers are faulty or non-faulty. This project demonstrates the potential of machine learning algorithms in improving the efficiency and reliability of semiconductor manufacturing processes.

