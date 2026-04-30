---
title: Configuring SQL API
description: This section guides you through the complete setup process for the ServiceNow SQL API, covering both instance configuration and driver installation. You will configure your ServiceNow instance to enable SQL API access, set up the necessary security controls, and install the appropriate drivers on your client machine.
locale: en-US
release: zurich
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [configure]
breadcrumb: [Access your ServiceNow data using SQL API, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Configuring SQL API

This section guides you through the complete setup process for the ServiceNow SQL API, covering both instance configuration and driver installation. You will configure your ServiceNow instance to enable SQL API access, set up the necessary security controls, and install the appropriate drivers on your client machine.

## SQL API configuration overview

The configuration process involves two main components:

1.  Instance Setup:

    Configure your ServiceNow instance by installing the SQL API plugin, creating a dedicated service account with the appropriate access roles, defining Access Control Lists \(ACLs\) to control data access, and establishing IP filtering policies for security.

    -   [Install SQL API plugin on your ServiceNow instance](install-sql-api-plugin.md)
    -   [Configure SQL API plugin on your ServiceNow instance](../task/configure-sql-api-overview.md)
2.  Driver Installation and Configuration:

    Download the SQL API drivers from the ServiceNow Store and install either the ODBC driver on your Windows client machine or configure the JDBC driver in your preferred database client.

    -   [Download the SQL API drivers on client machine](../task/download-sql-api-drivers.md)
    -   [Install ServiceNow SQL API ODBC driver on client machine](../task/install-odbc-driver.md)
    -   [Configure ServiceNow SQL API ODBC driver on client machine](../task/configure-odbc-driver.md)
    -   [Configure ServiceNow SQL API JDBC driver on client machine](../task/configure-jdbc-driver.md)

-   **[Install SQL API plugin on your ServiceNow instance](install-sql-api-plugin.md)**  
Installing the SQL API on your instance enables secure, read-only access to your instance data from external applications. You can integrate your data with external tools and analytics platforms to enhance your reporting and data analysis capabilities.
-   **[Configure SQL API plugin on your ServiceNow instance](../task/configure-sql-api-overview.md)**  
Overview of the three-step configuration process required to enable SQL API access including prerequisites and expected outcomes.
-   **[Download the SQL API drivers on client machine](../task/download-sql-api-drivers.md)**  
Download the ODBC and JDBC drivers from the ServiceNow store to your client machine to enable SQL API connectivity.
-   **[Install ServiceNow SQL API ODBC driver on client machine](../task/install-odbc-driver.md)**  
Install the ServiceNow ODBC driver on your Windows client machine to enable connectivity between your Business Intelligence \(BI\) tools and ServiceNow data through the SQL API.
-   **[Configure ServiceNow SQL API ODBC driver on client machine](../task/configure-odbc-driver.md)**  
Configure connection settings for the installed ODBC driver including server URL and authentication credentials to enable data access from BI tools to your ServiceNow instance.
-   **[Test SQL API ODBC driver connection using Interactive SQL](../task/test-sql-api-odbc-driver-connection-using-interactive-sql.md)**  
Run the Interactive SQL application for quick verification of connectivity and to test query results without using a full application.
-   **[Configure ServiceNow SQL API JDBC driver on client machine](../task/configure-jdbc-driver.md)**  
Configure the JDBC driver settings on your client machine to establish a connection to your ServiceNow instance and access data through the SQL API.
-   **[Route SQL API calls to Read Replica](../task/routing-sql-api-calls-to-read-replica.md)**  
You can route SQL API calls to Read Replica to optimize the performance of your ServiceNow instance.

**Parent Topic:**[Access your ServiceNow data using SQL API](accessing-your-servicenow-data-using-sql-api.md)

