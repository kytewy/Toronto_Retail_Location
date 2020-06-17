# Toronto_Retail_Location Project 

<img align="right" width="275" src="imgs/Drones.jpg">

## Background

With the people are being asked to socaily distance themselves from others, it causes online sales to rise in a big way! Retailers are facing big issues delivering their products. It is causing shortages and delays for companies that are usually reliable at quickly shipping us everything. 

Walmart has hired an addition 10,000 people to help with online order!

https://www.theglobeandmail.com/business/article-online-grocery-deliveries-struggle-with-surging-demand/


## Introducing Supership! 🚀

To combat this problem, we have created a startup called SuperShip. A shipping company that uses drones to drop packages on
driveways, balconys, and backyards. We are looking to break into the Toronto market. The analytics team is interested in where current demand is and where it will be in the future in order to select the right location for their shipping hub. 

## Project Description 

In this project, we will define fact and dimension tables for a star schema for a particular analytic focus, and write an ETL pipeline with databricks that transfers data from files from two local directories into these tables in Postgres using Python and SQL.

## ETL Process

<img align="center" src = "imgs\etl_arch.PNG" width = "600" > 

This ETL follows the follow steps.

1. Airflow submits pyspark scripts to Spark cluster via Livy. 
2. Spark transforms data and write temp parquet files in Blob Storage.
3. Airflow requests `COPY` commands to copy temp parquet files to Azure SQL Datawarehouse.


## Python Scripts Needed

Run create_tables.py then etl.py

- **create_tables.py**: Drops and creates your tables. You run this file to reset your tables before each time you run your ETL scripts.
- **sql_queries.py**: Contains all your sql queries 
- **etl.py**: Read JSON from data sources loads them into your tables. 

## Database Schema

<img align="center" src = "imgs\data_model.PNG" width = "600" > 

- table name : description

## Data Sources

### Appatment Building Evaluation

link: https://open.toronto.ca/dataset/apartment-building-evaluation/

- Format: Json
- Useful info: Understand the current demand from apartment buildings

### Devlopment Application

link: https://open.toronto.ca/dataset/development-applications/

- Format: csv
- Useful info: Where future demand will be. 

### Census Stats

link: https://www.toronto.ca/city-government/data-research-maps/neighbourhoods-communities/ward-profiles/

- Format: PDF
- Useful info: The statistics about each ward and gives us customer data on income, demograpghics and etc...
