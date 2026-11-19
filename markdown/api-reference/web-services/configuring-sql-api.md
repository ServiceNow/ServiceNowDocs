---
title: Configuring Live Connect
description: Configure your ServiceNow instance to enable Live Connect access, set up security controls, and install the required drivers on your client machine.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/api-reference/web-services/configuring-sql-api.html
release: australia
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 3
keywords: [configure]
breadcrumb: [Access your ServiceNow data using Live Connect, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Configuring Live Connect

Configure your ServiceNow instance to enable Live Connect access, set up security controls, and install the required drivers on your client machine.

## Configuration overview

Before you begin, confirm the following:

-   The Live Connect plugin is installed on your instance.
-   You have consulted your network team to identify the IP address range for your ODBC/JDBC client machines.
-   You have identified which ServiceNow tables must be accessible via Live Connect.

The configuration process involves two main components:

1.  Instance setup:
    -   [Install Live Connect on your ServiceNow instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/web-services/install-sql-api-plugin.md)
    -   [Assign roles and create service accounts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/web-services/create-service-account.md)
    -   [Create Access Control Lists \(ACLs\) for Live Connect](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/web-services/create-acls-sql-api.md)
    -   [Create IP filter criteria](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/web-services/create-ip-filter-criteria.md)
2.  Driver installation and configuration:
    -   [Download the Live Connect drivers on a client machine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/web-services/download-sql-api-drivers.md)
    -   [Install the ServiceNow Live Connect ODBC driver on a client machine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/web-services/install-odbc-driver.md)
    -   [Configure ServiceNow Live Connect ODBC driver on a client machine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/web-services/configure-odbc-driver.md)
    -   [Configure ServiceNow Live Connect JDBC driver on a client machine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/web-services/configure-jdbc-driver.md)

## After configuration

After completing all procedures, your user account can connect to your ServiceNow instance via ODBC or JDBC. You can then query tables for which access has been granted.

-   Use service accounts for production reports and dashboards. Service accounts promote continuity — personal accounts break if the user loses access or leaves the organization.
-   Access is not granted globally. A user account can query a table only if it has explicit read access through table-level ACLs \(`egress_sql` and `read`\) or a role with read permissions.
-   Non-interactive \(machine\) service accounts can't complete MFA challenges. Turn off MFA for those accounts. Personal accounts using OAuth aren't subject to this limitation.

-   **[Install Live Connect on your ServiceNow instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/web-services/install-sql-api-plugin.md)**  
Install Live Connect to enable secure, read-only access to your instance data from external applications.
-   **[Live Connect configuration on your ServiceNow instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/web-services/configure-sql-api-overview.md)**  
Complete the three-step configuration that's required to enable Live Connect access.
-   **[Enable OAuth for Live Connect](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/web-services/enable-oauth-for-live-connect.md)**  
Configure OAuth as an additional authentication method for Live Connect connections. This adds OAuth alongside basic authentication without replacing it.
-   **[Download the Live Connect drivers on a client machine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/web-services/download-sql-api-drivers.md)**  
Download ODBC and JDBC drivers to enable third-party Business Intelligence tools and data analysis platforms to connect to your ServiceNow instance data.
-   **[Install the ServiceNow Live Connect ODBC driver on a client machine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/web-services/install-odbc-driver.md)**  
Use the installation wizard to install the ODBC driver and configure the connection between your Business Intelligence tools and ServiceNow data.
-   **[Configure ServiceNow Live Connect ODBC driver on a client machine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/web-services/configure-odbc-driver.md)**  
Configure the ODBC driver with your instance URL, BCFIPS JAR file paths, and authentication credentials to enable BI tools to access your ServiceNow data.
-   **[Test Live Connect ODBC driver connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/web-services/test-sql-api-odbc-driver-connection-using-interactive-sql.md)**  
Use Interactive SQL to verify that the ODBC driver connects to your ServiceNow instance and returns query results.
-   **[Configure ServiceNow Live Connect JDBC driver on a client machine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/web-services/configure-jdbc-driver.md)**  
Configure the JDBC driver to connect to your ServiceNow instance and query your data.
-   **[Route Live Connect calls to Read Replica](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/web-services/routing-sql-api-calls-to-read-replica.md)**  
Route Live Connect calls to a Read Replica database to reduce the processing load on the primary database in your ServiceNow instance.

**Parent Topic:**[Access your ServiceNow data using Live Connect](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/web-services/accessing-your-servicenow-data-using-sql-api.md)

