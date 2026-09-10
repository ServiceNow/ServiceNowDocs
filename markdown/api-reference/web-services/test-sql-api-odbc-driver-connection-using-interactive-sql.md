---
title: Test Live Connect ODBC driver connection
description: Use Interactive SQL to verify that the ODBC driver connects to your ServiceNow instance and returns query results.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/web-services/test-sql-api-odbc-driver-connection-using-interactive-sql.html
release: australia
product: Web Services
classification: web-services
topic_type: task
last_updated: "2026-03-07"
reading_time_minutes: 1
keywords: [ODBC driver, Interactive SQL, iSQL, test connection, Live Connect]
breadcrumb: [Configure, Access your ServiceNow data using Live Connect, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Test Live Connect ODBC driver connection

Use Interactive SQL to verify that the ODBC driver connects to your ServiceNow instance and returns query results.

## Before you begin

The ODBC driver is configured on your client machine. See [Configure ServiceNow Live Connect ODBC driver on a client machine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/configure-odbc-driver.md).

Role required: administrator

## Procedure

1.  From the Start menu, select and hold \(or right-click\) Interactive SQL \(ODBC\), then select **Run as administrator**.

2.  To connect to your ServiceNow instance, enter the following command:

    -   Basic authentication:

        ```
        connect "username"*"password"@"dsn_name"
        ```

        Example:

        ```
        connect "odbc.user"*"TestSQLAPI"@"servicenow"
        ```

    -   OAuth authentication: OAuth credentials are handled automatically through your DSN configuration. Use `connect @"dsn_name"`.
    Replace `username`, `password`, and `dsn_name` with your respective credentials. DSN is configured in [Configure ServiceNow Live Connect ODBC driver on a client machine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/configure-odbc-driver.md).

    A confirmation message appears if the connection is successful.

3.  To verify the connection returns data, enter a SELECT query.

    Example:

    ```
    SELECT NUMBER, short_description FROM incident;
    ```

    Include the semicolon at the end of the query. Without it, a `Cont>` prompt appears.

    \[Omitted image "SampleSQLQuery.png"\] Alt text: Sample SQL Query.

    The query results appear, displaying incident numbers and descriptions from your instance.


## Result

The ODBC driver connection is verified. You can use the driver with BI tools and data analysis platforms to query your ServiceNow data.

**Parent Topic:**[Configuring Live Connect](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/configuring-sql-api.md)

