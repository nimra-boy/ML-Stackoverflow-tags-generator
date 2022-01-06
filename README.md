![intro](https://user.oc-static.com/upload/2017/01/31/14858512893477_so-logo.png)

# ML-Stackoverflow-tags-generator

## Table of Contents
1. [General Info](#general-info)
2. [Technologies](#technologies)
3. [Data](#data)
4. [Installation](#installation)
5. [API](#api)

### General Info
***
Development of a tag suggestion for Stackoverflow users. This will take the form of a machine learning algorithm that automatically assigns several relevant tags to a question.

## Technologies
***
A list of technologies used within the project:
* [python](https://www.python.org/): Version 3.7
* [scikit-learn](https://scikit-learn.org/stable/): Version 0.24.2
* [numpy](https://numpy.org/): Version 1.20.2
* [pandas](https://pandas.pydata.org/): Version 1.2.3
* [nltk](https://www.nltk.org/): Version 3.2.4
* [seaborn](https://seaborn.pydata.org/): Version 0.11.2
* [matplotlib](https://matplotlib.org/): Version 3.1.1

## Data
***
SQL Query
```SQL
SELECT Title, Body, Tags
From Posts
WHERE PostTypeId = 1
AND CreationDate between '2016-01-01' and DATEADD(m, 48, '2016-01-01')
AND len(Tags) > 0
AND Score > 50
```

## Installation
***
Download CSV data on [stackexchange](https://data.stackexchange.com/stackoverflow/query/new).
Put it on the same directory and name it like that: 'stackoverflowDf.csv'.
Then just perform a *Run all* to run the project.

## API
***
An API based on the XGBoost model is available in a second Git repostory at: https://github.com/nimra-boy/API_Tags_Generator/
