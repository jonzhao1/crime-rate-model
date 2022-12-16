## Crime Model
Data collected through the [Data Commons Python API](https://docs.datacommons.org/api/python/) for all 50 states in the United States about the population, median
age, and total crimes for every year from 2011 to 2019. This dataset is used for a logistic regression model that predicts whether the crime rate for a given year and state will be greater or less than the national average crime rate for that given year. 


Data about demographics, crime rates, income, rent prices, etc. were extracted from the Data Commons Python API. This dataset along with others I collected were used 
to predict crime rates based on the relationship between median income and median rent prices. All the datasets were put into an Amazon S3 bucket. More information 
about how to use the API can be found here: https://docs.datacommons.org/api/python/. 

NOTE: Even with an Amazon EC2 instance type of t2.large, pulling all the desired data from the API request caused a “Killed” error in the AWS CLI. Due to this, 
splitting up the API requests is necessary to ensure the instance has enough RAM to execute the code and retrieve all the data needed. Thus, the API requests were 
split into 3 scripts, with each script as an object in the Amazon S3 bucket. 
