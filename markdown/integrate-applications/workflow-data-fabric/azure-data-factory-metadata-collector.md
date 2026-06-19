---
title: Azure Data Factory metadata collector
description: The Azure Data Factory metadata collector provides read-only access to metadata from an external Azure Data Factory account.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/workflow-data-fabric/azure-data-factory-metadata-collector.html
release: australia
product: Workflow Data Fabric
classification: workflow-data-fabric
topic_type: concept
last_updated: "2026-04-01"
reading_time_minutes: 2
breadcrumb: [Configuring metadata collectors, Data Catalog, Workflow Data Fabric]
---

# Azure Data Factory metadata collector

The Azure Data Factory metadata collector provides read-only access to metadata from an external Azure Data Factory account.

Use this collector to harvest metadata from ADF, including pipelines, datasets, dataflows, linked services, triggers, integration runtimes, and global parameters. It gathers lineage information between ADF datasets and between ADF and external sources such as Snowflake.

## Metadata cataloged

The Azure Data Factory collector catalogs the following information.

<table id="table_frb_vjb_xhc"><thead><tr><th>

Object

</th><th>

Information cataloged

</th></tr></thead><tbody><tr><td>

Factory

</td><td>

ID, Name, ETag, Location, Create Time, Provisioning State, Version, Public Network Access, Factory Tags, Repository configuration \(Account name, Collaboration Branch, Repository Name, Disable Publish, Root Folder, Host Name, Client ID, Project Name, Last Commit ID, Tenant ID, Repo Configuration Type\).

</td></tr><tr><td>

Pipeline

</td><td>

ID, Name, Description, Etag, Concurrency, Folder, Parameters, Metric Policy Duration, Variables

</td></tr><tr><td>

Pipeline Activity

</td><td>

Name, Description, Type, Inactivity Status, State, User Properties, Activity Policy \(Retry, Timeout, Retry Interval In Secs, Secure Input, Secure Output\)

</td></tr><tr><td>

Linked Service

</td><td>

ID, Name, Description, Type, Etag, Connection String, Domain, Parameters **Note:** Harvesting of Connection String for SFTP Linked Services is not supported.

</td></tr><tr><td>

Dataset

</td><td>

ID, Name, Etag, Type, Database, Schema, Table, Folder, Container, File Name, Parameters

</td></tr><tr><td>

Dataflow

</td><td>

ID, Name, Etag, Type, Description, Folder

</td></tr><tr><td>

Trigger

</td><td>

ID, Name, Etag, Type, State, Description, Frequency, Interval, Start time, End time

</td></tr><tr><td>

Integration Runtime

</td><td>

ID, Etag, Name, Type, Description, State Compute Properties \(Node Size, Number of Nodes, Max Parallel Execution Per Node, Core Count, Compute Type, Clean up, Number of External Nodes, Number of Pipeline Nodes\), SSIS properties \( Catalog Server Endpoint, Catalog Admin Username, Catalog Pricing Tier, License Type, Dual Standby PairName, Edition\)

</td></tr><tr><td>

Global Parameter

</td><td>

ID, Name, Value, Type

</td></tr><tr><td>

ADF Table

</td><td>

ID, Name

</td></tr><tr><td>

ADF Column

</td><td>

ID, Name, Type, Precision, Scale

</td></tr><tr><td>

Pipeline Activity

</td><td>

Query

</td></tr></tbody>
</table>## Relationships between objects

Catalog pages show relationships between the following data asset types:

|Data asset page|Relationship|
|---------------|------------|
|Factory|Contains Global Parameter, Contains Pipeline, Contains Dataset, Contains Dataflow, Contains Trigger, Contains Integration Runtime|
|Pipeline|Has Tag \(also known as Annotation\), Contains Activity|
|Activity|Belongs to Pipeline, Contains Activity, Depends on Activity, uses Linked Service, uses Integration Runtime, uses Dataset|
|Linked Service|Uses Integration Runtime, Has Tag \(also known as Annotation\), Connects to database|
|Dataset|Uses Linked Service, Has Tabular Datasource, Has Tag \(also known as Annotation\)|
|Dataflow|Uses Dataflow, Imports Data From Linked Service, Exports Data From Linked Service, Imports Data From Dataset, Exports Data From Dataset, has Tag \(also known as Annotation\)|
|Integration Runtime|Uses Integration Runtime, Uses Linked Service|
|Trigger|Triggers Pipeline, Has Tag \(also known as Annotation\)|

## Lineage for Azure Data Factory

Collected lineage information:

<table id="table_z42_zvb_xhc"><thead><tr><th>

Object

</th><th>

Lineage available

</th></tr></thead><tbody><tr><td>

Dataset

</td><td>

The collector identifies the source or sink of the dataset: -   when the source/sink is Snowflake, Databricks, PostgreSQL, MySQL, Oracle, Teradata, DB2, and SQLServer.
-   when there is a Copy Activity Run copying data between two datasets.

</td></tr><tr><td>

ADF table

</td><td>

The collector identifies the associated table in an upstream table where the data is sourced from/sinked to.

</td></tr><tr><td>

ADF column

</td><td>

The collector identifies the associated table in an upstream column where the data is sourced from/sinked to.

</td></tr></tbody>
</table>Supported data sources for cross-system lineage:

-   Snowflake
-   Databricks

## Authentication types supported

The Azure Data Factory collector authenticates using Azure Service Principal.

-   **[Prepare to run the Azure Data Factory collector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/prepare-to-run-azure-data-factory-collector.md)**  
Set up Azure data assets, authentication, and permissions before running the collector.
-   **[Create an Azure Data Factory metadata collector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/create-azure-data-factory-metadata-collector.md)**  
Create a collector to import metadata from Azure Data Factory.

**Parent Topic:**[Configuring metadata collectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/configure-metadata-collectors-dc.md)

