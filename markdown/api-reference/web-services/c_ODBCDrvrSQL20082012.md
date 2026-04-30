---
title: ODBC driver in SQL Server
description: Use the ServiceNow ODBC driver in SQL Server as a Linked Server.
locale: en-US
release: yokohama
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [ODBC and client applications, Create data sources from other apps using ODBC driver, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# ODBC driver in SQL Server

Use the ServiceNow ODBC driver in SQL Server as a Linked Server.

Using the ODBC driver in SQL Server as a [Linked Server](http://msdn.microsoft.com/en-us/library/ms188279.aspx) allows SQL Server to query tables from a ServiceNow instance directly via the ODBC driver. Only use the procedures described with SQL Server 2008 and 2012. Other versions of SQL Server may cause unexpected behavior. If you encounter unexpected behavior, refer to the [troubleshooting linked server Knowledge Base article](https://support.servicenow.com/kb_view.do?sysparm_article=KB0538992).

## Required Permissions

Additional information on the required permissions for SQL Server Linked Servers can be found [on the MSDN blog](http://blogs.msdn.com/b/dataaccesstechnologies/archive/2010/08/19/permissions-needed-to-set-up-linked-server-with-out-of-process-provider.aspx).

**Note:** Review this information if you encounter permission errors with SQL Server.

-   **[ODBC SQL Server video tutorials](../reference/r_ODBCSQLServerVideos.md)**  
Watch video tutorials about configuring and troubleshooting the ODBC driver with a SQL Linked Server.
-   **[Configure SQL Server](../task/t_ConfiguringSQLServer.md)**  
The following example configuration was performed on SQL Server 2008, installed on Windows Server 2008.

**Parent Topic:**[ODBC and client applications](../reference/r_ODBCAndClientApplications.md)

