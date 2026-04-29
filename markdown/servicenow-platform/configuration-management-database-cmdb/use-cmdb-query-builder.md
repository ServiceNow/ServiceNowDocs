---
title: Build a CMDB query using the CMDB Query Builder
description: A CMDB query type that queries the infrastructure for CI classes and optionally non-CMDB tables, and the relationships and references that connect them.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [CMDB Query Builder, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Build a CMDB query using the CMDB Query Builder

A CMDB query type that queries the infrastructure for CI classes and optionally non-CMDB tables, and the relationships and references that connect them.

## Before you begin

Role required: cmdb\_query\_builder\_read to only view and run saved queries, and cmdb\_query\_builder to create and save queries, modify saved queries, and run queries. For reporting on queries, report related ACLs are required.

Authorized users can update and [delete](delete-cmdb-query.md) a query created by another user.

## About this task

Build the query by dragging the CI classes and non-CMDB tables that you want to include in the query. Then dropping them as nodes on the canvas, and defining relationship properties between them. You can filter on the attributes of any node to narrow down the results to a specific set of CIs of that class or to a single specific CI. You can also select which property columns appear in the query results.

As you step through building a query, list options and other user interface elements of the CMDB Query Builder, are dynamically filtered as appropriate to your selections.

To learn more about using Query Builder, see the [CMDB Query Builder Queries and Reporting - Platform Analytics Academy](https://www.youtube.com/watch?v=NArqszOamHc) ServiceNow Community video. For a step-by-step walk through of building CMDB queries in the Query Builder, including queries with application services, see [Example queries](../concept/sample-queries.md).

## Procedure

1.  Navigate to **All** &gt; **Configuration** and select **CMDB Query Builder**.

2.  On the **CMDB Query Builder** page do either of the following steps:

    -   Select **Create new**. Type in a **Name**, choose **CMDB Query** as the **Query type**, and then select **Create**.
    -   Select a widget of a saved query to continue building an existing query. [Search for a saved query](search-saved-queries.md) first if needed.
    -   Point to the upper right corner of a saved query widget, and select the **Duplicate Query** icon to edit a copy of a saved query. The default name of the new query contains the string 'copy'.
3.  On the canvas, you can do any of the following operations:

    -   Add CI classes to the query: On the **CMDB Classes** tab, select classes from the hierarchy list and drag them to the canvas.
    -   Add an Application Service CI to the query: On the **CMDB Classes** tab, select the **Application Service** class from the hierarchy list and drag it to the canvas.

        In Application Service Properties on the right-side bar, you can select **Convert attached nodes to pattern** to query on patterns between the application service and other CMDB class nodes. When querying on a pattern, the nodes on both ends of the pattern connection, can be any number of levels apart. If **Convert attached nodes to pattern** is not selected, then the connection between the application service node and other CMDB class nodes, represent direct relationships.

    -   Add non-CMDB tables to the query: Select a table from the **Non-CMDB Tables** list and drag it to the canvas.

        **Note:** A non-CMDB table cannot be the starting node in the query.

    -   Add connections \(relationships or patterns for application services\) between two nodes on the canvas:

        1.  On the first node in the connection, select the small square at the center of the right side.
        2.  On the second node in the connection, select the small square at the center of the left side to create the connection.
<table id="table_ipf_qw5_plb"><thead><tr><th>

Notation

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Full line

</td><td>

A relationship in a CMDB query.

</td></tr><tr><td>

Red asterisk at the center of the connection line

</td><td>

Information such as relationship type is missing, invalidating the query.

</td></tr><tr><td>

**Levels:&lt;n&gt; Types:&lt;n&gt;** or a **&lt;Reference type&gt;** notation on the connection line

</td><td>

As applicable: The number of relationship levels and the number of relationship types included for the connection. Or, a reference type for a relationship that is a reference.

</td></tr><tr><td>

Dashed line

</td><td>

A pattern connection between an application service node and another node.

</td></tr></tbody>
</table>    -   In Connection Properties on the right-side bar, configure relationship settings \(select the connection line if necessary\):
        1.  In the Relationship Direction section, select the **Parent** node \(the **Child** node automatically adjusts\).
        2.  In the Relationship Levels section, set **Level** to **First level relationships** if the CIs are directly connected. Or, **Up to 2nd level relationships** if the CIs are connected either directly or indirectly through another CI.
        3.  In the Relationship Types and Related Items section, select either option:

            |Option|Description|
            |------|-----------|
            |**No Relationships**|To query for CIs with no connecting relationships, such as `All Tomcat WAR CIs which are not connected to a Windows Server`.|
            |**Add Relationship Types**|To select specific or any relationship type.|
            |**Add a Related Item**|To query for related CIs between the nodes.|

    -   Configure CI reference column for a connection to a non-CMDB table: In the Connection Properties right-side bar, in the CI Reference Column section, select the column with a reference to a CI from the **Use CI reference column** list. If only one option is available, it is automatically selected.
    -   Configure the pattern between an application service node set with the **Convert attached nodes to pattern** option, and a non-CMDB table node: Select **Apply &lt;table&gt; reference filter to all nodes in the pattern** to apply the query to the application service CI itself and to the CIs within the application service.
    -   Add filters to a class node: Apply filters to narrow down a class query to a specific set of CIs or to a single specific CI.

        1.  Point to the node to add a filter to, and then select the **Apply filters** icon that pops up above the node.
        2.  In the Filters section, add attribute and [related list conditions](https://www.servicenow.com/docs/access?context=create-related-list-query&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).
        3.  Close the **Filters** section.
        For example: Add a filter for database location to query for databases located in Seattle.

        Select **Applied Filters** in the right-side bar to view all filters for each node on the canvas.

    -   Add And/Or operators to the query:

        1.  Connect one node to two other nodes.
        2.  Select the **And** box that appears on the connection line, to toggle between the **And**/**Or** operators.
        For example: C1 is Tomcat WAR, C2 is Linux Server, and C3 is Windows Server. Query for `All Tomcat WAR CIs which are connected either to Linux Server Or to a Windows Server`.

    -   Add property columns for a node, to appear in the query results:

        **Note:** For a relationship, the query results include the **parent**, **child**, and **type** columns. You cannot add any other columns from the \[cmdb\_rel\_ci\] table.

        1.  Select **Properties** in the right-side pane.
        2.  Select a node once or twice, so that the Report Columns section appears in the right-side bar, and then select **Add Columns**.
        3.  Select properties and then select outside the properties list to close it.
    -   Create a combination query by integrating a Service Mapping query into a CMDB query:

        1.  When building a CMDB query, select **Saved Service Queries** in the left-side bar.
        2.  Select and then drag a Service Mapping query to the canvas.
        This query returns all CIs that satisfy the CMDB query, and that are included in the services returned by the embedded Service Mapping query.

    -   Add a search tag that can then be used as a search criteria for saved queries:
        1.  Select the **Add Tags** icon at the top of the canvas.
        2.  Select **Add Tag** and in the **Query Tags** dialog box enter one or more tag strings.
        3.  Select the **Add Tags** icon again to close the **Query Tags** dialog box.
4.  Select **Save**.

    On the **Saved Queries** tab, point to a saved query widget and select **Query Information**. Query details such as the query type, last update date, CMDB groups associated with the query, and the query schedules appear.


## What to do next

-   Select **Run**.

    Only the first 100 results of the query appear in the results pane.

    -   Select **Load More Results** to view the next set of 100 results.

        **Note:** This option is available only with the V1 engine execution mode. For more information about CMDB Query engine execution modes, see [Set execution mode for running a query](config-query-builder-engine-mode.md).

    -   Select **Load All Results** to view the rest of the query results, up to the number specified by the [glide.cmdb.query.max\_results\_limit](../reference/cmdb-querybldr-sysproprties.md) system property \(10,000 by default\).
    Select a CI to open its CI form, and on the CI form select **Open in CMDB Workspace** to view CI health in the CI Health tile in CMDB Workspace. This operation requires the sn\_cmdb\_user \(CMDB user\) role.

    **Note:**

    -   Ensure that the [glide.security.use\_csrf\_token](../../../administer/login/reference/win-security-properties-password-reset.md) property is set to true, allowing all results to appear.
    -   When **Level** is set to **Up to 2nd level relationships**, the relationship type does not appear in the query results.
    -   When a query is running, wait for it to complete or to time out before opening or running another query.
-   [Modify Query Builder settings](cmdb-querybldr-config-display.md): Select the Settings icon to open the **Query Builder Settings** dialog box.
-   Copy and share the URL of a saved query with users that have access to the CMDB Query Builder. Pasting the shared URL in a new internet browser window, directly opens the saved query in the CMDB Query Builder.
-   [Create a report in CMDB Query Builder](../concept/create-query-results-report.md).
-   [Create a schedule](create-cmdb-query-schedule.md) to run the query at a future time, and to email the results to interested parties.
-   Export query results:

    Select the Query Results context menu and select **Export**. Even if the **Load More Results** button is visible, indicating that there are additional query results, only the results that are visible are exported.

-   [Export and import a CMDB query](export-import-query.md) to port a query definition between instances.
-   [Populate a CMDB group](../concept/cmdb-groups.md#) using a saved query.
-   [Delete a CMDB query](delete-cmdb-query.md).

**Related topics**  


[Example queries](../concept/sample-queries.md)

