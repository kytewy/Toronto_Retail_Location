<img align="right" width="275" src="imgs/Drones.jpg">

# Toronto_Retail_Location Project 

## Introduction

A startup called SuperShip, is looking to break into the Toronto market. They help with high-end retailers send their products 
to their customer faster than the compeition. To have a competitive advatange over competition, they need to analyze where 
demand is and will be in the fututre in order to select the right location for their shipping hub. The analytics team is particularly interested in understanding where demand is now and where it will be in the future.

## Project Description

In this project, we will define fact and dimension tables for a star schema for a particular analytic focus, 
and write an ETL pipeline with databricks that transfers data from files from two local directories into these tables in Postgres using Python and SQL.g

## Python Scripts Needed

Run create_tables.py then etl.py

- **create_tables.py**: Drops and creates your tables. You run this file to reset your tables before each time you run your ETL scripts.
- **sql_queries.py**: Contains all your sql queries 
- **etl.py**: Read JSON from data sources loads them into your tables. 

## Database Schema

<img src = "" width = "900" > 

- table name : description

## Data Sources

### Appatment Building Evaluation

link: https://open.toronto.ca/dataset/apartment-building-evaluation/

- Format:
- Helping information: Understand the current demand from apartment buildings

### Devlopment Application

link: https://open.toronto.ca/dataset/development-applications/

- Format:
- Helping information: Where future demand will be. 

### Census Stats

link: https://www.toronto.ca/city-government/data-research-maps/neighbourhoods-communities/ward-profiles/

- Format: PDF
- Helping information: The statistics about each ward and gives us customer data on income, demograpghics and etc...
