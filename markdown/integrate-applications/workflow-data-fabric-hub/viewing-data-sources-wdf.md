---
title: Available connectors
description: Discover available connectors to use in a zero copy connection.
locale: en-US
release: zurich
product: Workflow Data Fabric Hub
classification: workflow-data-fabric-hub
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Explore, Workflow Data Fabric Hub, Workflow Data Fabric]
---

# Available connectors

Discover available connectors to use in a zero copy connection.

In Workflow Data Fabric Hub, you can access a variety of data sources that enable you to retrieve real-time data from across your organization using zero copy connections.

## Key benefits

-   Discover integration opportunities to external data warehouses including Snowflake, Google BigQuery, and Amazon Redshift, data lakes such as Databricks, and databases, including Oracle.
-   Access external data using primary connectors developed by ServiceNow or community connectors developed by the open-source community.
-   Create a zero copy connection to a data source, enabling data stewards to build data fabric tables.

In the Workflow Data Fabric Hub, a connection admin can navigate to the **Available connectors** tab to view primary and community connectors and create a zero copy connection. After the connection is established, the connection admin can grant access to a data steward. The data steward can then access the zero copy connection from the **Established connections** tab to create a data fabric table.

![Available connectors in Workflow Data Fabric Hub.](../image/wdf-sources.png "Available connectors in Workflow Data Fabric Hub")

## Required ServiceNow AI Platform roles

The df\_connection\_admin role is required to view available connectors.

## Accessing available connectors

View available primary and community connectors on the **Available connectors** tab by navigating to **Admin** &gt; **Workflow Data Fabric Hub** &gt; **Available connectors** or **All** &gt; **Workflow Data Fabric Hub** &gt; **Available connectors**.

## Types of connectors

A connection admin with the df\_connection\_admin role can create connections to available data sources using primary and community connectors.

-   **Primary connectors**

    Primary connectors are developed, made available, and supported by ServiceNow. Primary connectors have been enhanced to improve the performance of Glide queries and list view operations. These improvements allow the majority of queries to be executed at the data source.

-   **Community connectors**

    Community connectors are developed by the open-source community and made available by ServiceNow. These connectors are certified for essential functionality but are not part of the ServiceNow support scope.


For details on creating connections using primary connectors, see [Primary connectors](primary-connectors-wdf.md).

For details on creating connections using community connectors, see [Community connectors](community-connectors-wdf.md).

