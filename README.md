# Jira-Splunk ETL Pipeline Project

This project automates the extraction, transformation, and loading (ETL) of Jira data into a PostgreSQL database for analytics and dashboard reporting. The pipeline is orchestrated using Apache Airflow to ensure scheduled, reliable, and maintainable workflows. All scripts and DAG configurations are version-controlled using GitLab to maintain code quality and support collaborative development.

The design goal of this pipeline is to create a flexible and dynamic data architecture where changes to the underlying database schema do not require manual updates to Splunk dashboards. This is achieved by leveraging the Splunk DB Connector and Heavy Forwarder, which query the PostgreSQL database and forward processed data to the Splunk Indexer. The Indexer then handles parsing and indexing, allowing dashboards to automatically reflect any schema changes through dynamic queries and index configurations. This approach minimizes manual intervention, supports real-time reporting, and ensures business users always have access to the latest insights without requiring dashboard rework.

# 🚀 Project Overview

Data Source: Jira Cloud
Orchestrator: Apache Airflow (Running on AWS EC2)
Destination: PostgreSQL (AWS RDS)
Version Control: GitLab
Connector- Splunk DB Connector + Heavy Forwarder + Indexer
Visualization: Splunk Dashboard

```
jira_etl_project/
├── dags/                  # Airflow DAGs for scheduling
│   └── jira_etl_dag.py
├── scripts/               # ETL Python scripts
│   └── etl_jira.py
├── config/                # Configuration files
│   └── settings.json
└── requirements.txt       # Project dependencies
```
