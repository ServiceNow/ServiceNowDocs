---
title: Debug performance diagnostics of a catalog item
description: Analyze the impact of the variable setup in a catalog item on its runtime performance, and identify any issues. You can review the processing time of the catalog item and its variables based on the triggered SQL queries.
locale: en-US
release: xanadu
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Debugging Service Catalog, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Debug performance diagnostics of a catalog item

Analyze the impact of the variable setup in a catalog item on its runtime performance, and identify any issues. You can review the processing time of the catalog item and its variables based on the triggered SQL queries.

## Before you begin

Role required: admin or catalog\_admin

## About this task

The variable SQL debugger is not applicable for the following variables:

-   Container Start
-   Container End
-   Container Split
-   Break

## Procedure

1.  Enable the variable SQL debugger by navigating to **Service Catalog** &gt; **Catalog Variables** &gt; **Enable Variable SQL Debugger**.

    **Note:**

    -   The variable SQL debugger is applicable for catalog items and record producers.
    -   After you enable the variable SQL debugger, if you disable the display of the troubleshooting information on a catalog page by navigating to **System Diagnostics** &gt; **Session Debug** &gt; **Disable All**, the variable SQL debugger is still active.
    -   To disable the variable SQL debugger, navigate to **Service Catalog** &gt; **Catalog Variables** &gt; **Disable Variable SQL Debugger**.
2.  Navigate to **Service Catalog** &gt; **Catalog Definitions** &gt; **Maintain Items**, select a catalog item that you want to debug, and click **Try It**.

3.  Click the more options icon \(![more options icon](../image/Actions.png)\) and select **Show Variable SQL Debugger**.

    The following information is displayed in the Variable SQL Debugger window:

    -   Number of variables included in the catalog item.
    -   Number of SQL queries triggered for the catalog item.
    -   Time taken to process and load the catalog item page.
    -   Time taken to run all SQL queries of the catalog item.
    |Field|Description|
    |-----|-----------|
    |Variable|Catalog item variable for which the performance diagnostics are displayed.|
    |Processing Time|Time taken to process and load the variable.|
    |SQL Count|Number of SQL queries triggered for the variable.|
    |SQL Time|Time taken to run SQL queries for the variable.|
    |SQLs|Details of the SQL queries triggered for the variable.|

4.  To sort by any field, click the field name.

    **Note:**

    -   By default, variables are sorted in descending order by their processing time.
    -   Variables within a single-row or multi-row variable set are displayed in hierarchical order.
5.  To view the configuration of a variable, click the variable name.

6.  To view a detailed summary of all SQL queries triggered for a variable, click **View Details** in the **SQLs** field of the variable.

7.  To change the sort order, Use the **Sort By** list.

    **Note:** By default, triggered SQLs are sorted in descending order by their execution order.


**Parent Topic:**[Debugging Service Catalog](../concept/debugging-service-catalog.md)

