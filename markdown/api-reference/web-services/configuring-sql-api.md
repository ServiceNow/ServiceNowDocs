---
title: Configuring Live Connect
description: This section guides you through the complete setup process for the ServiceNow Live Connect, covering both instance configuration and driver installation. You will configure your ServiceNow instance to enable Live Connect access, set up the necessary security controls, and install the appropriate drivers on your client machine.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/web-services/configuring-sql-api.html
release: australia
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [configure]
breadcrumb: [Access your ServiceNow data using Live Connect, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Configuring Live Connect

This section guides you through the complete setup process for the ServiceNow Live Connect, covering both instance configuration and driver installation. You will configure your ServiceNow instance to enable Live Connect access, set up the necessary security controls, and install the appropriate drivers on your client machine.

## Live Connect configuration overview

The configuration process involves two main components:

1.  Instance setup:

    Configure your ServiceNow instance by installing the Live Connect plugin. Assign the appropriate access roles to users \(service accounts or regular users\). Define Access Control Lists \(ACLs\) to control data access and establish IP filtering policies for security.

    -   [Install Live Connect on your ServiceNow instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/install-sql-api-plugin.md)
    -   [Live Connect configuration on your ServiceNow instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/configure-sql-api-overview.md)
2.  Driver installation and configuration:

    Download the Live Connect drivers from the ServiceNow Store. Install either the ODBC driver on your Windows client machine or configure the JDBC driver in your preferred database client.

    -   [Download the Live Connect drivers on a client machine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/download-sql-api-drivers.md)
    -   [Install the ServiceNow Live Connect ODBC driver on a client machine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/install-odbc-driver.md)
    -   [Configure ServiceNow Live Connect ODBC driver on a client machine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/configure-odbc-driver.md)
    -   [Configure ServiceNow Live Connect JDBC driver on a client machine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/configure-jdbc-driver.md)

-   **[Install Live Connect on your ServiceNow instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/install-sql-api-plugin.md)**  
Install Live Connect to enable secure, read-only access to your instance data from external applications.
-   **[Live Connect configuration on your ServiceNow instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/configure-sql-api-overview.md)**  
Complete the three-step configuration that's required to enable Live Connect access.
-   **[Enable OAuth for Live Connect](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/enable-oauth-for-live-connect.md)**  
Configure OAuth as an additional authentication method for Live Connect connections. This adds OAuth alongside basic authentication without replacing it.
-   **[Download the Live Connect drivers on a client machine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/download-sql-api-drivers.md)**  
Download ODBC and JDBC drivers to enable third-party Business Intelligence tools and data analysis platforms to connect to your ServiceNow data.
-   **[Install the ServiceNow Live Connect ODBC driver on a client machine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/install-odbc-driver.md)**  
Use the installation wizard to install the ODBC driver and configure the connection between your Business Intelligence tools and ServiceNow data.
-   **[Configure ServiceNow Live Connect ODBC driver on a client machine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/configure-odbc-driver.md)**  
Configure the ODBC driver with your instance URL, BCFIPS JAR file paths, and authentication credentials to enable BI tools to access your ServiceNow data.
-   **[Test Live Connect ODBC driver connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/test-sql-api-odbc-driver-connection-using-interactive-sql.md)**  
Use Interactive SQL to verify that the ODBC driver connects to your ServiceNow instance and returns query results.
-   **[Configure ServiceNow Live Connect JDBC driver on a client machine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/configure-jdbc-driver.md)**  
Configure the JDBC driver to connect to your ServiceNow instance and query your data.
-   **[Route Live Connect calls to Read Replica](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/routing-sql-api-calls-to-read-replica.md)**  
You can route Live Connect calls to Read Replica to optimize the performance of your ServiceNow instance.

**Parent Topic:**[Access your ServiceNow data using Live Connect](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/accessing-your-servicenow-data-using-sql-api.md)

