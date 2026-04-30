---
title: Connect a predefined data fabric table to a local table
description: Connect a data fabric table included with an application to a local table on your instance.
locale: en-US
release: zurich
product: Workflow Data Fabric Hub
classification: workflow-data-fabric-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Access real-time data, Workflow Data Fabric Hub, Workflow Data Fabric]
---

# Connect a predefined data fabric table to a local table

Connect a data fabric table included with an application to a local table on your instance.

## Before you begin

Identify the local table that you want to retrieve data from using the ServiceNow local instance connector.

Role required: a role containing the df\_data\_steward role

## About this task

You can connect a data fabric table included with an application to a different physical table on your instance. After changing the connection, you can reuse the data from the physical table in your data fabric table.

## Procedure

1.  Navigate to the **Data fabric tables** tab in the Workflow Data Fabric Hub in one of the following ways:

    -   Navigate to **All** &gt; **Workflow Data Fabric Hub** &gt; **Data fabric tables**
    -   Navigate to **Admin** &gt; **Workflow Data Fabric Hub** &gt; **Data fabric tables**.
2.  Find the data fabric table that you want to update.

3.  Connect the table to a different local table on the instance.

    1.  Select the More Actions icon \(![More actions icon](../../integrationhub/images/more-actions-menu-icon.png)\), and select **Change connection**.

    2.  On the Select a connection page, select the **ServiceNow local instance** connection.

    3.  Select **Continue**.

    A tree view of data assets appears, listing the local applications and tables.

4.  In the list of data assets, select the table that you want to fetch data from and select **Continue**.

5.  Map source columns to each target column in the data fabric table.

    Because the data fabric table is predefined and belongs to an application, you can't add or remove columns when mapping data. The columns in the data fabric table are fixed.

    1.  Review the label, name, and data type for each column in the target table.

    2.  Select a source column with a matching data type for each target column.

6.  Select **Finish**.


## Result

The data fabric table is connected to the local table that you selected using the ServiceNow local instance connector. Application users can access real-time data from the local table using the data fabric table.

**Parent Topic:**[Accessing real-time data in applications](../concept/mapping-application-tables.md)

