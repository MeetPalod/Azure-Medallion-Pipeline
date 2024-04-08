# Data Migration and Analytics using Microsoft Azure (Data Engineering)
In this project, I created an end-to-end data pipeline that moves the data from an On-Prem SQL database and followed steps such as Data Ingestion, Data Transformation, Data Loading, Data Governance and finally Data Reporting using Microsoft Power BI.




# Project Goals 

1. Data Ingestion - Create a data ingestion pipeline to extract data from on-premises SQL Server Database using Azure Data Factory
2. Data Storage - Create a centralized repository to store data from the SQL Server Database in Azure Data Lake Gen 2 storage.
3. Data Transformation - Create an ETL job to extract the data, do simple transformations, and load the clean data using Azure Databricks.
4. Data Governance - Create Azure key vaults and Active Directory to monitor and govern the whole project using Azure roles.
5. Data Analytics - Create a data integration pipeline with Power BI using Azure Synapse Analytics to create powerful visualizations.


# Data Architecture

The architecture (Data flow) used in this project uses different Azure functionalities.

<p align="center">
  <img width="950" height="550" src="https://github.com/MeetPalod/Azure-Medallion-Pipeline/blob/main/images/architecture.png">
</p>

With the combination of Azure Datalake and Azure Databricks, we can create a lakehouse architecture that follows three layer of data processing: 

* Bronze Layer - This is the exact copy of the data source, in its raw form. All the tables (relational model) or any unstructured data (Non-relational model) is stored in this layer. No transformations are done.
* Silver Layer - In this step, soft data transformations are performed such as fixing data types, column names, date formats, etc. to a standardized format and store in a more structured way.
* Gold Layer - This layer is the cleanest form of data that can be used for downstream tasks. Number of other things could also be implemented at this stage like business rules, conformity checks, etc.

# Dataset Used 
The dataset is an open source database provided by Microsoft namely 'AdventureWorks2017'. It contains a lot of different tables with their corresponding relationships. Dataset link - https://learn.microsoft.com/en-us/sql/samples/adventureworks-install-configure?view=sql-server-ver16&tabs=ssms

# Microsoft Azure Services used in this project
1. **Azure Data Lake Gen2 Storage** - A data lake is a single, centralized repository where you can store all your data, both structured and unstructured. It provides various tools to deal with Big Data analytics based on Azure Blob Storage. It is mainly designed to work with Hadoop and all frameworks that use the Apache HDFS as their data access layer.
2. **Azure Data Factory** - ADF is a fully managed, serverless data intergration service. It allows to create Data Pipelines to Extract, Transform and Load (ELT) data from more than 90 sources. It allows us to choose from more than 90 built-in connectors to acquire data from big data sources such as Amazon Redshift, Google BigQuery, and HDFS.
3. **Azure Databricks** - It is a cloud-based big data analytics platform provided by Microsoft Azure, built on top of Apache Spark. Azure Databricks is a fully managed first-party service that enables an open data lakehouse in Azure. Jupyter notebooks can be used to transform, perform analytics, machine learning, etc. offering the capabilities of Apache Spark.
4. **Azure Synapse Analytics** - Azure Synapse Analytics, formerly known as Azure SQL Data Warehouse, is a cloud-based analytics service provided by Microsoft Azure. It's designed to handle large volumes of data and enable organizations to perform data warehousing, big data analytics, and data integration tasks. It offers a distributed architecture to perform big data analytics.
5. **Azure Key Vault** - Azure Key Vault is a cloud service offered by Microsoft Azure that allows you to securely manage cryptographic keys, secrets, certificates, and other sensitive information used by your applications and services. Key Vault provides a centralized and secure way to store and control access to these sensitive materials.
6. **Azure Active Directory** - Azure Active Directory (Azure AD) is Microsoft's cloud-based identity and access management service. It provides a comprehensive set of capabilities for managing identities, securing access to resources, and enabling seamless authentication and authorization across applications and services. Azure AD is a foundational component of Microsoft's cloud services and plays a crucial role in modern IT infrastructure.
7. **Microsoft Power BI** - Microsoft Power BI is a powerful business intelligence (BI) platform that allows users to visualize and share insights from their data. It enables organizations to connect to a wide range of data sources, transform and shape the data, create interactive reports and dashboards, and share those insights with others. Power BI is designed to help users make data-driven decisions and gain actionable insights from their data.

 
Below is one of the dashboard reports created using PowerBI. 


<p align="center">
  <img width="800" height="400" src="https://github.com/MeetPalod/Azure-Medallion-Pipeline/blob/main/images/powerBI%20insights.png">
  
</p>







