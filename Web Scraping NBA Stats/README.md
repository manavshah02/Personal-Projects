# Web Scraping NBA Stats Using Python
In this project, we are using Python to scrape NBA stats and utilize those stats to predict which player should be winning MVP each year,
from 1994 to 2022. Through this project, I was able to learn how to web scrape data, clean data to make it easier and more accessible, and create machine
learning models and how to test their accuracy.

- **Language:** Python
- **Libraries Used:** Pandas, scikit-learn, requests, matplotlib
- **Packages:** BeautifulSoup (HTML Parser), Selenium

## Step 1: Web Scraping
The first step is to perform web scraping. The website basketball-reference.com is the site from which I am scraping the data 
and information that we need. I scraped the MVP standings, player statistics, and team standings from each year. To do the 
scraping, I used Python, with the Selenium, BeautifulSoup, Pandas, and requests libraries. I downloaded the files using 
requests and Selenium, then parsed them with BeautifulSoup and then loaded them into Pandas DataFrames. With those DataFrames created, I
converted them into CSV files which we are able to access our data and statistics that we require a lot easier.

## Step 2: Data Cleaning
The second step of this project is to perform data cleaning. I wanted to remove unwanted values, columns, and rows that are present.
I also wanted to ensure the players are not appearing multiple times in one season, rather appearing with the last team they played
for in that year. Then once cleaned, I combined the MVP, player, and team stats data using Pandas.  Along the way, I worked through a 
lot of data cleaning, including using merge, map, fillna, and replace. I also used matplotlib to explore the data. with this final DataFrame,
I was able to create a CSV file that with those combined statistics and utilize to build step 3, which is a machine learning model.

## Step 3: Machine Learning
Then the final step was developing a machine learning model to predict who would win MVP each year, based off their statistics 
and team record. I first prepared the data for machine learning and used a Ridge Regression model, which removed overfitting and 
only kept enough bias as necessary. Then I defined an error metric, backtest across most of the data set, and iterated on our predictors, which
were all the statistics of each player. This error metric helped us determine average precision, in which our Ridge Regression model had a
precision of 0.82. Then, I tried using a Random Forest model (combining the output of multiple decision trees to reach a single result) 
to make predictions, however this model seemed to result in a lower average precision of 0.72. Then finally I tried the StandardScaler model,
a model which removes the mean and scales the data to unit variance. The scaling shrinks the range of the feature values, however it will still
take outliers into factor when computing mean. In this model, average precision was seen to be the highest, resulting in an mean average
precision of 0.88.









###### This project was learned from Dataquest's Predicting the NBA MVP: Machine Learning Project Youtube course.


