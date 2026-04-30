---
title: Use Interactive SQL with ODBC
description: Run the Interactive SQL application for quick verification of connectivity and to test query results without using a full application.
locale: en-US
release: zurich
product: Web Services
classification: web-services
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [ODBC and client applications, Create data sources from other apps using ODBC driver, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Use Interactive SQL with ODBC

Run the Interactive SQL application for quick verification of connectivity and to test query results without using a full application.

## Before you begin

Role required: admin

## Procedure

1.  In Windows, navigate to **Start** &gt; **Programs** &gt; **ServiceNow ODBC** &gt; **Interactive SQL \(ODBC\)**.

2.  Connect to the base instance by entering the following command and selecting the appropriate user credentials in the format without special characters: `ID*password@DSNName`.

    ```
    CONNECT odbcuser*password@ServiceNow
    ```

    ![Connecting the SQL.](../image/ConnectingTheSQL.png)

3.  Issue a `SELECT` SQL command.

    ```
    SELECT NUMBER, short_description FROM incident;
    ```

    Make sure to include the semicolon at the end of your query statement. Otherwise, you are presented with a `'Cont>'` prompt.

    ![Sample SQL Query.](../image/SampleSQLQuery.png)


-   **[Specify the maximum number of rows returned](../reference/r_MaxRowsReturned.md)**  
By default, ServiceNow only returns 100 rows of data with each iSQL query. If you need to return more rows of data, set the maxrows parameter for the iSQL session.
-   **[SQL support](../reference/r_SQLSupport.md)**  
The ODBC driver embeds a third party SQL/ODBC engine from DataDirect, a division of Progress Software.

**Parent Topic:**[ODBC and client applications](../reference/r_ODBCAndClientApplications.md)

