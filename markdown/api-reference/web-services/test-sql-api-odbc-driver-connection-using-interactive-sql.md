---
title: Test SQL API ODBC driver connection using Interactive SQL
description: Run the Interactive SQL application for quick verification of connectivity and to test query results without using a full application.
locale: en-US
release: australia
product: Web Services
classification: web-services
topic_type: task
last_updated: "2026-03-07"
reading_time_minutes: 1
breadcrumb: [Configure, Access your ServiceNow data using SQL API, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Test SQL API ODBC driver connection using Interactive SQL

Run the Interactive SQL application for quick verification of connectivity and to test query results without using a full application.

## Before you begin

Role required: local administrator on client machine

## Procedure

1.  Navigate to the **Start Menu**.

2.  Select and hold \(or right-click\) on the **Interactive SQL \(ODBC\)**.

3.  Select **Run as Administrator**.

4.  Use this command format to connect to your ServiceNow instance database using the ODBC driver:

    ```
    connect “username”*”password”@”dsn_name”
    ```

    For example:

    ```
    connect "odbc.user"*"TestSQLAPI"@”servicenow”
    ```

5.  Issue a SELECT SQL command.

    ```
    SELECT NUMBER, short_description FROM incident;
    ```

    Include the semicolon at the end of your query statement. Otherwise, the system displays a `'Cont>'` prompt.

    ![Sample SQL Query.](../../odbc-driver/image/SampleSQLQuery.png)


**Parent Topic:**[Configuring SQL API](../concept/configuring-sql-api.md)

