---
title: Prepare to run the Microsoft SQL Server collector
description: Configure authentication and permissions before running the collector.Create a service account and grant permissions for NTLM authentication.Create a SQL Server login and grant permissions for username and password authentication.Register an Azure application and grant permissions for Service Principal authentication.Grant SQLAgentReaderRole permissions to harvest Agent job metadata.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-05-08"
reading_time_minutes: 4
keywords: [SQL Server Agent, Agent jobs, SQLAgentReaderRole, msdb database, SQL Server authentication, SQL Server login, username password, database permissions, SQL Server Agent, Agent jobs, SQLAgentReaderRole, msdb database]
breadcrumb: [Microsoft SQL Server metadata collector, Configuring metadata collectors, Data Catalog, Workflow Data Fabric]
---

# Prepare to run the Microsoft SQL Server collector

Configure authentication and permissions before running the collector.

## Before you begin

Role required: admin

## About this task

The collector supports three authentication methods for Microsoft SQL Server. All methods require SELECT ON DATABASE permission for metadata access. VIEW DEFINITION permission is required for column-level lineage harvesting.

## Procedure

1.  Select an authentication method and complete the corresponding setup task.

    -   Username and password authentication - See [Set up username and password authentication](prepare-to-run-microsoft-sql-server-collector.md#)
    -   NTLM authentication- See [Set up NTLM authentication](prepare-to-run-microsoft-sql-server-collector.md#)
    -   Microsoft Entra Service Principal authentication - See [Set up Service Principal authentication](prepare-to-run-microsoft-sql-server-collector.md#)
2.  Grant SQLAgentReaderRole permissions to harvest Agent job metadata.

    See [Set up permissions for harvesting SQL Server Agent jobs](prepare-to-run-microsoft-sql-server-collector.md#).


**Parent Topic:**[Microsoft SQL Server metadata collector](../concept/microsoft-sql-server-metadata-collector.md)

## Set up NTLM authentication

Create a service account and grant permissions for NTLM authentication.

### Before you begin

Role required: admin

The computer running the collector must be attached to the Active Directory domain.

### About this task

Configure NTLM authentication using an Active Directory service account with the minimum required permissions for metadata harvesting.

### Procedure

1.  Create a service account in Active Directory.

2.  Grant SELECT ON DATABASE permission.

    This permission allows the collector to harvest catalog data assets such as tables, views, and columns.

    ```
    GRANT SELECT ON DATABASE :: <databaseName> TO <user>;
    ```

    Replace `<databaseName>` and `<user>` with your values.

3.  Grant VIEW DEFINITION permission.

    This permission enables column-level lineage harvesting from views.

    ```
    GRANT VIEW DEFINITION ON DATABASE :: <databaseName> TO <user>;
    ```

    Replace `<databaseName>` and `<user>` with your values.

4.  Assign the public role for table size information.

    This allows the collector to run the sp\_spaceused stored procedure.

    See the [sp\_spaceused documentation](https://learn.microsoft.com/en-us/sql/relational-databases/system-stored-procedures/sp-spaceused-transact-sql) for details.


### What to do next

When configuring the collector, set these JDBC properties: `integratedSecurity=true`, `authenticationScheme=NTLM`

## Set up username and password authentication for SQL Server collector

Create a SQL Server login and grant permissions for username and password authentication.

### Before you begin

Role required: admin

### About this task

Configure a SQL Server login with the minimum required permissions for metadata harvesting.

### Procedure

1.  Create a login with password.

    ```
    CREATE LOGIN <loginName> WITH PASSWORD = '<password>';
    ```

    Replace `<loginName>` and `<password>` with your values.

2.  Create a user for the login.

    ```
    CREATE USER <user> FOR LOGIN <loginName>;
    ```

    Replace `<user>` and `<loginNam>` with your values.

3.  Grant SELECT ON DATABASE permission.

    This permission allows the collector to harvest catalog data assets such as tables, views, and columns.

    ```
    GRANT SELECT ON DATABASE :: <databaseName> TO <user>;
    ```

    Replace `<databaseName>` and `<user>` with your values.

4.  Grant VIEW DEFINITION permission.

    This permission enables column-level lineage harvesting from views.

    ```
    GRANT VIEW DEFINITION ON DATABASE :: <databaseName> TO <user>;
    ```

    Replace `<databaseName>` and `<user>` with your values.

5.  : Grant execute permission for sp\_spaceused.

    This permission allows the collector to harvest table size information.

    ```
    GRANT EXECUTE ON sp_spaceused TO <user>;
    ```

    Replace `<user>` with your value.


### What to do next

See the [Microsoft SQL Server permissions documentation](https://learn.microsoft.com/en-us/sql/relational-databases/security/permissions-database-engine) for more information about database permissions.

## Set up Service Principal authentication

Register an Azure application and grant permissions for Service Principal authentication.

### Before you begin

Role required: admin

### About this task

Configure Microsoft Entra Service Principal authentication by registering an Azure application and granting database access.

### Procedure

1.  Register a new application in Azure.

    1.  Navigate to **Azure Portal** &gt; **App Registrations**.

    2.  Select **New Registration**.

    3.  Enter the application name.

        Example: MySQLServerApplication.

    4.  For **Supported account types**, select **Accounts in this organizational directory only**.

    5.  Select **Register**.

2.  Create a client secret.

    1.  On the application page, select **Certificates and Secrets** &gt; **Client secrets**.

    2.  Select **New client secret**.

    3.  Add a description and set the expiration date.

    4.  Select **Add**.

    5.  Copy the secret value.

3.  Grant the service principal access to SQL Server.

    1.  In Azure Portal, navigate to your SQL Server instance.

    2.  Select **Access control \(IAM\)** &gt; **Add Role Assignment**.

    3.  Select **Reader** under the **Job function roles** tab.

    4.  Select **Next**.

    5.  For **Assign access to**, verify that **User, group or service principal** is selected.

    6.  Select **Select members**.

    7.  Search for your registered application name and select it.

    8.  Select **Review + assign**.

4.  Grant the service principal access to the database.

    1.  Connect to SQL Server using SQL Server Management Studio.

    2.  Run this command:

        ```
        CREATE USER [<service-principal>] FROM EXTERNAL PROVIDER;
        ```

        Replace `<service-principal>` with your service principal name.

    3.  Grant SELECT ON DATABASE permission.

        ```
        GRANT SELECT ON DATABASE :: <databaseName> TO [<service-principal>];
        ```

        Replace `<databaseName>` and `<service-principal>` with your values.

    4.  Grant VIEW DEFINITION permission.

        ```
        GRANT VIEW DEFINITION ON DATABASE :: <databaseName> TO [<service-principal>];
        ```

        Replace `<databaseName>` and `<service-principal>` with your values.


### What to do next

See the [Microsoft Entra authentication documentation](https://learn.microsoft.com/en-us/azure/app-service/configure-authentication-provider-aad) for more information.

## Set up permissions for harvesting SQL Server Agent jobs

Grant SQLAgentReaderRole permissions to harvest Agent job metadata.

### Before you begin

Role required: sysadmin

### About this task

To harvest SQL Server Agent job metadata, assign the SQLAgentReaderRole in the msdb system database.

### Procedure

1.  Locate the user that is used for running the collector.

2.  Grant SQLAgentReaderRole to the user.

    ```
    USE msdb;
    EXEC sp_addrolemember 'SQLAgentReaderRole', '<username>';
    ```

    Replace `<username>` with your user name.


