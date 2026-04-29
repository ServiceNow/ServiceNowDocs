---
title: Test the ODBC driver
description: After configuring the ODBC driver, test that the driver can connect to the base instance as the ODBC user and can query data from a target table.
locale: en-US
release: australia
product: Web Services
classification: web-services
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create data sources from other apps using ODBC driver, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Test the ODBC driver

After configuring the ODBC driver, test that the driver can connect to the base instance as the ODBC user and can query data from a target table.

## Before you begin

You must have administrator-level access for the Windows computer on which you want to test the ODBC driver.

## About this task

To test the connection, run the ODBC Administrator program.

## Procedure

1.  In Windows, navigate to **Start** &gt; **Programs** &gt; **ServiceNow ODBC** &gt; **ODBC Administrator**.

    The ServiceNow ODBC data source is installed as a system data source.

2.  Select the **System DSN** tab, and then select the **ServiceNow** data source.

3.  Click **Configure**.

    ![ServiceNow system data source](../image/ServiceNowDataSource.png)

4.  Click **Test Connect** in the ODBC driver Setup dialog box.

    ![Test data source connection](../image/TestConnect.png)

5.  Enter the login credentials.

    These are the usual ServiceNow base system login credentials for the ODBC user you created.

    ![Log on to data source](../image/DataSourceLogOn.png)

6.  Click **OK** to log in to the data source.

7.  Click **OK** again when the success message appears.


-   **[Generate logs for debugging](t_GenerateDebugLogs.md)**  
If you experience unexpected behavior when using the ODBC driver, you can enable debug logging and generate debug logs to help identify the issue.
-   **[Test a query](t_TestingAQuery.md)**  
To verify that the user has the appropriate permissions to send requests to the instance using ODBC, run a query using Interactive SQL.
-   **[ODBC troubleshooting](../reference/odbc-troubleshooting.md)**  
Review these troubleshooting resources to resolve issues with the ODBC driver.

**Parent Topic:**[Create data sources from other apps using ODBC driver](../concept/c_ODBCDriver.md)

**Related topics**  


[Configure the ODBC driver](t_ConfigureTheODBCDriver.md)

