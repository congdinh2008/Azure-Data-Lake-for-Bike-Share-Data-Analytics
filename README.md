# Building an Azure Data Lake for Bike Share Data Analytics
## Project Overview
In this project, you'll build a data lake solution for Divvy bikeshare.

Divvy is a bike sharing program in Chicago, Illinois USA that allows riders to purchase a pass at a kiosk or use a mobile application to unlock a bike at stations around the city and use the bike for a specified amount of time. The bikes can be returned to the same station or to another station. The City of Chicago makes the anonymized bike trip data publicly available for projects like this where we can analyze the data.

Since the data from Divvy are anonymous, we have generated fake rider and account profiles along with fake payment data to go along with the data from Divvy. The dataset looks like this:
<img src="./images/dend-project-erd.jpeg" title="Relational ERD for the Divvy Bikeshare Dataset (with fake data tables)">
Relational ERD for the Divvy Bikeshare Dataset (with fake data tables)

The goal of this project is to develop a data lake solution using Azure Databricks using a lake house architecture. You will:

- Design a star schema based on the business outcomes listed below;
- Import the data into Azure Databricks using Delta Lake to create a Bronze data store;
- Create a gold data store in Delta Lake tables;
- Transform the data into the star schema for a Gold data store;

The business outcomes you are designing for are as follows:
1. Analyze how much time is spent per ride
- Based on date and time factors such as day of week and time of day
- Based on which station is the starting and / or ending station
- Based on age of the rider at time of the ride
- Based on whether the rider is a member or a casual rider
2. Analyze how much money is spent
- Per month, quarter, year
- Per member, based on the age of the rider at account start
3. EXTRA CREDIT - Analyze how much money is spent per member
- Based on how many rides the rider averages per month
- Based on how many minutes the rider spends on a bike per month

## Tasks for the project
### Task 1: Design a star schema based on the business outcomes below
<img src="./images/divvy_star_schema.jpg" title="Divvy Star Schema">

### Task 2: Import the data into Azure Databricks using Delta Lake to create a Bronze data store

#### 2.1 Create Azure Databricks Workspace
<img src="./images/create_azure_databricks.png" title="Create Azure Databricks Workspace">


#### 2.2 Create Azure Databricks Cluster
<img src="./images/create_cluster.png" title="Create Azure Databricks Cluster">

#### 2.3 Import the data into DBFS
<img src="./images/upload_file_dbfs.png" title="Import the data into DBFS">


### Task 3: Create a gold data store in Delta Lake tables
Create Staging Stations
<img src="./images/data_explorer_staging_stations.png" title="Create Staging Stations">

Create Staging Riders
<img src="./images/data_explorer_staging_riders.png" title="Create Staging Riders">

Create Staging Payments
<img src="./images/data_explorer_staging_payments.png" title="Create Staging Payments">

Create Staging Trips
<img src="./images/data_explorer_staging_trips.png" title="Create Staging Trips">


