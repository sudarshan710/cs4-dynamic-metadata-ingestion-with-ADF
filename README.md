# Dynamic Data Ingestion using MetaData Control Table with Azure Data Factory

  This project revolves around a simple ingestion pipeline to insert multiple tables using Metadata Control Table using Data Flow and Pipeline in Azure Data Factory. Later, the data would undergo bronze-silver-gold
  layer transformations including GDPR (PII Masking).

## Structure

  - SQL Server Database Table as source.
  - Azure Blob Storage (/Data Lake) as sink.
  - Using Lookup, ForEach activiting in Pipeline with DataFlow connection between Source and Sink.
  - Bronze-Silver-Gold Layer Transformations for GDPR privacy compliances.

## Pipeline

The pipeline is structured as `Lookup`->`ForEach`->[`Ingestion Dataflow`]->`Databricks`. We use Azure Databricks Notebook to perform transfomations.

<img width="1920" height="1080" alt="pipeline_run" src="https://github.com/user-attachments/assets/0fe269bb-ed93-4d4e-b951-7598f2a00c27" />


