---
title: Get started with connections
description: Use the connections table to set up a Basic, JMS, JDBC, or HTTP\(s\) connection to a target host.
locale: en-US
release: australia
product: Connections and Credentials
classification: connections-and-credentials
topic_type: reference
last_updated: "2026-05-09"
reading_time_minutes: 2
breadcrumb: [Connections and Credentials, Access Management]
---

# Get started with connections

Use the connections table to set up a Basic, JMS, JDBC, or HTTP\(s\) connection to a target host.

## Connection Table

The Connection table \(sys\_connection\) is the base table for all connection tables. You can set up connections for the following protocols:

-   Basic connection for PowerShell and SSH
-   JDBC
-   JMS
-   HTTP\(s\)

The connection table references the connection alias table, which couples the connection alias to connection information. Every connection records the following information:

|Field|Description|
|-----|-----------|
|Name|Name of the connection. This field must be unique on the table.|
|Credential|Specify the credential to use with this connection. This is optional.|
|Connection alias|The connection alias resolves your connection and credentials at run time. Only one connection is active per Connection alias at any one time.|
|Active|Check to make the current connection active.|
|Domain|Domain to which the connection belongs.|

Credential is unique across active connections, if not empty.

## Upgrading connection information

-   The JDBC connection \[jdbc\_connection\] and JMS connection \[orch\_jms\_ds\] tables are existing Orchestration connection tables that now extend from the Connection \[sys\_connection\] table. The tables originally extended from sys\_metadata. The sys\_metadata related data is removed.
-   The tables move from the Orchestration run time plugin \[com.snc.runbook\_automation.runtime\] to the Credentials &amp; Connections plugin.
-   The upgrade process obtains JDBC and JMS connection information and creates corresponding connection aliases and assigns the alias to its corresponding connection.
-   JDBC field name changes:
    -   JDBC server is renamed to host
    -   Database port is renamed to port
    -   Data of the JDBC server and database migrates to host and port during the upgrade

-   **[Create a basic connection for PowerShell and SSH](../task/configure-ps-connection.md)**  
Configure connection information to use with a custom activity or action that uses the PowerShell or Secure Shell \(SSH\) protocol.
-   **[Create an HTTP\(s\) connection](../task/create-https-connection.md)**  
The HTTP\(s\) connection provides the information custom HTTP\(s\) actions or activities use to connect.
-   **[Create a JDBC connection](../task/create-JDBC-connection.md)**  
The JDBC Connection provides the information custom JDBC actions or activities use to connect to various target databases.
-   **[Create a JMS connection](../task/configure-connection-JMS.md)**  
Configure your system to use Java Messaging Service \(JMS\) with a custom JMS activity or action.
-   **[Create connection attributes for IntegrationHub](../task/create-connection-attributes.md)**  
Define connection-specific variables that you can use in Integration Hub integration steps.

**Parent Topic:**[Connections and Credentials](r-credentials.md)

