---
title: Exploring Zero Copy Connectors
description: Discover how the Zero Copy Connectors application unifies business and technology data from multiple sources, enabling centralized, real-time access to your enterprise data without copying it to your instance.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Zero Copy Connectors, Workflow Data Fabric]
---

# Exploring Zero Copy Connectors

Discover how the Zero Copy Connectors application unifies business and technology data from multiple sources, enabling centralized, real-time access to your enterprise data without copying it to your instance.

## Zero Copy Connectors overview

The Zero Copy Connectors application provides a view where you can browse data source connectors, establish connections, and create data fabric tables that provide access to data from external sources.

-   Access enterprise data from external data warehouses including Snowflake, Google BigQuery, and Amazon Redshift, data lakes such as Databricks, and databases including Oracle.
-   Retrieve data from external sources in real time without copying any data to your instance using zero copy connections.
-   Fuel AI agents and workflows on the ServiceNow AI Platform with external data using data fabric tables.
-   Provide data to AI-powered features on the ServiceNow AI Platform, expand workflow automation, and enrich metrics and analytics with enterprise data.

## Zero Copy Connectors users

|User|Description|
|----|-----------|
|Connection admin|Establishes secure connections to external data sources by coordinating with data source administrators, managing connection credentials, and maintaining data access.|
|Data steward|Creates data fabric tables that provide access to external data, and maintains data quality to meet the business needs of data consumers.|
|Data consumer|Accesses data fabric tables to develop applications. Defines an application's data requirements and coordinates with the data steward to refine data.|

## End-to-end workflow

This infographic shows a sample end-to-end workflow of different users working together to gather requirements, establish a zero copy connection, and create a data fabric table in the Zero Copy Connectors application.

![Different users in an organization work together to define data requirements, establish a connection, and build data fabric tables for consumption. View the steps after the infographic for details.](../../../administer/workflow-data-fabric/image/mmasset0020810-workflow-data-fabric-hub-workflow-horizontal.png "Creating zero copy connections and data fabric tables")

In this workflow:

1.  A data consumer meets with a data steward and the connection admin to discuss data requirements for a new application on the ServiceNow AI Platform.
2.  The connection admin gathers the data requirements and meets with the data source admin to create a service account that can access the schema and tables needed for the new application.
3.  The connection admin establishes a secure connection to the external data lake in the Zero Copy Connector Hub using the service account credentials provided by the data source admin.
4.  The connection admin configures access controls in the connection details, ensuring the data steward can access the connection to view data assets in the external data lake and create a data fabric table.
5.  The data steward selects the established connection in the Zero Copy Connector Hub and creates a data fabric table.
6.  The data steward explores the available schema, selects a source table with the required data, and maps columns between the source table and the data fabric table.
7.  The data steward works with the data consumer to review the data fabric table and ensure that it meets the business needs of the application.
8.  The data consumer begins developing the new application and accesses the data fabric table and its external data in real time just like any table on the ServiceNow AI Platform.
9.  The data source admin monitors the external schema for consistency and communicates future schema changes to the connection admin and data steward.

## Zero Copy Connectors benefits

|Benefit|Feature|Users|
|-------|-------|-----|
|Access real-time data from external sources directly, without copying any data to your instance.|[Zero copy connections](connections-zcc.md)|Connection admin|
|Create a virtual representation of data from an outside source and make it accessible to data consumers on the instance as if it's stored locally.|[Data fabric tables](data-fabric-tables-zcc.md)|Data steward, data consumer|
|Map internal or external data to a predefined data fabric table in an application using a zero copy connection.|[Data fabric tables included with applications](mapping-application-tables-zcc.md)|Instance admin, connection admin, data steward|

## Differences between Zero Copy Connectors and Integration Hub

Choose whether to use Zero Copy Connectors or Integration Hub to integrate with external systems.

-   When you want to retrieve real-time data from external sources without storing it on your instance, use Zero Copy Connectors.
-   When you want advanced import and transformation options or customizable integrations, use Integration Hub.

## What to explore next

To learn more about configuring and using Zero Copy Connectors, see:

-   [Configuring Zero Copy Connectors](configuring-zcc.md)
-   [Managing zero copy connections](managing-connections-zcc.md)
-   [Managing data fabric tables](managing-data-fabric-tables-zcc.md)
-   [Accessing real-time data in applications](mapping-application-tables-zcc.md)
-   [Zero Copy Connectors reference](../reference/reference-zcc.md)

