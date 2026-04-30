---
title: Change the connection in a data fabric table
description: Connect a data fabric table to a different data source.
locale: en-US
release: zurich
product: Workflow Data Fabric Hub
classification: workflow-data-fabric-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Manage data fabric tables, Workflow Data Fabric Hub, Workflow Data Fabric]
---

# Change the connection in a data fabric table

Connect a data fabric table to a different data source.

## Before you begin

Role required: a role containing the df\_data\_steward role in both the established connection and the new connection

## Procedure

1.  Navigate to the **Data fabric tables** tab in Workflow Data Fabric Hub in one of the following ways:

    -   Navigate to **All** &gt; **Workflow Data Fabric Hub** &gt; **Data fabric tables**.
    -   Navigate to **Admin** &gt; **Workflow Data Fabric Hub** &gt; **Data fabric tables**.
2.  Find the data fabric table that you want to update.

3.  Select the More Actions icon \(![More actions icon](../../integrationhub/images/more-actions-menu-icon.png)\), and select **Change connection**.

    -   A data fabric table with multiple primary keys can only use its current connection. To change the connection, you must delete and recreate the table with the data source that you want to use.
    -   A data fabric table with a connection that still needs configuration or is deactivated can't use a different connection. You must finish configuring the connection or activate the current connection before you can change it.
4.  Choose an established connection for the data source that you want to use and select **Continue**.

5.  Select the source table with the data that you need.

6.  Map source table columns to the existing columns in the data fabric table.

7.  Select **Finish**.


**Parent Topic:**[Managing data fabric tables in Workflow Data Fabric Hub](../concept/managing-data-fabric-tables-wdf.md)

