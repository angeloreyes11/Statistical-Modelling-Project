# City Bikes API - Statistical Modelling Project

## Project/Goals

Main objectives needed for this assignment:

- Explore the different API documentations to review it's structure to query an API request from multiple APIs that were needed for this project. (CityBikes, Foursquare, and Yelp)
- Pull and understand the data being returned. This include knowing how to parse relevant data and use methods of data cleaning before converting it to a DataFrame.
- Combine these new DataFrame into a new DataFrame for analyzing and building EDAs to help interpretation of that data. 
- Build a regression model to analyze relationships between different characteristics of our parsed data.


## Process
## Step 1: Data Collection 

- Using API request queries to pull desired data from different sources to use for data analyzation.
- Knowledge on where to look for documentation for these queries.
- Parse JSON data for convertion to DataFrames

## Step 2: EDA

- Use different visualization models to help understand the data further. (ploty, and metplotlib)
- Use SQLite3 to store our results to our local machine.

## Step 3: Model Building

- Use python's statsmodel to contruct a regression model.
- Output a OLS regression summary as well as plot different graphs for visualization help. (residual plots and predicted vs actual plot diagrams)

## Step 4: Model Evaluation

- Usee these results and their numbers to determine relationships and significant level of the model.

## Results

Based on the results of our regression model, it looks like that the coefficients indicate that our model's independent variable on the available bikes on the distance of each POIs is not statistically significant. We can examine small coefficient numbers (0.0022 for distance_meters_forsquare and 0.0012 for distance_meters_yelp) and their associated p-values are high which indicates that these predictors are not significant in predicting the available bikes in the area. We can also see that got a high p-value(F-static) (0.423) which is much higher than the usual significance level of 0.05. This means that the overall importance of the model is not very significant. To summarized, this current model that compares the distances of POIs and their relationship with how many number of bikes that is available appears to be very insignificant. Many factors might had affected this result. Other characteristics that we can pull from the different APIs that we chose to not include or drop may enhance this model, or it could be possible that the POI distances are just not a strong enough indicators for bike availability.

## Challenges 

A major hurdle that was faced during this project is Yelp API daily limitation. While trying to build a code to parse the requested data, there were a limit of 500 requests per day that only resets at 5 pm MST. This wasted a couple of days of my time as I had to wait for them to reset in order to continue working on the next steps of the project. 

## Future Goals

If given more time to work on this project, I would include other similar POI characteristics instead of dropping them to see whether or not this would increase the significance of our results.
