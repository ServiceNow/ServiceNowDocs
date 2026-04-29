---
title: Configure ServiceNow SQL API JDBC driver on client machine
description: Configure the JDBC driver settings on your client machine to establish a connection to your ServiceNow instance and access data through the SQL API.
locale: en-us
release: australia
product: Web Services
classification: web-services
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Access your ServiceNow data using SQL API, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Configure ServiceNow SQL API JDBC driver on client machine

Configure the JDBC driver settings on your client machine to establish a connection to your ServiceNow instance and access data through the SQL API.

## Before you begin

Verify the following prerequisites are met:

-   You have downloaded the ServiceNow SQL API JDBC driver to your client machine. See [Download the SQL API drivers on client machine](download-sql-api-drivers.md) for more information.
-   JDK 17 is installed on your client machine.
-   You have valid ServiceNow credentials for a Service Account with the required roles assigned. See [Create a Service Account and assign Roles](create-service-account.md) for more information.
-   Your client machine's IP address is included in the SQL API IP filter criteria. See [Create IP filter criteria](create-ip-filter-criteria.md) for more information.
-   You have the necessary connection parameters including your ServiceNow instance URL and Service Account credentials.

Role required: local administrator on client machine for installation

## About this task

After configuring the JDBC driver, your applications can execute SQL queries against authorized ServiceNow tables through the SQL API.

## Procedure

1.  Locate the downloaded ServiceNow JDBC driver JAR file on your client machine.

    The driver file is typically named `servicenow-jdbc-driver.jar` or similar.

2.  Add the JDBC driver to your application's classpath or configure it in your BI tool's driver management section.

    The method for adding the driver varies depending on your application. Consult your BI tool's documentation for specific instructions on adding custom JDBC drivers.

3.  Configure the JDBC connection URL using the following format:

    ```
    jdbc:servicenow://https://<instance-name>.service-now.com
    ```

    For example, `jdbc:servicenow://https://exampleinstance.service-now.com`.

4.  Enter the Service Account credentials:

    -   **Username**: Enter the User ID of the Service Account with the sn\_jdbc\_rest\_access role.
    -   **Password**: Enter the password for the Service Account.
5.  Test the connection to confirm that the JDBC driver can successfully connect to your ServiceNow instance.

    Most BI tools and database clients provide a **Test Connection** button. Use this feature to validate your configuration before proceeding.


## Result

After successfully configuring the JDBC driver, your BI tool or application can connect to ServiceNow and execute SQL queries against authorized tables. You can now query ServiceNow data directly without requiring data export or replication.

**Parent Topic:**[Configuring SQL API](../concept/configuring-sql-api.md)

