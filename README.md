# Bristol-air-quality-database-creation

### Project Overview
The main aim of this project was to create a relational database and then convert it into a NoSQL database which would store the Bristol air quality data set using Python, SQL and MongoDB. The air quality data set used was gotten from the UK air quality website. I considered data ranging from 2004 to 05 October 2022 taken from 19 monitoring stations in and around Bristol.

### The Data
The air quality data set used was gotten from the UK air quality website. I considered data taken from 19 monitoring stations in and around Bristol. The data had 23 columns, I have created a sample table to show this.

|Date Time|NOx|NO2|NO|SiteID|PM10|NVPM10|VPM10|NVPM2.5|PM2.5|VPM2.5|CO|O3|SO2|Temperature|RH|Air Pressure|Location|geo_point_2d|DateStart|DateEnd|Current|Instrument Type|
|-----------|-----------|-----------|-----------|-----------|-----------|-----------|-----------|-----------|-----------|-----------|-----------|-----------|-----------|-----------|-----------|-----------|-----------|-----------|-----------|-----------|-----------|-----------|
1998-02-08T04:00:00+00:00|31.0|23.0|5.0|188|10.0| | | | | |0.3|40.0|3.0| | | |AURN Bristol Centre|51.4572041156,-2.58564914143| | | False|Continuous (Reference)|

I decided to work with data ranging from Jan 1st 2010 to October 19th 2022. I had a list of the stations and their matching station Id so, the next step was to do some data cleaning to ensure that there were no null rows or incorrect station details that could affect the quality of the data. 

The notebook script that I used to do my data cleaning can be found here.


### Process
As this is a database implementation project the next step involved creating an entity diagram to identify the entities, attributes and relationships. I used the SQL Workbench to do this. The entity diagram for the air pollution dataset I created is below.
erd: "/images/pollution.png?raw=true"

I then went on to use the foward engineerng feature on the workbench to generate the sql script to create the tables on the entity diagram. I then went on to the python aspect of the project. I wrote a python script that would connect to phpmyadmin, create and then populate the database.
The script can be found here.

To test my database I wrote some queries.

### NoSQL Database
After going through the diffent subsets of NoSQL databases, I decided to go with a document database. I went with this option because it was using a JSON format which I was easily able to understand. The fact that it also uses key - value pairs wich gave me the familiarity of a python dictionary made me feel more at home with the database. Document databases are great for a number of applications but the one that stood out to me was that it was good for handling and extracting real time data. The air pollution dataset is a real time data and so I felt I was making the right decision. I decided to use Mongo DB Atlas UI for this task.

I used the MongoDB compass to import my data and then used the MongoDB shell to run queries on it 

"/images/shell_method.PNG?raw=true"


### Conclusion
