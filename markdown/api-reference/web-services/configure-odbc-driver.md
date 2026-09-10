---
title: Configure ServiceNow Live Connect ODBC driver on a client machine
description: Configure the ODBC driver with your instance URL, BCFIPS JAR file paths, and authentication credentials to enable BI tools to access your ServiceNow data.
locale: en-us
canonical_url: https://www.servicenow.com/docs/r/api-reference/web-services/configure-odbc-driver.html
release: australia
product: Web Services
classification: web-services
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure, Access your ServiceNow data using Live Connect, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Configure ServiceNow Live Connect ODBC driver on a client machine

Configure the ODBC driver with your instance URL, BCFIPS JAR file paths, and authentication credentials to enable BI tools to access your ServiceNow data.

## Before you begin

Confirm that you have the following:

-   A valid ServiceNow user account \(personal or service account\) with the required roles. See [Assign roles and create service accounts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/create-service-account.md).
-   The client machine IP address is included in the Live Connect IP filter criteria. See [Create IP filter criteria](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/create-ip-filter-criteria.md).
-   Your ServiceNow instance URL and user account credentials \(personal or service account\).

Role required: administrator

## Procedure

1.  From the Start menu, select and hold \(or right-click\) **ServiceNow Live Connect - ODBC Manager** &gt; **Management Console**, select **Run as administrator**, then navigate to **Services** &gt; **ServiceNow\_ODBC** &gt; **Service Settings** &gt; **IP Parameters**.

2.  Edit the **ServiceJVMClassPath** parameter.

    \[Omitted image "sql-api-odbcdriver-ip-parameters.png"\] Alt text: Management Console showing ServiceJVMClassPath parameter in IP Parameters section

3.  Append the paths to the BCFIPS JAR files.

    Separate each path with a semicolon. The JAR files are in the dependencies folder from the driver download \(see [Download the Live Connect drivers on a client machine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/download-sql-api-drivers.md)\).

    Example paths:

    `<Windows-machine-local-path>\<folder-name>\bc-fips-2.0.0.jar;<Windows-machine-local-path>\<folder-name>\bcpkix-fips-2.0.7.jar;<Windows-machine-local-path>\<folder-name>\bcutil-fips-2.0.3.jar`

    If you move the JAR files to a different location in the future, update the paths in the **ServiceJVMClassPath** parameter.

4.  Do this only if you want to authenticate using OAuth.

    1.  Open the **DataSourceIPCustomProperties** parameter.

    2.  Update the value to set OAuth to True and provide OAuth client ID, client secret, token URL, access token, refresh token.

        OAuth properties are described in [OAuth connection properties for ODBC and JDBC drivers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/oauth-connection-properties-for-odbc-and-jdbc-drivers.md)

        For example, you can enter the value in this pattern: `url=https://<instance>.service-now.com;UseOAuth=True;`

    **Warning:** If the OAuth client secret contains a semicolon, the ODBC driver can't parse the connection string correctly because semicolons are used as delimiters between key-value pairs. If your auto-generated client secret contains a semicolon, regenerate the client secret until you receive one without a semicolon, then use that secret in your ODBC configuration.

5.  From the Start menu, select and hold \(or right-click\) **ODBC Data Source Administrator** \(32-bit or 64-bit, matching your installed driver\), then select **Run as administrator**.

6.  In the **System DSN** tab, create a DSN or configure an existing DSN.

7.  Enter the following connection settings:

<table id="table_uzk_qm1_n3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Data Source Name**

</td><td>

Unique identifier for this connection \(for example, Instance1\).

</td></tr><tr><td>

**Description**

</td><td>

Optional description of the data source.

</td></tr><tr><td>

**Service Name**

</td><td>

Name configured during installation \(for example, ServiceNow\_ODBC\).

</td></tr><tr><td>

**Service Data Source**

</td><td>

Service name configured during installation.

</td></tr><tr><td>

**Custom Properties**

</td><td>

`url=https://<instance>.service-now.com`, where &lt;instance&gt; is your instance name.Enter connection properties as semicolon-separated key-value pairs. At minimum, include your instance URL: url=https://

&lt;instance&gt;.service-now.com. To connect using OAuth instead of a username and password add the OAuth properties described in [OAuth connection properties for ODBC and JDBC drivers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/oauth-connection-properties-for-odbc-and-jdbc-drivers.md).

</td></tr></tbody>
</table>8.  Select **Apply**.

9.  To verify the connection, select **Test Connection** and enter your user account credentials based on your authentication method:

    -   Basic authentication: Enter the username and password.
    -   OAuth: OAuth credentials are used automatically from your earlier configuration.
    A confirmation message appears if the connection is successful.

10. Select **OK** to save the configuration.


## Result

The ServiceNow Live Connect ODBC driver is configured. You can connect ODBC-compatible applications such as Power BI or Excel to this data source to access your ServiceNow data.

**Parent Topic:**[Configuring Live Connect](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/configuring-sql-api.md)

