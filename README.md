# network-monitoring-ai
This project is designed for monitoring, analyzing user behavior, managing bandwidth, and extracting data from Fortigate 60F.

🎯 Project Objectives
Monitoring and optimizing network and internet resources for organizational users
Collecting logs and behavioral data from Fortigate 60F and user systems
Storing and processing data (Batch & Stream)
Unified dashboard for daily and weekly reporting

🏗️ Main Components of the Scenario
Data Sources :
  🔹 Fortigate 60F → Syslog transmission (traffic, web, users)
  🔹 Agent on user systems (e.g., Wazuh/Osquery/Winlogbeat) → Tracks visited websites and running processes
  🔹 File Server (Winlogbeat) → Logs for file access and modifications

Ingestion Layer:
  Kafka (Streaming) → For real-time log collection
  Logstash or Filebeat → For batch/log transmission
  Fluentd/FluentBit (optional) → For lightweight log collection

Processing Layer
  Apache Spark → Batch analysis (daily/weekly)
  Kafka Stream or Logstash → Real-time analysis
  Airflow → Scheduling ETL and periodic processing

Storage Layer
  PostgreSQL → Structured data (users, websites, bandwidth usage)
  MongoDB → Semi-structured data (JSON from agents)
  TimescaleDB or InfluxDB → Time-series data (real-time traffic)

Visualization Layer
  Grafana → Unified dashboard (real-time + daily/weekly reports)
  Connection to PostgreSQL, TimescaleDB, and Elasticsearch (optional for search)




# Structure Project :



# Objectives :
  1) Monitor and analyze user behavior
  2) Review and control bandwidth
  3) Generate daily and weekly reports
  4) Implement AI models for detecting suspicious behavior
