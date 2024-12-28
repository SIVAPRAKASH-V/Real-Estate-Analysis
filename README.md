# Real Estate Sales Analytics and Prediction Pipeline

## Project Overview
This project leverages the **Real Estate Sales 2001-2020 State of Connecticut** dataset to build an end-to-end machine learning pipeline. The solution demonstrates the integration of Azure tools to automate real estate analytics and achieve high accuracy in predicting property types based on various features such as sale prices, locations, and transaction details.

### Key Features:
- **Data Preprocessing & Training**: Using Databricks for efficient data transformation and machine learning.
- **Workflow Orchestration**: Leveraging Azure Data Factory for automation.
- **End-to-End Integration**: Combining Azure Data Lake, Databricks, and Data Factory for seamless data processing and analytics.

---

## Solution Architecture

### Data Preparation
1. **Raw Data Storage**:
   - Kaggle dataset is ingested and stored in **Azure Data Lake Storage (ADLS)** Bronze Layer.
2. **Data Transformation**:
   - Databricks processes raw data into **Delta Tables** in the Silver Layer.
   - Cleaned and transformed data is moved to the **Gold Layer** using Azure Data Factory.

### Machine Learning Model
- **Algorithm**: A Random Forest model is trained on the Gold Layer data for property classification.
- **Deployment**: Azure Data Factory orchestrates the model training and deployment processes on Azure Databricks.

### Workflow Breakdown
1. **Ingestion**: Data is ingested from the Bronze Layer to the Silver Layer.
2. **Transformation**: Data is transformed and moved from the Silver Layer to the Gold Layer.
3. **Prediction**: The Random Forest algorithm classifies property types with high accuracy.
4. **Automation**: Azure Data Factory automates all data movement and transformation pipelines.

   
![image](https://github.com/user-attachments/assets/533909ef-a46e-4668-a655-094c861f712a)

---

## Azure Components

### Azure Data Factory (ADF)
- Automates data movement and transformation.
- Creates and orchestrates pipelines for the seamless flow of data across layers.

### Azure Databricks
- Cloud-based analytics platform for processing large datasets.
- Transforms raw data and builds machine learning models to generate insights efficiently.

### Azure Data Lake Storage (ADLS)
- A scalable repository for storing raw (Bronze), transformed (Silver), and refined (Gold) data.
- Provides access to Databricks for data analysis and model training.

---

## Pipeline Design

### Bronze Zone
- Raw, unprocessed data stored in Azure Data Lake.

### Silver Zone
- Data cleaned and transformed using Databricks.
- Intermediate Delta Tables created for analysis.

### Gold Zone
- Refined data ready for machine learning.
- Used for model training and insights generation.

### ML Model
- **Algorithm**: Random Forest.
- **Purpose**: Predict property types with high accuracy.

### Orchestration
- Azure Data Factory automates:
  - Data movement from Bronze to Silver to Gold.
  - Model training and deployment in Databricks.

---

## Repository Structure
```
|-- notebooks/
|   |-- extraction.ipynb
|   |-- transformation.ipynb
|   |-- load.ipynb
|   |-- EDA.ipynb
|-- README.md
```

---

## How to Use

1. **Setup**
   - Configure Azure Data Lake, Databricks, and Data Factory services.
   - Upload the dataset to the Bronze Zone in ADLS.

2. **Data Processing**
   - Use Databricks notebooks for cleaning and transforming data.
   - Run ADF pipelines to automate data flow between zones.

3. **Model Training and Deployment**
   - Train the Random Forest model using Gold Layer data.
   - Deploy the model via Databricks.

4. **Execution**
   - Monitor and orchestrate workflows using Azure Data Factory.

---

## Results
- Successfully automated the data processing and ML pipeline.
- Achieved high accuracy in property type prediction.
- Demonstrated seamless integration of Azure tools for real estate analytics.

---

## Acknowledgements
- Kaggle for providing the dataset.
- Azure for robust cloud infrastructure.

---

For detailed instructions and troubleshooting, please comment or contact the author.

# Thank you
If you like this project give stars.

