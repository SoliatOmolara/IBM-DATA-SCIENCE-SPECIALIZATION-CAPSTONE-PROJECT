# IBM-DATA-SCIENCE-SPECIALIZATION-CAPSTONE-PROJECT


## OUTLINE
1. Introduction

2. Methodology

3. Results

4. Conclusion

5. Appendix

## Executive Summary
### Summary of methodologies
Data Collection through API

Data Collection with Web Scraping

Data Wrangling 

Exploratory Data Analysis with SQL

Exploratory Data Analysis with Data Visualization

Interactive Visual Analytics with Folium

Machine Learning Prediction

## Summary of all results
Exploratory Data Analysis result

Interactive analytics in screenshots

Predictive Analytics result

# INTRODUCTION
## Project background and context
Space X advertises Falcon 9 rocket launches on its website with a cost of 62 million dollars; other providers cost upward of 165 million dollars each, much of the savings is because Space X can reuse the first stage. Therefore, if we can determine if the first stage will land, we can determine the cost of a launch. This information can be used if an alternate company wants to bid against space X for a rocket launch. This goal of the project is to create a machine learning pipeline to predict if the first stage will land successfully.

## Problems we want to find answers
What factors determine if the rocket will land successfully?

The interaction amongst various features that determine the success rate of a successful landing.

# METHODOLOGY
## Data collection methodology:

1. Data was collected using SpaceX API and web scraping from Wikipedia. 

2. Perform data wrangling

    One-hot encoding was applied to categorical features
    
3. Perform exploratory data analysis (EDA) using visualization and SQL

    The table was created on Ibm-db2 database and was connected to Jupyter notebook

4. Perform interactive visual analytics using Folium and Plotly Dash

5. Perform predictive analysis using classification models
    
    How to build, tune, evaluate classification models

# DATA COLLECTION

## The data was collected using various methods;

1. Data collection was done using get request to the SpaceX API.

2. Next, I decoded the response content as a Json using .json() function call and turn it into a pandas dataframe using .json_normalize().

3. It was then cleaned, checked for missing values and fill with missing values where necessary.

4. In addition, I performed web scraping from Wikipedia for Falcon 9 launch records with BeautifulSoup. 

5. The objective was to extract the launch records as HTML table, parse the table and convert it to a pandas dataframe for future analysis.

# DATA COLLECTION WITH SPACEX API

1. I used the get request to the SpaceX API to collect data, clean the requested data and did some basic data wrangling and formatting.
 
2. This link to the notebook is https://github.com/LeehahData/IBM-DATA-SCIENCE-SPECIALIZATION-CAPSTONE-PROJECT/blob/main/Data%20Collection%20with%20Request.ipynb

# DATA COLLECTION WITH WEBSCRAPPING

1. I applied web scrapping to webscrap Falcon 9 launch records with BeautifulSoup 

2. I parsed the table and converted it into a pandas dataframe.

3. This is the link to the notebook is https://github.com/LeehahData/IBM-DATA-SCIENCE-SPECIALIZATION-CAPSTONE-PROJECT/blob/main/Data%20Collection%20with%20webscrapping.ipynb

# DATA WRANGLING
1. I performed exploratory data analysis and determined the training labels.

2. I calculated the number of launches at each site, and the number and occurrence of each orbits

3. I created landing outcome label from outcome column and exported the results to csv.
The link to the notebook is https://github.com/LeehahData/IBM-DATA-SCIENCE-SPECIALIZATION-CAPSTONE-PROJECT/blob/main/Data%20Wrangling.ipynb

# EDA WITH DATA VISUALIZATION

1. I explored the data by visualizing the relationship between flight number and launch Site, payload and launch site, success rate of each orbit type, flight number and orbit type, the launch success yearly trend. 

2. This is the link to the notebook   https://github.com/LeehahData/IBM-DATA-SCIENCE-SPECIALIZATION-CAPSTONE-PROJECT/blob/main/Exploratory%20Data%20Analysis%20with%20Visualization.ipynb

# EDA WITH SQL

1. I loaded the SpaceX dataset into IBM-db2 database and later connected it to jupyter notebook

2. I applied EDA with SQL to get insight from the data. I wrote queries to find out for instance:
  
  a. The names of unique launch sites in the space mission.

  b. The total payload mass carried by boosters launched by NASA (CRS)

  c. The average payload mass carried by booster version F9 v1.1

  d. The total number of successful and failure mission outcomes
  
  e. The failed landing outcomes in drone ship, their booster version and launch site names.

  f. The link to the notebook is https://github.com/LeehahData/IBM-DATA-SCIENCE-SPECIALIZATION-CAPSTONE-PROJECT/blob/main/Exploratory%20Analysis%20using%20Sql.ipynb

# BUILD AN INTERACTIVE MAP WITH FOLIUM

1. I marked all launch sites, and added map objects such as markers, circles, lines to mark the success or failure of launches for each site on the folium map.

2. I assigned the feature launch outcomes (failure or success) to class 0 and 1.i.e., 0 for failure, and 1 for success.

3. Using the color-labeled marker clusters, I identified which launch sites have relatively high success rate. 

4. calculated the distances between a launch site to its proximities to answered some questions for instance:
  
  a. Are launch sites near railways, highways and coastlines.

  b. Do launch sites keep certain distance away from cities.

# BUILD A DASHBOARD WITH PLOTLY DASH

1. I built an interactive dashboard with Plotly dash

2. I plotted pie charts showing the total launches by a certain sites

3. I plotted scatter graph showing the relationship with Outcome and Payload Mass (Kg) for the different booster version.

# PREDICTIVE ANALYSIS (CLASSIFICATION)

1. I loaded the data using Numpy and pandas, transformed the data, split our data into training and testing.

2. I built different machine learning models and tune different hyperparameters using GridSearchCV.

3. I used accuracy score  as the metric for our model, improved the model using feature engineering and algorithm tuning.

4. I found the best performing classification model.

5. This is the link to the notebook https://github.com/LeehahData/IBM-DATA-SCIENCE-SPECIALIZATION-CAPSTONE-PROJECT/blob/main/Machine%20Learning%20Prediction.ipynb

# CONCLUSION

From the datasets We can conclude that:

1. The larger the flight amount at a launch site, the greater the success rate at a launch site.

2. Launch success rate started to increase in 2013 till 2020.

3. Orbits ES-L1, GEO, HEO, SSO, VLEO had the most success rate.

4. KSC LC-39A had the most successful launches of any sites.

5. The Decision tree classifier is the best machine learning algorithm for this task.


# THANKS FOR READING!!!





















