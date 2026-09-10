---
title: Connect Power BI Desktop to ODBC driver
description: Connect Power BI Desktop to your ServiceNow instance using the ODBC driver to access and analyze ServiceNow data. Create dashboards and reports that visualize your ServiceNow data.
locale: en-us
canonical_url: https://www.servicenow.com/docs/r/api-reference/web-services/connect-power-bi-odbc.html
release: australia
product: Web Services
classification: web-services
topic_type: task
last_updated: "2026-03-04"
reading_time_minutes: 2
breadcrumb: [Integrate, Access your ServiceNow data using Live Connect, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Connect Power BI Desktop to ODBC driver

Connect Power BI Desktop to your ServiceNow instance using the ODBC driver to access and analyze ServiceNow data. Create dashboards and reports that visualize your ServiceNow data.

## Before you begin

-   The Live Connect plugin is installed on your ServiceNow instance.
-   The ServiceNow ODBC driver is installed and configured on your client machine.
-   You have a personal user account or service account with the **sn\_odbc\_rest\_access** role assigned.
-   Access Control Lists \(ACLs\) are configured for the tables you must query.
-   IP filter criteria are configured to allow connections from your client machine.

Role required: admin

## About this task

**Note:**

Step-by-step instructions for third-party tools are illustrative. Consult tool-specific documentation for the latest updates. Power BI Desktop is solely used as an example.

This connection enables you to query ServiceNow data directly without requiring data export or replication. You can combine ServiceNow data with other data sources in your analysis.

## Procedure

1.  Open Power BI Desktop on your client machine.

2.  Navigate to **Home** &gt; **Get Data** &gt; **More**.

    \[Omitted image "powerBI-1.png"\] Alt text: UI screen for navigating to more options.

3.  In the Get Data dialog, search for `ODBC`.

    \[Omitted image "powerBI-2.png"\] Alt text: UI screen to select ODBC

4.  Select **ODBC**and then select **Connect**.

5.  In the From ODBC dialog box, select your configured ServiceNow ODBC data source name \(DSN\) from the **Data source name \(DSN\)** list.

    \[Omitted image "powerBI-3.png"\] Alt text: UI screen to select DSN

6.  Select **Advanced options**.

7.  In the **SQL statement \(optional\)** field, enter your Live Connect query.

8.  From the **Supported row reduction clauses \(optional\)** menu, select **TOP**.

    This limits the number of rows returned in your query, which reduces data transfer and improve performance.

    \[Omitted image "powerBI-4.png"\] Alt text: UI screen to enter your SQL query

9.  Select **OK**.

    Skip the **username**, **password**, and **credentials connection string properties** fields. Your authentication method \(Basic or OAuth\) is already configured in your ODBC DSN and will be used automatically. The connection uses the user account you specified during DSN setup.

    A preview of your data appears in a new window. Only tables for which you have configured egress\_sql and read ACLs will be visible and accessible.

    \[Omitted image "powerBI-5.png"\] Alt text: UI screen to show the sample data

10. Do one of the following:

    -   To import the data directly into Power BI, select **Load**.
    -   To open the Power Query Editor and modify the data before loading, select **Transform Data**.

## Result

Power BI Desktop is now connected to your ServiceNow instance via the ODBC driver. You can create visualizations, reports, and dashboards using your ServiceNow data. The connection respects all ServiceNow security controls, including ACLs and role-based access restrictions.

**Parent Topic:**[Integrate Live Connect Drivers with third-party BI tools](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/configure-drivers-bi-tools.md)

