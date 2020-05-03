# COVID19_DeepLearning
A RNN approach to predicting when a stay at home order was announced given case data

## File overview

### dataprep

This folder was used to scrape the below sources and gather needed data

1. shelterinplace.csv: scraped via "webscraping.ipynb" notebook, which pulls from NYTimes
2. us-counties.csv: pulled from NYTimes github page, https://github.com/nytimes/covid-19-data
3. city_count.csv: manually created to handle city/county discrepancies between above two files
4. us_county_sociohealth_data.csv: pulled from github page: https://www.kaggle.com/johnjdavisiv/us-counties-covid19-weather-sociohealth-data

mergedata.ipynb: Combines the above four data sources into a **final.csv** for the RNN model

### RNN_Model.ipnyb

This is our primary model with the below architecture. It produces an RNN model that looks at the next 19 days to predict if today has a stay at home for a given county. This file also contains our model performance evaluation.

<img src="/images/RNN_Model.png" height="300px" width="150px">

### RNN_Model_extended.ipnyb

This model includes demographic information with the below architecture. Similar to the RNN_Model, it looks at the next 19 days to predict if today has a stay at home for a given county.

<img src="/images/RNN_Model_2.png" height="300px" width="300px">
