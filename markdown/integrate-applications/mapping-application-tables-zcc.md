---
title: Accessing real-time data in applications
description: Fetch real-time data using a data fabric table instead of using the physical table included with an application.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Zero Copy Connectors, Workflow Data Fabric]
---

# Accessing real-time data in applications

Fetch real-time data using a data fabric table instead of using the physical table included with an application.

## Overview of data fabric tables in applications

An application developer can package both a physical table and a predefined data fabric version of the same table within a single application. The data fabric table has the same definition and columns as the physical table, but can access external data using a zero copy connection. This gives the instance admin flexibility to choose how to populate the table. For example, the instance admin can use any of the following methods:

-   Use the physical table and enter data manually.
-   Use the physical table and import data using Integration Hub.
-   Use the predefined data fabric table to connect to an outside source and fetch external data without storing it permanently.
-   Use the predefined data fabric table to connect to a physical table on the instance and fetch data from that table without copying it permanently.

By default, a data fabric table included with an application retrieves data from a physical table in the same application using the ServiceNow local instance connector. This makes a snapshot of the latest physical table data accessible from the data fabric table in lists, forms, or scripts when needed.

The instance admin can choose to keep the predefined data fabric table connected to its physical table or change the connection to retrieve external data or data from a different physical table.

Connecting to an external data source using requires coordination between the instance admin, connection admin, and data steward. To configure this type of data fabric table, follow the process shown in this infographic.

![Different users in an organization work together to connect an application table to an external data source. View the steps after the infographic for details.](../../../administer/workflow-data-fabric/image/mmasset0021028-connecting-a-data-fabric-table-in-an-application-to-external-source-horizontal.png "Connecting a predefined data fabric table to an external data source")

In this workflow:

1.  The connection admin creates a connection to an external source and enables the data steward to access the connection.
2.  The data steward works with the instance admin to learn about the data requirements of the application.
3.  The data steward connects the data fabric table from the application to an external source using the provided connection.
4.  The data steward selects a source table and maps source columns to the existing columns in the data fabric table.
5.  Users access the application, and interact with flows retrieving data from the external source in real-time.

-   **[Connect a predefined data fabric table to an external data source](../task/map-application-table-external-zcc.md)**  
Connect a data fabric table included with an application to an external data source.
-   **[Connect a predefined data fabric table to a local table](../task/map-application-table-internal-zcc.md)**  
Connect a data fabric table included with an application to a local table on your instance.

**Parent Topic:**[Zero Copy Connectors](zero-copy-connectors.md)

