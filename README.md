# Tokyo-Data-Olympic-ETL-Development

## Project Overview

This project involves building a data pipeline and analytics solution using various Azure services. The main objective is to ingest data from an on-premises SQL Server database, transform it, and visualize it through Power BI.

The pipeline comprises:
1. **Data ingestion** using Azure Data Factory.
2. **Data storage** in Azure Data Lake Storage Gen2.
3. **Data transformation** using Azure Databricks.
4. **Data warehousing** using Azure Synapse Analytics.
5. **Dashboard creation** using Power BI.

---

## Tools Used
- Azure Data Factory
- Azure Synapse Analytics
- Azure Databricks
- Azure Data Lake Storage Gen2
- Microsoft Power BI

---

## Architecture Overview

The architecture for this project is depicted below:


---

## Dataset

- **Source**: [Kaggle]
- The dataset contains Olympic-related data, uploaded and processed through Azure components.

---

## Steps to Implement the Solution

### 1. Setting Up Azure Data Lake Storage
- Create a container named `olympic-data`.
- Inside the container, create two directories:
  - **raw-data**: Upload the entire dataset as-is.
  - **transformed-data**: Store the cleaned and transformed dataset.

### 2. Configuring Azure Data Factory
- **Pipeline Creation**:
  - Set up a pipeline to perform a copy activity from the dataset source (e.g., GitHub) to the `raw-data` directory in the Azure Data Lake.
- **Linked Services**:
  - Source: Configure an HTTP file as the source.
  - Sink: Connect to Azure Blob Storage for the raw data directory.

### 3. Data Transformation with Azure Databricks
- **Cluster Setup**:
  - Create a cluster to run PySpark scripts.
- **Notebook Creation**:
  - Develop a notebook in Databricks.
  - Establish a connection between Databricks and Azure Data Lake.
  - Transform the data from the raw-data directory and move the cleaned dataset to the `transformed-data` directory.

### 4. Loading Data into Azure Synapse Analytics
- Import the transformed data from Azure Data Lake into Azure Synapse Analytics for further analysis and querying.

### 5. Power BI Dashboard Development
- Connect Power BI to Azure Synapse Analytics.
- Import the data and create interactive visualizations and dashboards.
- Apply data modeling techniques to structure the data for better insights.

---

## Challenges and Solutions

| **Challenge**                           | **Solution**                                           |
|-----------------------------------------|-------------------------------------------------------|
| Unable to create a cluster in Databricks| Requested additional core permissions from Microsoft. |
| System OS incompatibility with Power BI | Used a Microsoft Azure Virtual Machine to run Power BI. |

---

## Power BI Dashboard

The final dashboard provides interactive visualizations of the dataset, enabling data-driven decision-making. Below is a sample screenshot of the dashboard:


---

## Additional Notes
- **Azure VM Configuration**:
  - Created and configured a Virtual Machine in Azure for Power BI usage due to system limitations.
- **Spark Code**:
  - The Spark scripts for data transformation are available in the Databricks notebook.

---

## Dataset Link
- Dataset: [Kaggle Olympic Data]

---

## How to Run the Project
1. Set up the Azure resources as described.
2. Follow the pipeline steps to ingest and transform the data.
3. Use the provided Spark scripts in Databricks for data cleaning.
4. Load the cleaned data into Azure Synapse.
5. Connect Power BI to Azure Synapse and create the dashboard.

---

## Author
This project was developed as part of a hands-on data engineering and analytics exercise.

