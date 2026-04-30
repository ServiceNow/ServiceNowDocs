---
title: Connect a predefined data fabric table to an external data source
description: Connect a data fabric table included with an application to an external data source.
locale: en-US
release: zurich
product: Workflow Data Fabric Hub
classification: workflow-data-fabric-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Access real-time data, Workflow Data Fabric Hub, Workflow Data Fabric]
---

# Connect a predefined data fabric table to an external data source

Connect a data fabric table included with an application to an external data source.

## Before you begin

-   Work with the instance admin or application admin to identify the data fabric table that needs data from an external source.
-   Work with the connection admin to create a connection to the external source or request access to an established connection.

Role required: a role containing the df\_data\_steward role

## About this task

You can fetch data from an external source using an application's data fabric table, instead of using the application's physical table. By using the data fabric table, users can access external data in real time, rather than accessing data that has been imported and stored in a physical table.

## Procedure

1.  Navigate to the **Data fabric tables** tab in the Workflow Data Fabric Hub in one of the following ways:

    -   Navigate to **All** &gt; **Workflow Data Fabric Hub** &gt; **Data fabric tables**
    -   Navigate to **Admin** &gt; **Workflow Data Fabric Hub** &gt; **Data fabric tables**.
2.  Find the data fabric table that you want to update.

3.  Connect the table to an external data source.

    1.  Select the More Actions icon \(![More actions icon](../../integrationhub/images/more-actions-menu-icon.png)\), and select **Change connection**.

    2.  On the Select a connection page, select the established connection provided by the connection admin.

    3.  Select **Continue**.

    A tree view of data assets appears, listing the available schema and tables in the external data source.

4.  In the list of data assets, select the table that you want to fetch data from and select **Continue**.

5.  Map source columns to each target column in the data fabric table.

    Because the data fabric table is predefined and belongs to an application, you can't add or remove columns when mapping data. The columns in the data fabric table are fixed.

    1.  Review the label, name, and data type for each column in the target table.

    2.  Select a source column with a matching data type for each target column.

6.  Select **Finish**.


## Result

The data fabric table is connected to the data source that you selected, with the field mapping you defined. Application users can access data from the data source in real time as if it's stored locally on the instance.

**Parent Topic:**[Accessing real-time data in applications](../concept/mapping-application-tables.md)

