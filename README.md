# Project_Disaster_Response
The project consist of building a ML model that will predict the response tactics for disaster management

##### Table of Content
1. [Installation](#Installation)
2. [Project Summary](#Project-Summary)
3. [Data](#Data)
4. [Results](#Results)
5. [Acknowledgements_and_Additional_Scripts](#Acknowledgements-and-Additional-Scripts)

## Installation
The code should run using the standard Python packages (Python versions 3.*).

This project also uses the following packages:

1. Python
2. NumPy
3. pandas
4. scikit-learn (v0.17)
5. active_session script provided
6. sqlalchemy
7. nltk 

## Project Summary
In this project, supervised learning techniques was used by preparing pre-labeled tweets and text messages from real life disasters by using an ETL pipeline. From which the machine learning model was build. To accurately predict that the correct persons respond to the disaster.      

## Data 
The data was obtained from a Figure Eight company and the following files was provided:

1. disaster_messages.csv
2. disaster_categories.csv

The files was read into python therefore completing the extract part of the ETL process. Transforming the data into a workable format was performed by merging the dataset using the id key. The duplicates was removed from the dataset and categories was seperated into different columns that was seperated by ;. The columns was renamed as per the order provided in the data.

The category values was perseved to have 0 and 1 values only. Checkes was perfomed to see if this was the case, it was noted that one category named related had 0, 1 and 2 as values. Related values of 2 was dropped as the messages was in different lanuage and could not be tokenize. Another category called child alone had only 0 values and this category was dropped as well, since no predictions can be made from this level.

The NaN values in the dataset have no impact on the prediction of the model since the message will predict a corresponfing response.

The completed transformed data was loaded to SQL.

## Results

The ML model was build using a pipeline as well as gridsearch to obatin the best model. To view the results the following code needs to be run in the flask app in the terminal: python app/run.py. After which you have to go to the website [here](https://view6914b2f4-3001.udacity-student-workspaces.com/) to view a summary of the data provided as two graphs. A message can be entered into the bar that states 'enter a message to classified' and clicking the classify message button. The message will be classified and the persons that need respond to the message will be marked in green.

Screenshots wall be provided on both the summary of train data as well as a random classified message [here](https://github.com/sylvesters911/Project_Disaster_Response/blob/master/DisasterSummary.PNG) and [here](https://github.com/sylvesters911/Project_Disaster_Response/blob/master/ClassifyExample.PNG)


## Acknowledgements and Additional Scripts
Acknowledgements sited is Udacity and an additional script is used to keep the session active, Figure Eight.
