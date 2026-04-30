---
title: Test a query
description: To verify that the user has the appropriate permissions to send requests to the instance using ODBC, run a query using Interactive SQL.
locale: en-US
release: zurich
product: Web Services
classification: web-services
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Test the ODBC driver, Create data sources from other apps using ODBC driver, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Test a query

To verify that the user has the appropriate permissions to send requests to the instance using ODBC, run a query using Interactive SQL.

## About this task

For testing, use a query that returns exactly one record, such as a query using the **Number** value of a record.

## Procedure

1.  In the base system instance, navigate to **Incident** &gt; **All**.

2.  Record the **Number** of an incident record.

3.  On the computer where the ODBC driver is installed, navigate to **Start** &gt; **Programs** &gt; **ServiceNow ODBC** &gt; **Interactive SQL**.

4.  Enter `connect "odbc.user"*"password"@ServiceNow` and press **Enter**.

5.  Enter the following text, substituting the incident number you recorded.

    `select short_description from incident where number=’<incident number>';`

6.  Press **Enter**.


## Result

The instance should respond with the short description of the incident record.

**Parent Topic:**[Test the ODBC driver](t_TestingTheODBCDriver.md)

