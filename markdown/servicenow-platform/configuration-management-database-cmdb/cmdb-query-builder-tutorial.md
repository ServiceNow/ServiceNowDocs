---
title: CMDB — Servers connected to a database
description: Use this example to build a CMDB query to find all servers with a connection to a database.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Example queries, Reference, CMDB Query Builder, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CMDB — Servers connected to a database

Use this example to build a CMDB query to find all servers with a connection to a database.

## Before you begin

Role required: none

## Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **CMDB Query Builder**.

2.  Select **Create new** and then enter a name, for example `All servers with a connection to a DB`.

3.  Choose **CMDB Query** and then select **Create**.

4.  In the **CMDB Classes** list, locate the **Server** class and drag it to the canvas.

    **Tip:** Use the search box to find items quickly.

5.  Locate the **Database** class, and place it to the right of the **Server** class node on the canvas.

6.  Select at the center of the right side of **Server**, and then at the center of the left side of **Database** to create a connection line between the two class nodes.

7.  Select once or twice on the connection line until the Connection Properties panel appears in the sidebar.

8.  In the Relationship Types and Related Items section, select **Add Relationship Types** and add all the relationships from the list.

    ![Connecting the Server and the Database nodes and adding relationship types.](../image/QuerySample.png)

    Settings in the Relationship Direction section reflect the parent-child direction in the relationship. If the Database class is the parent in the relationship, then the **Parent** and **Child** settings are switched.

9.  Select **Save**, and then select **Saved Queries** on the left to see the widget for the saved query.

10. Select the query widget to return to the canvas in edit mode.

11. Select **Run** to execute the query.

    Review the query results. Each row displays the name of a server CI, the name of a database CI, and the relationship type between them.

12. Add columns to the query results.

    1.  Select the **Server 1** node on the canvas once or twice so that the Server 1 Report Columns section appears in the right-side pane.

    2.  Select **Add Columns**.

    3.  Select **Manufacturer** and then select outside the columns list to close it.

    4.  Select **Run**.

        The query results now include the **Manufacturer** column.

    5.  Select **Save** again to save your customization for this query.


