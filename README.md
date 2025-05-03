## About this project:
This project aims to find a supervised regression and or classification model that best predicts domestic flight delays at U.S. airports based on data from the past 15 years. Put simply, the main question for this project is the following: What factors contribute to flight delays? Identifying factors, both controllable and uncontrollable, can inform passengers of best ways to prepare for and predict flight delays. This knowledge can also help airlines mitigate flight delays to save money and stress.

## Data collection:
scraper.ipynb is a script created to automate data collection for this project. Data is collected from the Bureau of Transportation Statistics 
(“Reporting Carrier On-Time Performance (1987-present)”) by running a headless browser using Selenium webdriver. <br />

Users can customize the date range of collected data by specifying the years and months to loop through. <br />

The exact features to be collected can also be modified, but the default variables are the following:
      "YEAR", "MONTH", "OP_UNIQUE_CARRIER", "ORIGIN_AIRPORT_SEQ_ID", "ORIGIN_CITY_MARKET_ID",
      "ORIGIN_CITY_NAME", "ORIGIN_STATE_ABR", "DEST_AIRPORT_SEQ_ID", "DEST_CITY_MARKET_ID",
      "DEST_CITY_NAME", "DEST_STATE_ABR", "DEP_DELAY", "ARR_DELAY", "CANCELLED", "CANCELLATION_CODE",
      "DIVERTED", "CARRIER_DELAY", "WEATHER_DELAY", "NAS_DELAY", "SECURITY_DELAY", "LATE_AIRCRAFT_DELAY"


## Data analysis:
delay_prediction.ipynb is the notebook used for exploratory data analysis and ML modeling. <br />

EDA plots consist of scatterplot and barplot visualizations of flight observations divided by year, month, carrier (airline), and airports.
Each division was also broken down into contributions by five delay factors as recorded by the Bureau: carrier delay, late arrival delay, 
weather delay, National Airspace System (NAS) delay, and security delay. <br />

The ML models used in the notebook include linear regression, logistic regression, Naive Bayes, and Decision Trees. All models come from the 
sci-kit learn/sklearn libraries.
