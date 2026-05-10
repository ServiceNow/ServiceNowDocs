---
title: Data fabric tables
description: Fuel your AI agents and enrich workflows on the ServiceNow AI Platform with external data using data fabric tables.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Explore, Zero Copy Connectors, Workflow Data Fabric]
---

# Data fabric tables

Fuel your AI agents and enrich workflows on the ServiceNow AI Platform with external data using data fabric tables.

## Key benefits

-   Fetch external data in real time and view the data in lists and forms as if it's stored in your instance.
-   Reduce storage consumption and performance load in your instance.
-   Control access to external data so that only authorized users can view the data.

A data fabric table is a virtual representation of data stored in an external source, accessible directly from the ServiceNow AI Platform. The data fabric table definition is stored in the ServiceNow AI Platform, but its external records live in the memory in read-only mode. You can view external records from a data fabric table in lists and forms the same way you view records in a physical table.

Access to a data fabric table is controlled the same way access is controlled to a physical table. Data fabric tables belong to the application scope selected by the data steward during their creation.

![A list of your data fabric tables.](../image/zcc-data-fabric-table.png "Data fabric tables")

## Required ServiceNow AI Platform roles

A role containing the df\_data\_steward role or the connection\_admin role is required to create and manage data fabric tables.

## Accessing data fabric tables

View and manage data fabric tables on the **Data fabric tables** tab by navigating to **Admin** &gt; **Zero Copy Connector Hub** &gt; **Data fabric tables** or **All** &gt; **Zero Copy Connector Hub** &gt; **Data fabric tables**.

## Viewing data fabric tables

View a list of all the data fabric tables that data stewards have created on the **Data fabric tables** tab.

-   Search for a data fabric table by label or name.
-   Filter the list of tables by data source and connection.
-   Filter the list of tables by creator.
-   View a list of data fabric tables from active connections in the **Active** tab.
-   View a list of data fabric tables from connections that are deactivated or not configured in the **Others** tab.

## Use cases

-   **Unifying data from multiple sources**

    A manufacturer experiences an outage when a key piece of machinery fails, stopping production entirely. Unfortunately, the data needed to help prevent these failures is scattered across multiple systems.

    -   Asset inventory data in IT Asset Management \(ITAM\) and maintenance personnel data are stored locally in your instance.
    -   Historical asset maintenance records and real-time sensor are stored in an external data lake.
    To help prevent potential failures and outages, you can provide service technicians with all the necessary data by connecting these systems using data fabric tables. For example:

    1.  Sensor data is fed to the data lake and analyzed by machine learning, generating a failure score.
    2.  When the failure score crosses a certain threshold, an alert is generated and sent to your instance.
    3.  The alert triggers a maintenance request flow, creating a case assigned to a service technician.
    4.  The technician reviews the case details and accesses inventory data from the instance, along with maintenance records and real-time sensor data from the external data lake, all in one place using data fabric tables.
    5.  The technician makes an informed decision and acts to address the issue before another outage occurs.
-   **Retrieving real-time data in an application**

    An application can include both a physical table and a data fabric version of the same table. This gives the instance admin flexibility when installing the application. The admin can choose whether to populate the physical table through data import or allow users to access real-time data from an external data source via the data fabric table.

-   **Analyzing data and generating AI-guided insights using AI Data Explorer**

    Create visualizations and analyses of fetched data through a conversational interface in AI Data Explorer. For more information, see [Use AI to explore data with AI Data Explorer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/now-assist-explorer.md).

    **Note:** You must first add the relevant data fabric tables to the Semantic Table Configuration \[sn\_query\_gen\_table\_config\] table in Query Generation. See [Add a table to the semantic data layer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/add-table-semantic-layer.md).

-   **Enhancing the performance of AI experiences using the Knowledge Graph**

    Enhance the performance of Now Assist Virtual Agent, AI agents, and generative AI skills by leveraging data fabric tables in the Knowledge Graph application. For more information, see [Knowledge Graph](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/knowledge-graph/knowledge-graph-landing.md).


## Differences between data fabric tables and remote tables

Data fabric tables are similar to remote tables on the ServiceNow AI Platform, but data fabric tables query external data sources and retrieve data using a zero copy connection instead of a script.

A data fabric table enables you to view external data, but you can't insert, update, or delete data in an external data source like you can from a remote table.

