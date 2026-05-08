---
title: Build a Service Mapping query using the CMDB Query Builder
description: The Service Mapping query type is a pattern consisting of classes and relationships between those classes. After you build the pattern and run the query, the query returns all the Service Mapping services that contain that pattern.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [CMDB Query Builder, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Build a Service Mapping query using the CMDB Query Builder

The Service Mapping query type is a pattern consisting of classes and relationships between those classes. After you build the pattern and run the query, the query returns all the Service Mapping services that contain that pattern.

## Before you begin

Role required: cmdb\_query\_builder\_read to only view and run saved queries, and cmdb\_query\_builder to create and save queries, modify saved queries, and run queries.

Authorized users can update and [delete](delete-cmdb-query.md) a query created by another user.

## About this task

Build the query by dragging the CI classes that you want to include in the query, dropping them as nodes on the canvas, and then defining relationship properties between them. For every class node in the query, you can filter on its attributes to narrow down the results to a specific set of CIs of that class or to a single specific CI. You can also select which property columns appear in the query results.

As you step through building a query, list options and other user interface elements of the CMDB Query Builder, are dynamically filtered as appropriate to your selections.

See [Example queries](../concept/sample-queries.md) for a step-by-step walk through of building a Service Mapping query in the CMDB Query Builder.

## Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **CMDB Query Builder**.

2.  On the **CMDB Query Builder** page do either of the following:

    1.  Select **Create new**.

    2.  Enter a **Name**.

    3.  Select **Service Mapping Query** as the **Query type**.

    4.  Select **Create**.

    5.  Select a widget of a saved query to continue building an existing query. [Search for a saved query](search-saved-queries.md) first if needed.

    6.  Point to the upper right corner of a saved query widget.

    7.  Select the **Duplicate Query** icon to edit a copy of a saved query.

        The new query's default name contains the string 'copy'.

3.  On the canvas, you can do any of the following:

    -   Add CI classes to the query: Select classes from the **CMDB Classes** hierarchy list and drag them to the canvas.
    -   Add connections \(relationships\) between two nodes on the canvas:

        1.  On the first node in the relationship, select the small square at the center of the right side.
        2.  On the second node in the relationship, select the small square at the center of the left side to create the connection.
        3.  In **Connection Properties** on the right-side bar, configure the following \(select the connection line if necessary\):
            -   In the Relationship Direction section, select the **Parent** node \(the **Child** node automatically adjusts\).
            -   In the Service Query Properties section, select **Find Related CIs** or **Find Unrelated CIs** to query for a pattern in which the two classes have or do not have relationships with each other, respectively.

                For example, `All Tomcat WAR CIs which are not connected to a Windows Server`.

        |Notation|Description|
        |--------|-----------|
        |Dashed line|A relationship in a Service Mapping query.|

    -   Add filters to a class node: Apply filters to narrow down a class to a specific set of CIs or to a single specific CI.

        1.  Point to the node to add a filter to, and then select the **Apply filters** icon that pops up above the node.
        2.  In the Filters section, add attribute and related list conditions.
        3.  Close the **Filters** section.
        For example: Add a filter for business criticality to query for businesses that are 'most critical'.

        Select **Applied Filters** in the right-side bar to view all filters for each node on the canvas.

    -   Add And/Or operators to the query:

        1.  Connect one node to two other nodes.
        2.  Select the **And** box that appears on the connection line, to toggle between the **And** and the **Or** operators.
        For example C1 is Tomcat WAR, C2 is Linux Server, and C3 is Windows Server. Query for all Tomcat WAR CIs which are connected either to Linux Server Or to a Windows Server.

    -   Add property columns for a node, to display in the query results:

        **Note:** For a relationship, the query results display the **parent**, **child**, and **type** columns. You cannot add any other columns from the \[cmdb\_rel\_ci\] table.

        1.  Select **Properties** in the right-side pane.
        2.  Select a node once or twice, so that the node's Report Columns section appears in the right-side bar, and then select **Add Columns**.
        3.  Select properties and then select outside the properties list to close it.
    -   Select columns and add filters that will be applied to the resulting set of services:
        1.  Select **Properties** in the right-side bar, and then select an empty space on the canvas to ensure that nothing is selected.
        2.  Select **Add Columns** at the bottom of the right-side bar and select columns to add. Select outside the columns list to close it.
        3.  Select the **Apply Service Mapping Query Filters** icon at the top of the canvas and add filters.
    -   Inverse the entire query and search for all Service Mapping services that do not include the query pattern: Select a node once or twice so that Query Properties appear in the right-side bar. In the Metadata section, toggle **Services Including This Pattern** to enable or disable the option.
    -   Add a search tag that can then be used as a search criteria for saved queries:
        1.  Select the **Add Tags** icon at the top of the canvas.
        2.  Select **Add Tag** and in the **Query Tags** dialog box enter one or more tag strings.
        3.  Select the **Add Tags** icon again to close the **Query Tags** dialog box.
4.  Select **Save**.

    On the **Saved Queries** tab, point to a saved query widget and select **Query Information** to view query details such as the query type, last update date, and the query schedules.


## What to do next

-   Select **Run**.

    The query results pane displays only the first 100 results of the query.

    -   Select **Load More Results** to display the next set of 100 results.
    -   Select **Load All Results** to display the rest of the query results, up to the number specified by the [glide.cmdb.query.max\_results\_limit](../reference/cmdb-querybldr-sysproprties.md) system property \(10,000 by default\).
    Select a CI to open its CI form, and on the CI form select **Open in CMDB Workspace** to view CI health in the CI Health tile in CMDB Workspace. This operation requires the sn\_cmdb\_user \(CMDB user\) role.

    **Note:** When a query is running, wait for it to complete or to time out before opening or running another query.

-   [Modify Query Builder settings](cmdb-querybldr-config-display.md): Select the Settings icon to open the **Query Builder Settings** dialog box.
-   Copy and share the URL of a saved query with users that have access to the CMDB Query Builder. Pasting the shared URL in a new internet browser window, directly opens the saved query in the CMDB Query Builder.
-   [Create a report in CMDB Query Builder](../concept/create-query-results-report.md).
-   [Create a schedule](create-cmdb-query-schedule.md) to run the query at a future time, and to email the results to interested parties.
-   Export query results:

    Export query results that are visible: Select the Query Results context menu and select **Export**. Even if the **Load More Results** button is visible, indicating that there are additional query results, only the results that are visible are exported.

-   [Export and import a CMDB query](export-import-query.md) to port a query definition between instances.
-   [Populate a CMDB group](../concept/cmdb-groups.md#) using the saved query.
-   [Delete a CMDB query](delete-cmdb-query.md).

**Related topics**  


[Example queries](../concept/sample-queries.md)

