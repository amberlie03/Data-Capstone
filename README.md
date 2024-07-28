# Data-Capstone
# Background
SpaceX is one of the most successful companies for affordable space travel. SpaceX advertises the Falcon9 rocket launches as 62 million dollars, whereas other providers cost upwards of 165 million dollars each. The reason for this price difference is that the first stage of launching can be reused. Therefore, if we determine whether the first stage will land, we can determine the cost of the launch. The goal of this project is to use the public information and training a machine learning model to predict if SpaceX will land successfully and reuse the first stage.

# Explore
How payload mass, launch site, number of flights, and orbits affect first-stage landing success
Rate of successful landings over time
Best predictive model for successful landing (binary classification)
# Executive Summary
The research attempts to identify the factors for a successful rocket landing.

Collect data using SpaceX REST API and web scraping techniques
Wrangle data to create success/fail outcome variable
Explore data with data visualization techniques, considering payload, launch site, flight number and yearly trend
Analyze the data with SQL, calculating total payload, payload range for successful launches, and total # of successful and failed outcomes
Explore launch site success rates and proximity to geographical markers
Visualize the launch sites with the most success and successful payload ranges
Build Models to predict landing outcomes using logistic regression, support vector machine (SVM), decision tree and K-nearest neighbor (KNN)
Results
# Exploratory Data Analysis:
Launch success has improved over time
KSC LC-39A has the highest success rate among landing sites
Orbits ES-L1, GEO, HEO, and SSO have a 100% success rate
# Visualization / Analytics:
Most launch sites are near the equator, and all are close to the coast
# Predictive Analytics
All models performed similarly on the test set. The decision tree model slightly outperformed in accuracy
# Methodology
Request rocket launch data from API
Decode the response and turn into a data frame using .json_normalize()
Request info by applying custom functions
Construct data into a dictionary and create a data frame from it
Filter the data for Falcon 9 
Replace missing values with the column mean
Export the data to CSV
# Data Collection - Web Scraping
Request Falcon 9 data from the static url
Create a BeautifulSoup object from the HTML response
Extract all the column names from HTML table
Parse the tables to collect data 
Convert data into dictionary and create data frame
Export to CSV
# Data Wrangling
Convert outcomes into 1 for a successful landing and 0 for an unsuccessful landing
# EDA with Visualization
Create charts to analyze relationships and show comparisons
# EDA with SQL
Query the data to understand more about the data
# Maps with Folium
Create maps to visualize launch sites, view launch outcomes and see distance to proximities
# Dashboard with Plotly Dash
Create dashboard
Pie chart showing successful launches
Scatter chart showing Payload Mass vs. Success Rate by Booster Version
# Predictive Analytics
Create NumPy array from the Class column
Standardize the data with StandardScaler. Fit and transform the data.
Split the data using train_test_split
Create a GridSearchCV object for parameter optimization
Apply GridSearchCV on different algorithms: logistic regression, support vector machine, decision tree, K-Nearest Neighbor
Calculate accuracy on the test data for all models
Assess the confusion matrix for all models
Identify the best model using Jaccard_Score, F1_Score and Accuracy
# Conclusion
Decision Tree is the best algorithm model for this data 
Most launches are close to the equator and coastlines but further from cities
Launch success increases overtime, KSC LC-39A has the highest success rate of launches
The higher the payload mass the better the performance
Orbits ES-L1, GEO, HEO, and SSO have a 100% success rate

