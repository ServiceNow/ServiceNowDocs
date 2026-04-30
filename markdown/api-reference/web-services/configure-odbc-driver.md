---
title: Configure ServiceNow SQL API ODBC driver on client machine
description: Configure connection settings for the installed ODBC driver including server URL and authentication credentials to enable data access from BI tools to your ServiceNow instance.
locale: en-us
release: zurich
product: Web Services
classification: web-services
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure, Access your ServiceNow data using SQL API, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Configure ServiceNow SQL API ODBC driver on client machine

Configure connection settings for the installed ODBC driver including server URL and authentication credentials to enable data access from BI tools to your ServiceNow instance.

## Before you begin

-   You have a valid ServiceNow credentials for a Service Account with the required roles assigned. See [Create a Service Account and assign Roles](create-service-account.md) for more information.
-   Your client machine's IP address is included in the SQL API IP filter criteria. See [Create IP filter criteria](create-ip-filter-criteria.md) for more information.
-   You have the necessary connection parameters including your ServiceNow instance URL and Service Account credentials.

Role required: local administrator on client machine for installation

## About this task

After installing the ServiceNow SQL API ODBC driver on your client machine, you must configure the connection settings to establish a secure connection to your ServiceNow instance. After configuration, you can test the connection to verify that your client machine can successfully communicate with the ServiceNow SQL API.

## Procedure

1.  Open the Start Menu.

2.  Select and hold \(or right-click\) on the **Management Console**.

3.  Select **Run as administrator**.

4.  Navigate to **ServiceNow SQL API - ODBC Manager** &gt; **Manager \(local configuration\)** &gt; **&lt;drive&gt;:\\Program Files\\ServiceNow\\ODBC\\cfg\\oadm.in** &gt; **Services** &gt; **&gt;ServiceNow\_ODBC** &gt; **Service Settings** &gt; **IP Parameters**.Navigate to **ServiceNow SQL API - ODBC Manager** &gt; **Manager \(local configuration\)** &gt; **&lt;drive&gt;:\\Program Files\\ServiceNow\\ODBC\\cfg\\oadm.in** &gt; **Services** &gt; **&gt;ServiceNow\_ODBC** &gt; **Service Settings** &gt; **IP Parameters**.

5.  Open the `ServiceJVMClassPath` parameter.

    ![UI screen of ODBC driver ServiceJVMClassPath.](../image/sql-api-odbcdriver-ip-parameters.png)

6.  Append the value, separated by semicolons, with the location where the `bc-fips-2.0.0.jar`, `bcutil-fips-2.0.3.jar`, and `bcpkix-fips-2.0.7.jar` files are extracted.

    See [Download the SQL API drivers on client machine](download-sql-api-drivers.md) to locate the JAR files.

    For example, the JAR file location follows this pattern:

    `<Windows-machine-local-path>\<folder-name>\bc-fips-2.0.0.jar;<Windows-machine-local-path>\<folder-name>\bcpkix-fips-2.0.7.jar;<Windows-machine-local-path>\<folder-name>\bcutil-fips-2.0.3.jar`.

    If you change the location of the JAR files, you must update the path in the `ServiceJVMClassPath` parameter.

7.  Open the Start Menu.

8.  Select and hold \(or right-click\) on the **ODBC Data Source Administrator \(32-bit or 64-bit\) based on the ODBC driver you installed**.Right-click **ODBC Data Source Administrator** that matches your installed ODBC driver \(32-bit or 64-bit\).

9.  Select **Run as administrator**.

10. Select the **System DSN** tab.

11. Create a DSN or configure an existing DSN \(32-bit or 64-bit\) based on the ODBC driver you installed.

12. In the SN ServiceNow Local ODBC Driver Setup dialog, configure the following connection settings:

<table id="table_uzk_qm1_n3c"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Data Source Name

</td><td>

Any descriptive name such as Instance1Use one name per connected instance.

</td></tr><tr><td>

Description

</td><td>

This is optional.

</td></tr><tr><td>

Service Name

</td><td>

ServiceNow\_ODBCThis field must match exactly as set in **ODBC Data Source** details.

</td></tr><tr><td>

Service Data Source

</td><td>

ServiceNowThis field must match exactly as set in **ODBC Data Source** details.

</td></tr><tr><td>

Custom Properties

</td><td>

`url=https://<instance>.service-now.com`Enter your ServiceNow instance URL.

</td></tr></tbody>
</table>    ![UI screen of ODBC driver DNS settings.](../image/sql-api-odbcdriver-dns-setting.png)

13. Select **Apply**.

14. Verify the connection by selecting **Test Connection** and entering the Service Account username and password.

    If the test is successful, you will see a confirmation message indicating that the connection was established.

15. Save the data source configuration by selecting **OK**.

16. Close the ODBC Data Source Administrator by selecting **OK**.


## Result

The ServiceNow SQL API ODBC driver is configured on your client machine. You can connect your ODBC-compatible applications, such as Power BI, or Excel, to this data source to access your ServiceNow data.

## What to do next

You can use Interactive SQL application to verify the connection and test SQL queries. See [Test SQL API ODBC driver connection using Interactive SQL](test-sql-api-odbc-driver-connection-using-interactive-sql.md).

**Parent Topic:**[Configuring SQL API](../concept/configuring-sql-api.md)

