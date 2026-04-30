---
title: Configure SQL Server
description: The following example configuration was performed on SQL Server 2008, installed on Windows Server 2008.
locale: en-US
release: xanadu
product: Web Services
classification: web-services
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [ODBC driver in SQL Server, ODBC and client applications, Create data sources from other apps using ODBC driver, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Configure SQL Server

The following example configuration was performed on SQL Server 2008, installed on Windows Server 2008.

## Before you begin

The ODBC driver must be installed on the same computer on which SQL Server is installed.

## Procedure

1.  Right-click the SQL Server Management Studio application and select **Run as Administrator**.

2.  Log in to the database to which you want to link.

3.  Right-click **Server Objects** &gt; **Linked Servers**.

4.  Click **New Linked Server**.

5.  Enter the following values in the dialog.

    -   Linked server: `SERVICENOW`. This is the name of the Linked Server.
    -   Provider: `Microsoft OLE DB Provider for ODBC drivers`
    -   Product name: `ServiceNow`. This is an identifier. Enter any value that is appropriate.
    -   Data source: `ServiceNow`. This is the name of your DSN.
    ![New Linked Server](../image/NewLinkedServer.png)

6.  Select **Security** from the Select a page list, and then enter the following security values:

    1.  For a login connection, select **Be made using this security context**.
    2.  Enter the user name and password for connecting to the ServiceNow instance.
    3.  Click **OK**.
    ![ODBC SQL Server Security](../image/OdbcSqlserverSecurity.png)

7.  Navigate to **Server Objects** &gt; **Linked Server** &gt; **Providers** and double-click Microsoft **OLE DB Provider for ODBC drivers**.

8.  Select the following options.

    -   Nested Queries
    -   Level zero only
    -   Support 'Like' operator
    **Tip:**

    ServiceNow recommends running the third-party provider in the out-of-process mode setting \(AllowInProcess=FALSE\). If you run the provider in-process \(within the same process as SQL Server\), then any issues with the provider can affect the SQL Server process, which in turn could result in crashing SQL server.

    ![SQL Server Provider Options](../image/SqlserverProviderOptions.jpg)

9.  Test your connection by selecting the newly created linked server SERVICENOW and selecting **Test connection**.

10. Execute the following query in a query builder window to retrieve some results.

    ![ODBC SQL Server Query](../image/OdbcSqlserverQuery.png)


## What to do next

Number Precision Errors

You may encounter precision errors querying for decimal or number field values using the OPENQUERY syntax with the ODBC driver. In this case, use the Cast syntax to convert the precision. For example:

```
SELECT * FROM OPENQUERY (SERVICENOW , 'select Cast(sys_mod_count as Decimal(38,0)), number, short_description from incident' ) GO
```

SQL Server Connection String

To use the ODBC driver directly in SQL Server 2008, specify the connection string in the following format.

```
Dsn=ServiceNow;uid =username;pwd =password
```

**Note:** The latest SQL Server 2008 patches are required for the ability to specify a connection string in the user interface, via the SQL import wizard

Using sp\_addlinkedserver

The following example creates a linked server named "ServiceNow ODBC" that uses the Microsoft OLE DB Provider for ODBC \(MSDASQL\) and the data\_source parameter

```
EXEC sp_addlinkedserver 
   @server  = N 'ServiceNow ODBC' , 
   @srvproduct  = N '' ,
   @provider  = N 'MSDASQL' , 
   @datasrc  = N 'ServiceNow';
 GO
```

After creating the linked server, you must update its properties to specify the login credentials.

**Parent Topic:**[ODBC driver in SQL Server](../concept/c_ODBCDrvrSQL20082012.md)

