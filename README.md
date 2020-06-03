# Disaster Response Messages

A set of messages related to disaster response, covering multiple languages, suitable for text categorization and related natural language processing tasks.

## Contents
1. [Motivation](https://github.com/shwets1503/Disaster_Response_Pipeline/blob/master/README.md#motivation)
2. [Dataset](https://github.com/shwets1503/Disaster_Response_Pipeline/blob/master/README.md#dataset)
3. [Installation](https://github.com/shwets1503/Disaster_Response_Pipeline/blob/master/README.md#installation)
4. [Files Description](https://github.com/shwets1503/Disaster_Response_Pipeline/blob/master/README.md#files description)
5. [Results](https://github.com/shwets1503/Disaster_Response_Pipeline/blob/master/README.md#results)

---

## Motivation
In this project, I am using my Data Engineering skills to analyze disaster data from Figure Eight. The classifier model is built using Extract, Transform and Load process(ETL), natural language processing(NLP) and machine learning pipeline for classifying disaster messages. The project also includes a web app where an emergency worker can input a new message and get classification results in several categories. It can be useful to detect what messages actually need attention during the event of a disaster.

---

## Dataset
The dataset contains 30,000 messages drawn from events including an earthquake in Haiti in 2010, an earthquake in Chile in 2010, floods in Pakistan in 2010, super-storm Sandy in the U.S.A. in 2012, and news articles spanning a large number of years and 100s of different disasters.

The data has been encoded with 36 different categories related to disaster response and has been stripped of messages with sensitive information in their entirety.

---

## Installation

1. Run the following commands in the project's root directory to set up database and model.

  - To run ETL pipeline that cleans data and stores in database python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db
  - To run ML pipeline that trains classifier and saves python models/train_classifier.py data/DisasterResponse.db models/classifier.pkl
2. Run the following command in the app's directory to run your web app. python run.py

3. Go to http://0.0.0.0:3001/

---

## Files Description
This is the file-folder structure of the project.

```
.
├── app     
│   ├── run.py                           # Flask file that runs app
│   └── templates   
│       ├── go.html                      # Classification result page of web app
│       └── master.html                  # Main page of web app    
├── data                   
│   ├── disaster_categories.csv          # Dataset including all the categories  
│   ├── disaster_messages.csv            # Dataset including all the messages
│   └── process_data.py                  # Data cleaning
├── models
│   └── train_classifier.py              # Train ML model           
└── README.md
```
---

## Results
The model has accuracy of 95.34% which is really good and precision of 76%. 

![Disasters](https://user-images.githubusercontent.com/33171500/83582390-9663e900-a4fe-11ea-9300-7779c116819c.png)

![Disasters (1)](https://user-images.githubusercontent.com/33171500/83582473-d0cd8600-a4fe-11ea-99f3-39dc6dd42b47.png)






