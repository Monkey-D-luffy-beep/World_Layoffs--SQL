# World_Layoffs--SQL
# World Layoffs Data Cleaning &amp; EDA Project  This project is a comprehensive exploration of a real-world Kaggle dataset that tracks global layoffs during the COVID-19 pandemic. It focuses on data cleaning and exploratory data analysis (EDA) using MySQL, demonstrating techniques to ensure data integrity and derive business insights.


# World Layoffs Data Cleaning & EDA Project

This project is a comprehensive exploration of a real-world Kaggle dataset that tracks global layoffs during the COVID-19 pandemic. It focuses on data cleaning and exploratory data analysis (EDA) using MySQL, demonstrating techniques to ensure data integrity and derive business insights.

## Project Overview

- **Dataset:** World layoffs data from Kaggle.
- **Domain:** HR analytics / Business trends during COVID-19.
- **Technologies:** MySQL (leveraging advanced SQL features like CTEs and window functions).
- **Objectives:**
  - Clean the raw dataset by identifying and removing duplicates.
  - Standardize and correct inconsistent data entries.
  - Handle null values and remove unusable data.
  - Perform EDA to uncover trends across companies, industries, locations, and time periods.

## Data Cleaning Process

1. **Staging Table Creation:**  
   To safeguard the original data, a staging table was created and used for all cleaning operations.
   ```sql
   CREATE TABLE world_layoff.layoffs_staging LIKE world_layoff.layoffs;
   INSERT layoffs_staging SELECT * FROM world_layoff.layoffs;
