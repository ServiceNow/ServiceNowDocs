---
title: Configuring Live Connect
description: This section guides you through the complete setup process for the ServiceNow Live Connect, covering both instance configuration and driver installation. You will configure your ServiceNow instance to enable Live Connect access, set up the necessary security controls, and install the appropriate drivers on your client machine.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/api-reference/web-services/configuring-sql-api.html
release: zurich
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [configure]
breadcrumb: [Access your ServiceNow data using Live Connect, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Configuring Live Connect

This section guides you through the complete setup process for the ServiceNow Live Connect, covering both instance configuration and driver installation. You will configure your ServiceNow instance to enable Live Connect access, set up the necessary security controls, and install the appropriate drivers on your client machine.

## Live Connect configuration overview

The configuration process involves two main components:

1.  Instance Setup:

    Configure your ServiceNow instance by installing the Live Connect plugin, creating a dedicated service account with the appropriate access roles, defining Access Control Lists \(ACLs\) to control data access, and establishing IP filtering policies for security.

    -   [Install Live Connect plugin on your ServiceNow instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/web-services/install-sql-api-plugin.md)
    -   [Configure Live Connect plugin on your ServiceNow instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/web-services/configure-sql-api-overview.md)
2.  Driver Installation and Configuration:

    Download the Live Connect drivers from the ServiceNow Store and install either the ODBC driver on your Windows client machine or configure the JDBC driver in your preferred database client.

    -   [Download the Live Connect drivers on client machine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/web-services/download-sql-api-drivers.md)
    -   [Install ServiceNow Live Connect ODBC driver on client machine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/web-services/install-odbc-driver.md)
    -   [Configure ServiceNow Live Connect ODBC driver on client machine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/web-services/configure-odbc-driver.md)
    -   [Configure ServiceNow Live Connect JDBC driver on client machine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/web-services/configure-jdbc-driver.md)

-   **[Install Live Connect plugin on your ServiceNow instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/web-services/install-sql-api-plugin.md)**  
Installing the Live Connect on your instance enables secure, read-only access to your instance data from external applications. You can integrate your data with external tools and analytics platforms to enhance your reporting and data analysis capabilities.
-   **[Configure Live Connect plugin on your ServiceNow instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/web-services/configure-sql-api-overview.md)**  
Overview of the three-step configuration process required to enable Live Connect access including prerequisites and expected outcomes.
-   **[Download the Live Connect drivers on client machine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/web-services/download-sql-api-drivers.md)**  
Download the ODBC and JDBC drivers from the ServiceNow store to your client machine to enable Live Connect connectivity.
-   **[Install ServiceNow Live Connect ODBC driver on client machine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/web-services/install-odbc-driver.md)**  
Install the ServiceNow ODBC driver on your Windows client machine to enable connectivity between your Business Intelligence \(BI\) tools and ServiceNow data through the Live Connect.
-   **[Configure ServiceNow Live Connect ODBC driver on client machine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/web-services/configure-odbc-driver.md)**  
Configure connection settings for the installed ODBC driver including server URL and authentication credentials to enable data access from BI tools to your ServiceNow instance.
-   **[Test Live Connect ODBC driver connection using Interactive SQL](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/web-services/test-sql-api-odbc-driver-connection-using-interactive-sql.md)**  
Run the Interactive SQL application for quick verification of connectivity and to test query results without using a full application.
-   **[Configure ServiceNow Live Connect JDBC driver on client machine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/web-services/configure-jdbc-driver.md)**  
Configure the JDBC driver settings on your client machine to establish a connection to your ServiceNow instance and access data through the Live Connect.
-   **[Route Live Connect calls to Read Replica](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/web-services/routing-sql-api-calls-to-read-replica.md)**  
You can route Live Connect calls to Read Replica to optimize the performance of your ServiceNow instance.

**Parent Topic:**[Access your ServiceNow data using Live Connect](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/web-services/accessing-your-servicenow-data-using-sql-api.md)

