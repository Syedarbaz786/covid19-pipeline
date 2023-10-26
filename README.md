# Covid-19 ETL Pipeline Project
## An automated data pipeline for ecdc information.
## Goal of the project
The purpose of this project is to build an ETL pipeline that will be able to provide information to data analysts, doctors and medical researchers with population statistics affected by the covid-19 virus for different cities. It does this by first extracting cases deaths, hospital admissions data from various datasets, from ecdc website. Then by an ADF pipeline the data get transfomered to the Data Lake Gen 2.

## Use Cases
Below are some of the use cases of the data collected:
- The data can be used to identify the impact that affected people by covid-19 virus have on city population, going even further to categorize the impact by gender.
- Medical researchers can use the data to identify what some of the most common reason that the people are getting affected by the virus.
- Doctors can create a good vacccine for the people.

## Database Model
- This project contains various datasets from the ecdc website like cases_deaths, hospital_admissions, testing and country_response and all the datasets are in csv formats.
- The brief description of the datasets are given below.

### Cases Deaths Table

- Columns: country, country_code, continent, population, indicator, daily_count, date, rate_14_day, source.

### Hospital Admissions Table

- Columns: country, indicator, date, year_week, value, source, url.

### Testing Table

- Columns: country, country_code, year_week, new_cases, tests_done, population, testing_rate, positivity_rate, testing_data_source.

### Country Response Table

- Columns: country, response_measure, change, date_start, date_end.

## Tools and Technologies used
The tools used in this project include:
- Microsoft Azure: Microsoft Azure is a comprehensive cloud computing platform and infrastructure service offered by Microsoft. It provides a wide range of cloud services, including virtual machines, databases, AI and machine learning tools, analytics, and more. Azure enables businesses to build, deploy, and manage applications and services through a global network of data centers, offering scalability, flexibility, and a robust ecosystem of tools and services for various cloud computing needs.


- Azure Data Factory: Azure Data Factory is a cloud-based data integration service provided by Microsoft Azure. It allows users to create, schedule, and manage data pipelines, facilitating the movement, transformation, and orchestration of data from various sources to various destinations. Azure Data Factory supports both on-premises and cloud-based data sources, making it a valuable tool for ETL (Extract, Transform, Load) processes, data migration, and data transformation tasks. It offers a visual interface for building data workflows and integrates with other Azure services for enhanced data processing and analytics.

- Azure Data Lake Storage Gen2: Azure Data Lake Storage Gen2 is a scalable and secure data lake solution provided by Microsoft Azure. It combines the capabilities of Azure Blob Storage with enhanced analytics and data management features, such as hierarchical file systems and data lake capabilities. Gen2 is designed for big data and analytics workloads, offering features like fine-grained access control, data encryption, and integration with various Azure data services, making it a powerful choice for storing and analyzing large volumes of data in a distributed and cost-effective manner.

## Datasets Used
The datasets used and sources include:
- All the datasets are used from https://www.ecdc.europa.eu/en/data.

## Steps:
1- The dataset is pulled from the ecdc websites using the Azure data factory.
2- The http ingestion is done.
3- For the data storage we use Azure Data Lake Gen 2

## Built With
- Microsoft Azure
## Authors
- Syed Arbaz

