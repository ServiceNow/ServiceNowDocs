---
title: Configure ServiceNow Live Connect JDBC driver on a client machine
description: Configure the JDBC driver to connect to your ServiceNow instance and query your data.
locale: en-us
canonical_url: https://www.servicenow.com/docs/r/api-reference/web-services/configure-jdbc-driver.html
release: australia
product: Web Services
classification: web-services
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Access your ServiceNow data using Live Connect, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Configure ServiceNow Live Connect JDBC driver on a client machine

Configure the JDBC driver to connect to your ServiceNow instance and query your data.

## Before you begin

Verify the following:

-   The ServiceNow Live Connect JDBC driver is downloaded. See [Download the Live Connect drivers on a client machine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/download-sql-api-drivers.md).
-   JDK 17 is installed.
-   A valid ServiceNow user account \(personal or service account\) with the required roles. See [Assign roles and create service accounts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/create-service-account.md).
-   The client machine IP address is included in the Live Connect IP filter criteria. See [Create IP filter criteria](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/create-ip-filter-criteria.md).
-   Your ServiceNow instance URL and user account credentials \(personal or service account\).
-   Your OAuth Application Registry configured if you plan to connect using OAuth instead of basic authentication. See [Enable OAuth for Live Connect](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/enable-oauth-for-live-connect.md).

Role required: administrator

## Procedure

1.  Locate the ServiceNow JDBC driver JAR file on your client machine.

    The file is typically named `servicenow-jdbc-driver.jar`.

2.  Add the JDBC driver to your application's classpath or configure it in your BI tool's driver management section.

    The method varies by application. Consult your BI tool documentation for instructions.

3.  Configure the JDBC connection URL:

    ```
    jdbc:servicenow://https://<instance-name>.service-now.com
    ```

    Example:

    ```
    jdbc:servicenow://https://exampleinstance.service-now.com
    ```

4.  Select an authentication method and configure the driver properties.

<table id="choicetable_cry_fmy_hkc"><tbody><tr><td id="d650764e203">

**Method**

</td><td>

Properties

</td></tr><tr><td id="d650764e212">

**Basic Authentication**

</td><td>

Set **user** to the user ID with the **sn\_jdbc\_rest\_access** role and **password** to the user password.

</td></tr><tr><td id="d650764e230">

**OAuth**

</td><td>

Set **useoauth** to `true` and provide the OAuth properties described in [OAuth connection properties for ODBC and JDBC drivers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/oauth-connection-properties-for-odbc-and-jdbc-drivers.md).

</td></tr></tbody>
</table>5.  To verify the connection, test that the JDBC driver connects to your ServiceNow instance.

    Most BI tools and database clients provide a **Test Connection** button.

    A confirmation message appears if the connection is successful.


## Result

The JDBC driver is configured. Your BI tool or application can connect to ServiceNow and execute SQL queries against authorized tables.

**Parent Topic:**[Configuring Live Connect](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/configuring-sql-api.md)

