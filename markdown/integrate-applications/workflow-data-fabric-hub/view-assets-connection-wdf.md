---
title: View data assets from an established connection
description: View the external schema and tables that are accessible to the service account used in a zero copy connection.
locale: en-US
release: yokohama
product: Workflow Data Fabric Hub
classification: workflow-data-fabric-hub
topic_type: task
last_updated: "2025-03-13"
reading_time_minutes: 1
breadcrumb: [Managing zero copy connections in Workflow Data Fabric Hub, Workflow Data Fabric Hub, Data and Automation]
---

# View data assets from an established connection

View the external schema and tables that are accessible to the service account used in a zero copy connection.

## Before you begin

Role required: df\_connection\_admin or a role containing the df\_data\_steward role

## Procedure

1.  Navigate to the **Established connections** tab in Workflow Data Fabric Hub in one of the following ways:

    -   Navigate to **All** &gt; **Workflow Data Fabric Hub** &gt; **Established connections**.
    -   Navigate to **Admin** &gt; **Workflow Data Fabric Hub** &gt; **Established connections**.
2.  Select the connection with data assets that you want to view.

3.  Select the **Data Assets** tab.

4.  Browse or search for available data assets in the schema explorer.

5.  View the data fabric tables that are currently mapped to a source table.

    1.  Select a source table in the schema explorer.

    2.  Select the **Data fabric tables** sub-tab.

6.  View the available columns in a source table.

    1.  Select a source table in the schema explorer.

    2.  Select the **Columns** sub-tab.


## What to do next

-   Identify the tables and columns that you want to map to a data fabric table.
-   Create a data fabric table and map source columns to the target table. See [Managing data fabric tables in Workflow Data Fabric Hub](../concept/managing-data-fabric-tables-wdf.md).
-   Consult with the data source administrator if the required schema and tables aren't available from this connection.

**Parent Topic:**[Managing zero copy connections in Workflow Data Fabric Hub](../concept/managing-connections-wdf.md)

