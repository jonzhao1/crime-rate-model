## DataCommons-Python_API
Data about demographics, crime rates, income, rent prices, etc. were extracted from the Data Commons Python API. This dataset along with others I collected were used 
to predict crime rates based on the relationship between median income and median rent prices. All the datasets were put into an Amazon S3 bucket. More information 
about how to use the API can be found here: https://docs.datacommons.org/api/python/. 

NOTE: Even with an Amazon EC2 instance type of t2.large, pulling all the desired data from the API request caused a “Killed” error in the AWS CLI. Due to this, 
splitting up the API requests is necessary to ensure the instance has enough RAM to execute the code and retrieve all the data needed. Thus, the API requests were 
split into 3 scripts, with each script as an object in the Amazon S3 bucket. 
