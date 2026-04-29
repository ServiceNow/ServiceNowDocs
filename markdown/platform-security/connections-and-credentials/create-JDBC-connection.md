---
title: Create a JDBC connection
description: The JDBC Connection provides the information custom JDBC actions or activities use to connect to various target databases.
locale: en-US
release: australia
product: Connections and Credentials
classification: connections-and-credentials
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Get started with connections, Connections and Credentials, Access Management]
---

# Create a JDBC connection

The JDBC Connection provides the information custom JDBC actions or activities use to connect to various target databases.

## Before you begin

You must have an appropriate JAR file, whether it is supplied with the instance or a custom JAR file.

**Note:** The ServiceNow instance supplies `mysql-connector-java-5.1.21.jar`, `sql-server-jdbc-4.0.jar`, and `ojdbc6.jar` files as part of the current release, which supports MySQL, SQLServer, and Oracle databases. Other databases, such as Sybase or DB2 Universal, must use a custom JAR file that must be uploaded to the instance before setting the JDBC connection.

Role required: connection\_admin

## About this task

JDBC credentials are retrieved separately by the activity designer template and support [external credential storage](../concept/c_ExternalCredentialStorage.md), such as CyberArk.

## Procedure

1.  Navigate to **All** &gt; **Credentials &amp; Connections** &gt; **Connections**, click **New** and select **JDBC Connection**.

2.  Complete the form using the fields in the table.

    The database selection in the **Format** field determines which fields are available.

<table id="table_dls_tpv_sx"><thead><tr><th>

Field

</th><th>

Database Format

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

All

</td><td>

Unique name of this JDBC connection. For example, you might enter **JDBC MySQLProd**.

</td></tr><tr><td>

Credential

</td><td>

All

</td><td>

Add credentials for JDBC provider.

</td></tr><tr><td>

Connection alias

</td><td>

All

</td><td>

Select the alias record to associate with this connection. Using an alias enables you to update the connection record without having to reconfigure any actions or activities that use the alias.

</td></tr><tr><td>

Query timeout

</td><td>

All

</td><td>

Maximum elapsed time the JDBC query is allowed to run without a response.

</td></tr><tr><td>

Connection timeout

</td><td>

All

</td><td>

Number of seconds the system waits before closing a JDBC connection or connection request.

 For example, if the **Connection Timeout** value is 10 seconds, the system waits 10 seconds for a successful connection. If a successful connection does not occur during this time, the connection request times out. If a successful connection does occur, the connection remains open until there is a 10-second period of inactivity. Once the connection has been inactive for 10 seconds, the connection is closed.

 **Note:** Avoid setting the **Connection Timeout** value to zero, as this may cause a stale connection.

</td></tr><tr><td>

Active

</td><td>

All

</td><td>

Check the box to make this an active connection.

</td></tr><tr><td>

Domain

</td><td>

All

</td><td>

Domain for this table. By default, the JDBC Connection \[jdbc\_connection\] table runs in the **global** domain.

</td></tr><tr><td>

Format

</td><td>

All

</td><td>

Database type for this connection. The default choices are: -   **MySQL**
-   **Oracle**
-   **SQLServer**
-   **None**
 You can add **Sybase** or **DB2 Universal** to the choice list by uploading the appropriate JDBC driver JAR file to the instance. Orchestration automatically recognizes these drivers when they are loaded into the system and adds them to this list.

</td></tr><tr><td>

Host

</td><td>

Oracle, MySQL, SQLServer

</td><td>

Host name or IP address of the database server.

</td></tr><tr><td>

Oracle sid

</td><td>

Oracle

</td><td>

The Oracle database site identifier. The default value is **orcl**.

</td></tr><tr><td>

Oracle port

</td><td>

Oracle

</td><td>

Port that the Oracle database is using. The default value is **1521**.

</td></tr><tr><td>

Database name

</td><td>

MySQL, SQLServer

</td><td>

Name of the database.

</td></tr><tr><td>

Port

</td><td>

My SQL, SQLServer

</td><td>

Port that the selected database is using.

</td></tr><tr><td>

Instance name

</td><td>

SQLServer

</td><td>

Instance name for the selected SQLServer

</td></tr><tr><td>

Connection URL

</td><td>

All

</td><td>

URL that the MID Server uses to connect to the specified database. The URL is created automatically when you save the form, and is read-only for the default databases. **Note:** If the format selected is not one of the default databases, you must create the connection URL manually so that the MID Server knows how to create the connection.

</td></tr><tr><td>

JDBC driver

</td><td>

None, DB2 Universal, Sybase

</td><td>

The JDBC driver to use for this connection when it is not a default database. **Note:** If you add a Sybase or DB2 Universal database, you must enter the driver name in this field and upload the driver JAR file to the instance.

</td></tr><tr><td>

Use MID server

</td><td>

All

</td><td>

Check to use a MID server for this action or activity. If selected, define fields in the Advanced MID Server Configuration section.

</td></tr><tr><td>

MID Selection

</td><td>

All

</td><td>

Option to select a specific MID Server or MID Cluster. Choose any one of the following options. -   **Auto-Select MID Server**: Your ServiceNow instance selects the MID Server without manual input.
-   **Specific MID Server**: Your ServiceNow instance uses MID Server that you specify.
-   **Specific MID Cluster**: Your ServiceNow instance uses the MID Cluster that you specify.

A MID Cluster is a group of MID Servers that enables your ServiceNow instance to handle multiple integrations, and improve integration speed. For more information, see [Configure a MID Server cluster](https://www.servicenow.com/docs/access?context=t_ConfigureAMIDServerCluster&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

 This field is available when **Use MID Server** is checked. **Note:** Ensure that the Integration Hub connection record is referred, not an Orchestration connection record.

</td></tr><tr><td>

Capabilities

</td><td>

All

</td><td>

The capabilities the MID Server must support to be eligible for selection. The system runs the action or activity from a MID Server that supports the selected capabilities. Only displays if **Use MID server** is selected.

 Required capabilities determine which MID Server is selected at runtime. To learn more about how a MID Server is selected during runtime, see [MID Server selection](https://www.servicenow.com/docs/access?context=c_MIDServerSelector&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US). This field is visible only when **Auto-Select MID Server** is selected from the MID Selection list.

</td></tr><tr><td>

MID Application

</td><td>

All

</td><td>

The application the MID Server must support to be eligible for selection. The system runs the action from a MID Server that supports the selected application. Only displays if **Use MID server** is selected.

 To learn more about how a MID Server is selected during runtime, see [MID Server selection](https://www.servicenow.com/docs/access?context=c_MIDServerSelector&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

MID Server

</td><td>

All

</td><td>

Specific MID Server on which the step runs. This field is visible only when **Specific MID Server** is selected from the MID Selection list.

</td></tr><tr><td>

MID Cluster

</td><td>

All

</td><td>

The specific MID Cluster you want to use. This field is available when **Use MID Server** is checked, and **Specific MID Cluster** is selected from the MID Selection list.

</td></tr></tbody>
</table>3.  Click **Submit**.


**Parent Topic:**[Get started with connections](../reference/connection-information.md)

**Related topics**  


[JDBC credentials](../reference/r_JDBCCredentialsForm.md)

