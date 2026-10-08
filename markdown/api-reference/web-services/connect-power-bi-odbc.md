---
title: Connect Power BI Desktop to ODBC driver
description: Connect Power BI Desktop to your ServiceNow instance using the ODBC driver to access and analyze ServiceNow data. Create dashboards and reports that visualize your ServiceNow data.
locale: en-us
canonical_url: https://www.servicenow.com/docs/r/zurich/api-reference/web-services/connect-power-bi-odbc.html
release: zurich
product: Web Services
classification: web-services
topic_type: task
last_updated: "2026-03-04"
reading_time_minutes: 5
breadcrumb: [Integrate, Access your ServiceNow data using Live Connect, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Connect Power BI Desktop to ODBC driver

Connect Power BI Desktop to your ServiceNow instance using the ODBC driver to access and analyze ServiceNow data. Create dashboards and reports that visualize your ServiceNow data.

## Before you begin

-   The Live Connect plugin is installed on your ServiceNow instance. See [Install Live Connect on your ServiceNow instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/web-services/install-sql-api-plugin.md).
-   The ServiceNow ODBC driver is installed and configured on your client machine. See [Configure ServiceNow Live Connect ODBC driver on a client machine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/web-services/configure-odbc-driver.md).
-   A personal user account or service account with the **sn\_odbc\_rest\_access** role is assigned. See [Assign roles and create service accounts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/web-services/create-service-account.md).
-   For personal user accounts using basic authentication, the **snc\_basic\_auth\_api\_access** role must also be assigned.
-   The `egress_sql` and read Access Control Lists \(ACLs\) are configured for the tables you must query. See [Create Access Control Lists \(ACLs\) for Live Connect](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/web-services/create-acls-sql-api.md).
-   IP filter criteria are configured to permit connections from your client machine. See [Create IP filter criteria](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/web-services/create-ip-filter-criteria.md).
-   Administrator privileges on the client machine are required to run Power BI Desktop as administrator.

Role required: sn\_odbc\_rest\_access

## About this task

**Note:** Instructions for third-party tools are illustrative. Consult tool-specific documentation for the latest updates. Power BI Desktop is only used as an example.

This connection enables you to query ServiceNow data directly without requiring data export or replication to a data lake or a data warehouse. You can combine ServiceNow data with other data sources in your analysis.

**Warning:** Large tables such as incident or cmdb\_ci may cause timeout errors or performance issues when using the graphical interface to select tables. For large tables, use the SQL statement approach with the TOP clause to limit the number of rows returned. Small tables such as core\_company and cmn\_location typically work without issues using either approach.

## Procedure

1.  Open Power BI Desktop as administrator by selecting and holding \(or right-clicking\) the application and selecting **Run as administrator**.

    Running as administrator is required to prevent connection errors with the ODBC driver.

2.  Navigate to **Home** &gt; **Get Data** &gt; **More**.

    \[Omitted image "powerBI-1.png"\] Alt text: Power BI Desktop Home tab with Get Data and More options highlighted.

3.  In the Get Data dialog, search for `ODBC`.

    \[Omitted image "powerBI-2.png"\] Alt text: Get Data dialog with ODBC selected in the search results.

4.  Select **ODBC** and then select **Connect**.

5.  From the **Data source name \(DSN\)** list, select your configured ServiceNow ODBC DSN.

    \[Omitted image "powerBI-3.png"\] Alt text: From Data Source Name list with a configured ODBC DSN selected.

6.  Do one of the following based on your table size:

<table><thead><tr><th>

Table size

</th><th>

Action

</th></tr></thead><tbody><tr><td>

Small tablesFor example, core\_company or cmn\_location

</td><td>

Select **OK** to use the graphical interface for table selection.

</td></tr><tr><td>

Large tablesFor example, incident or cmdb\_ci

</td><td>

Select **Advanced options** to write a SQL statement. You can use this option to also write custom queries.

</td></tr></tbody>
</table>7.  If you selected **Advanced options**, in the **SQL statement \(optional\)** field, enter your Live Connect query.

    For large tables, include a WHERE clause to filter data or use the TOP clause to limit rows.

8.  From the **Supported row reduction clauses \(optional\)** menu, select **TOP**.

    This limits the number of rows returned in your query, which reduces data transfer and improves performance. Use this option for large tables to prevent timeout errors. If you need to filter the data, rather than just limit its size, before building your dashboard or report, use a WHERE clause instead of or with TOP. Filtering large tables in the graphical Navigator preview can still retrieve the entire table and time out.

    \[Omitted image "powerBI-4.png"\] Alt text: Advanced options panel showing the SQL statement field and Supported row reduction clauses menu.

9.  Select **OK**.

    Skip the **username**, **password**, and **credentials connection string properties** fields. Your authentication method \(Basic or OAuth\) is already configured in your ODBC DSN and will be used automatically. The connection uses the user account you specified during DSN setup.

    If you used the SQL statement approach, a preview of your query results appears. If you selected tables directly, the Navigator window displays available tables and a preview pane.

    Only tables for which you have configured `egress_sql` and read ACLs will be visible and accessible.

    The preview is limited to the first 1,000 rows. The complete dataset loads when you select **Load** or **Transform Data**.

    \[Omitted image "powerBI-5.png"\] Alt text: Query results preview showing sample rows returned from the ODBC connection.

    If you encounter timeout errors or the preview fails to load, the table may be too large. Close the dialog and reconnect using the SQL statement approach with a TOP clause or WHERE clause to reduce the dataset size.

10. If you used the direct table selection method, select the tables you want to import from the Navigator window, then do one of the following:

    -   To import the data directly into Power BI, select **Load**.
    -   To open the Power Query Editor and transform or filter the data before loading, select **Transform Data**.
    In Power Query Editor, you can remove unnecessary columns, apply filters, change data types, and perform other transformations. Reducing the dataset size in Power Query Editor improves performance and reduces load times, and is recommended by Microsoft.


## Result

Power BI Desktop is connected to your ServiceNow instance via the ODBC driver. You can create visualizations, reports, and dashboards using your ServiceNow data. The connection respects all ServiceNow security controls, including ACLs and role-based access restrictions.

To create relationships between tables, use the Model view in Power BI Desktop. Joins created in the Model view are processed locally in Power BI. For better performance with large datasets, create joins in your SQL statement instead.

## What to do next

To publish your report to the Power BI Service for sharing with other users or to set up scheduled data refresh, select **Home** &gt; **Publish** in Power BI Desktop. Configure the Power BI Gateway to enable automatic data refresh from your ServiceNow instance. For gateway installation requirements, see [Install an on-premises data gateway](https://learn.microsoft.com/en-us/data-integration/gateway/service-gateway-install#requirements).

**Parent Topic:**[Integrate Live Connect Drivers with third-party BI tools](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/web-services/configure-drivers-bi-tools.md)

**Related topics**  


[Power BI Desktop data import mode and limits](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/web-services/power-bi-import-mode-and-limits.md)

