# Data Scientist Salary Project
Created a salary estimator for data scientist related jobs.

## Data collection
Scraped company info and job descriptions from glassdoor.com using python and selenium

## Data Cleaning
* Parsed: numeric data out of salary, parsed rating out of company names, city out of  headquarter and job description 
* Removed: jobs without salary
* Created new variables: min/max/avg salary, city of headquarter, if job location the same as headquarter, age of company, and skills listed in the job description.

## EDA
Performed exploratory data analysis for the various categorical variables. 
<img src="https://github.com/wei955/Salary-Estimator/blob/master/EDA_Pics/corr.png" height="280">
<img src="https://github.com/wei955/Salary-Estimator/blob/master/EDA_Pics/location_salary.png" height="250">



## Model Building
Split the data into train and tests sets with a test size of 20%, and used three models: Multipul Regression, Lasso Regression, Random Forest. <br>
Evaluated models using Mean Absolute Error. Used GridsearchCV to reach the best model. The Random Forest model is considered as the best-performed one.
* Random Forest : MAE = 16.06
* Lasso Regression: MAE = 16.43
* Multipul Regression: MAE = 23.50

## Productionization
Built a flask API endpoint that was hosted on a local webserver. The API endpoint takes in a request with a list of values from a job listing and returns an estimated salary.

## Reference:
* Web Scraper Code: https://github.com/arapfaik/scraping-... 
* Article: https://towardsdatascience.com/seleni...
* FlaskAPI tutorial: https://towardsdatascience.com/productionize-a-machine-learning-model-with-flask-and-heroku-8201260503d2
* Google chromedrive download: https://chromedriver.chromium.org/

