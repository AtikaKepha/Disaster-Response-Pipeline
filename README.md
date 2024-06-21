# Disaster Response Pipeline Project 

## Introduction
In this project, data engineering was used to analyze disaster data from Appen (formerly Figure 8) to build a model for an API that classifies disaster messages.

A data set containing real messages that were sent during disaster events was used. A machine learning pipeline to categorize these events so that you can send the messages to an appropriate disaster relief agency was also created.

A web app where an emergency worker can input a new message and get classification results in several categories was used for deployment. The web app also displays visualizations of the data. 


## File Descriptions

### app folder
**master.html** - main page of web app
**go.html** - classification result page of web app
**run.py** - Flask file that runs app

### data folder
**disaster_categories.csv** - data to process 
**disaster_messages.csv** - data to process
**process_data.py** - ETL pipeline used to load, clean, extract feature and store data in SQLite database
**DisasterResponse.db**- database to save clean data to

### models folder
**train_classifier.py** - ML pipeline used to load cleaned data, train model, and save trained model as pickle (.pkl) file for later use
**classifier.pkl** - saved model 


## Installation
* Python version 3.11.3

Libraries used are as follows;
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Sklearn
* Plotly

## Instructions
1. Run the following commands in the project's root directory to set up your database and model.

    - To run ETL pipeline that cleans data and stores in database
        `python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db`
    - To run ML pipeline that trains classifier and saves
        `python models/train_classifier.py data/DisasterResponse.db models/classifier.pkl`

2. Run the following command in the app's directory to run your web app.
    `python run.py`

3. Go to http://127.0.0.1:5000

## Acknowledgements
* * [Figure Eight](https://www.figure-eight.com/) for providing the datasets to train the model.

## Screenshots
1. Main page of web app
https://github.com/AtikaKepha/Disaster-Response-Pipeline/blob/main/Screenshots/Main%20Page%20-%20Message%20Classification.png
https://github.com/AtikaKepha/Disaster-Response-Pipeline/blob/main/Screenshots/Main%20Page%20-%20Distribution%20of%20Message%20Genres.png
https://github.com/AtikaKepha/Disaster-Response-Pipeline/blob/main/Screenshots/Main%20Page%20-%20Distribution%20of%20Message%20Categories.png
https://github.com/AtikaKepha/Disaster-Response-Pipeline/blob/main/Screenshots/Main%20Page%20-%20Categories%20Distribution%20in%20Direct%20Genre.png

2. Run process_data.py for ETL pipeline
https://github.com/AtikaKepha/Disaster-Response-Pipeline/blob/main/Screenshots/process_data.py.png

3. Run train_classifier.py for ML pipeline
https://github.com/AtikaKepha/Disaster-Response-Pipeline/blob/main/Screenshots/classifier.py1.png
https://github.com/AtikaKepha/Disaster-Response-Pipeline/blob/main/Screenshots/classifier.py2.png

6. Run run.py in app's directory to run web app
https://github.com/AtikaKepha/Disaster-Response-Pipeline/blob/main/Screenshots/run.py.png
