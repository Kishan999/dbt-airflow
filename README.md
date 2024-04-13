Overview
========

This project aims to showcase the integration of Data Build Tool (DBT), Apache Airflow, and Snowflake to orchestrate the ingestion, transformation, and storage of data. In this project, we are reading data from local CSV files, creating views in Snowflake, performing transformations using DBT, and finally writing the transformed data back to Snowflake.

Components
================

**Data Sources**: Local CSV files containing raw data.
**Snowflake**: Cloud-based data warehousing platform where the data is stored and processed.
**DBT (Data Build Tool)**: A tool for transforming data in your warehouse, written in SQL or Jinja.
**Apache Airflow**: A platform to programmatically author, schedule, and monitor workflows.
**Astronomer Cosmos**: Connects DBT with Apache Airflow, enabling seamless integration and execution.

Workflow Overview:
===========================

1. **Data Injestion**

- Raw data is sourced from local CSV files.
- Data is loaded into Snowflake staging area.

2. **Data Transformation:**

- DBT is utilized to transform the raw data into structured formats.
- Transformations include cleaning, aggregating, and joining data as required.

3. **Data Storage**

- Transformed data is written back into Snowflake.
- Views are created for easy access to transformed data.

4. **Orchestration with Apache Airflow:**

- Apache Airflow schedules and monitors the entire workflow.
- DAGs (Directed Acyclic Graphs) are defined to orchestrate the sequence of tasks.
- Astronomer Cosmos facilitates the integration between DBT and Airflow.

Architecture:
=================================
![Untitled Diagram](https://github.com/Kishan999/dbt-airflow/assets/30801304/8a10551a-afd0-45d9-a92c-618e0a989eaa)


Instructions:
=================================
1. **Setup Snowflake**:

- Create a Snowflake account and configure necessary users, roles, and warehouses.
- Update Snowflake connection details in the Airflow configuration.

2. **Setup Airflow:**

- Install Apache Airflow and required dependencies.
- Configure Airflow connections for Snowflake.

3. **Setup DBT:**

- Install DBT and configure connection to Snowflake.
- Define DBT models for data transformation in the dbt/models directory.

4. **Setup Astronomer Cosmos:**

- Install and configure Astronomer Cosmos for connecting DBT with Apache Airflow.
- Ensure proper configuration to execute DBT models within Airflow DAGs.

5. **Project Configuration:**

- Update any project-specific configurations in respective configuration files (e.g., Airflow DAGs, DBT project file).

6. **Run the Workflow:**

- Start Apache Airflow scheduler and webserver.
- Trigger the DAG to initiate the workflow.

