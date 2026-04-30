---
title: Connect Power BI Desktop to ODBC driver
description: Connect Power BI Desktop to your ServiceNow instance using the ODBC driver to access and analyze ServiceNow data. Create dashboards and reports that visualize your ServiceNow data.
locale: en-us
release: zurich
product: Web Services
classification: web-services
topic_type: task
last_updated: "2026-03-04"
reading_time_minutes: 2
breadcrumb: [Integrate, Access your ServiceNow data using SQL API, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Connect Power BI Desktop to ODBC driver

Connect Power BI Desktop to your ServiceNow instance using the ODBC driver to access and analyze ServiceNow data. Create dashboards and reports that visualize your ServiceNow data.

## Before you begin

Verify the following prerequisites are in place:

-   The SQL API plugin is installed on your ServiceNow instance.
-   The ServiceNow ODBC driver is installed and configured on your client machine.
-   You have a Service Account with the **sn\_odbc\_rest\_access** role assigned.
-   Access Control Lists \(ACLs\) are configured for the tables you must query.
-   IP filter criteria are configured to allow connections from your client machine.

Role required: admin

## About this task

**Important:**

Step-by-step instructions for external tools in this guide are illustrative — you must consult tool-specific documentation for latest updates. Power BI Desktop is solely used as an example in this guide.

This connection enables you to query ServiceNow data directly without requiring data export or replication, and allows you to combine ServiceNow data with other data sources in your analysis.

## Procedure

1.  Open Power BI Desktop on your client machine.

2.  Navigate to the **Home** &gt; **Get Data** &gt; **More**.

    ![UI screen for navigating to more options.](../image/powerBI-1.png)

3.  In the Get Data dialog, search for and select **ODBC** from the list of available data sources.

    ![UI screen to select ODBC](../image/powerBI-2.png)

4.  Select **Connect**.

5.  In the ODBC dialog box, select your configured ServiceNow ODBC data source name \(DSN\) from the **Data source name \(DSN\)** drop down list.

    ![UI screen to select DSN](../image/powerBI-3.png)

6.  Select **Advanced options**.

7.  In the **SQL statement \(optional\)** field, enter your SQL API query.

8.  From the **Supported row reduction clauses \(optional\)** menu, select **TOP**.

    ![UI screen to enter your SQL query](../image/powerBI-4.png)

9.  Select **OK**.

    A preview of your data appears in a new window.

    ![UI screen to show the sample data](../image/powerBI-5.png)

    Only tables for which you have configured egress\_sql and read ACLs will be visible and accessible.

10. Do one of the following:

    -   To import the data directly into Power BI, select **Load**.
    -   To open the Power Query Editor and modify the data before loading, select **Transform Data**.

## Result

Power BI Desktop is now connected to your ServiceNow instance via the ODBC driver. You can create visualizations, reports, and dashboards using your ServiceNow data. The connection respects all ServiceNow security controls, including ACLs and role-based access restrictions.

**Parent Topic:**[Integrate SQL API Drivers with third-party BI tools](../reference/configure-drivers-bi-tools.md)

