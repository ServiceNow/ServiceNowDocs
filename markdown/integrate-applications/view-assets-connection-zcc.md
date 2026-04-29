---
title: View data assets from an established connection
description: View the external schema and tables that are accessible to the service account used in a zero copy connection.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Manage zero copy connections, Zero Copy Connectors, Workflow Data Fabric]
---

# View data assets from an established connection

View the external schema and tables that are accessible to the service account used in a zero copy connection.

## Before you begin

Role required: df\_connection\_admin or a role containing the df\_data\_steward role

## Procedure

1.  Navigate to the **Established connections** tab in Zero Copy Connector Hub in one of the following ways:

    -   Navigate to **All** &gt; **Zero Copy Connector Hub** &gt; **Established connections**.
    -   Navigate to **Admin** &gt; **Zero Copy Connector Hub** &gt; **Established connections**.
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
-   Create a data fabric table and map source columns to the target table. See [Managing data fabric tables](../concept/managing-data-fabric-tables-zcc.md).
-   Consult with the data source administrator if the required schema and tables aren't available from this connection.

**Parent Topic:**[Managing zero copy connections](../concept/managing-connections-zcc.md)

