# Data Lakes with Spark

## Business need

A music streaming startup, Sparkify, has grown their user base and song database even more and want to move their data warehouse to a data lake. Their data resides in S3, in a directory of JSON logs on user activity on the app, as well as a directory with JSON metadata on the songs in their app.

## Steps to achieve
As a Data engineer, I have built an ETL pipeline that extracted data from S3, processed the data using Spark and loaded the data back into S3 using Fact & set of dimensional tables. This will allow the Sparkify analytics team to continue finding insights in what songs their users are listening to.

The used files are

1. dl.cfg --> Configuration file which has details of AWS login
2. etl.py --> Program file to read the data from S3, processed it using the spark and loaded the data back into S3.
3. data --> sample files to understand the structure similar to the data stored in S3. 

## Instructions

1. Update the dl.cfg file with the AWS login
2. Ensure that you updtae the output_data parameter in the etl.py file and execute the file 'etl.py' with python3 in the terminal as > python3 etl.py

## Outcome

The outcome will create a Star schema with a Fact table and set of dimesion tables in the S3 bucket

1. songplays - fact table created from song plays data
2. users - dimension table, unique user records with "user level" by most recent timestamp from log_data
3. songs - dimension table, collection of songs from song_data
4. artists - dimension table, information of different artists from song_data
5. time - dimension table, unique time records from log_data


