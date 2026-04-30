---
title: Generate logs for debugging
description: If you experience unexpected behavior when using the ODBC driver, you can enable debug logging and generate debug logs to help identify the issue.
locale: en-US
release: zurich
product: Web Services
classification: web-services
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Test the ODBC driver, Create data sources from other apps using ODBC driver, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Generate logs for debugging

If you experience unexpected behavior when using the ODBC driver, you can enable debug logging and generate debug logs to help identify the issue.

## Before you begin

[Configure the logging level of the ODBC driver](t_CnfgLoggingLevel.md)

Role required: admin

## About this task

Debug logs can be useful when submitting an incident with Customer Service and Support.

When you enable debug logging, note the version and bitness \(32 bit or 64 bit\) of the installed ODBC driver, the Windows operating system, and the client application you are using with the ODBC driver.

To generate debug logs, follow these steps.

## Procedure

1.  Close all active applications that may use the ODBC driver.

2.  Navigate to one of these paths, based on your operating system.

    -   For Windows 10 and later: `C:\ProgramData\ServiceNow\odbc\logging\`
    -   For Windows 7: `C:\Users\<user_name>\AppData\Local\ServiceNow\odbc\logging`
    -   For Windows XP and earlier: `C:\Program Files\ServiceNow\ODBC\%LOCALAPPDATA%\ServiceNow\odbc\logging`
3.  Delete any existing log data to ensure that you log only relevant information.

4.  Run a query that produces the unexpected behavior, then immediately close the application and review the log files.


**Parent Topic:**[Test the ODBC driver](t_TestingTheODBCDriver.md)

**Related topics**  


[Configure the logging level of the ODBC driver](t_CnfgLoggingLevel.md)

