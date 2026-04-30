---
title: Configure event collection from HPOM
description: Configure the HPOM connector instance to receive events from HP Operations Manager \(HPOM\).
locale: en-US
release: yokohama
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Configure a pull connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Configure event collection from HPOM

Configure the HPOM connector instance to receive events from HP Operations Manager \(HPOM\).

## Before you begin

Role required: evt\_mgmt\_admin

Supported version: 08.60.005.

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Integrations** &gt; **Connector Instances**.

2.  Click **New** and create an HPOM connector instance with the following details:

    |Field|Value|
    |-----|-----|
    |Name|Specify a unique name for the HPOM connector instance.|
    |Host IP|Specify the HPOM IP address.|
    |Credential|Click in the **Credential** field. Select a credential from the list or click the search icon. Either select the required credentials from the list or click **New** and create the required credentials. If you create the credentials, save them using a unique and recognizable name, for example, HPOMOPS.|
    |Schedule \(seconds\)|The frequency in seconds that the system checks for new events from HPOM.|
    |Description|Type a description for the use of the HPOM event collection instance.|
    |Connector definition|The vendor and protocol used to gather events from the external event source. Select the **HPOM** connector definition.|
    |Last error message|The last error message is automatically updated.|
    |Last run time|The last run time value is automatically updated.|
    |Last run status|The last run time status is automatically updated.|
    |MID Servers \(MID Server for Connectors section\)|Optional. Name of a MID Server. If no MID Server is specified, an available MID Server that has a matching IP range is used. In the MID Servers for Connectors section, specify a MID Server that is up and valid. You can configure several MID Servers. If the first is down, the next MID Server is used. If that MID Server is not available, the next is selected, and so on. MID Servers are sorted according to the order that their details were entered into the MID Server for Connectors section.|

3.  Right-click the form header and click **Save**.

    The connector instance values are added to the form and the parameters that are relevant to the connector appear.

4.  In the Connector Parameters section, specify the values of the mandatory HPOM parameters.

    -   **driver**. Specify the driver to be used to make the call. This driver is specific to the type of database you are calling into.
        -   For an IBM DB2 Universal driver, specify: com.ibm.db2.jcc.DB2Driver
        -   For an Oracle driver, specify: oracle.jdbc.OracleDriver
        -   For a Microsoft SQL driver, specify: com.microsoft.sqlserver.jdbc.SQLServerDriver
        -   For a MySQL driver, specify: com.mysql.jdbc.Driver
        -   For a Sybase driver, specify: com.sybase.jdbc3.jdbc.SybDriver
    -   **url**. Specify a URL. The JDBC protocol uses a connection string to establish the authentication and other parameters to establish a connection between the client and the database. Each database has its own connection string format. In the following URLs, replace the variables, for example, &lt;username&gt; and &lt;password&gt;, with your values.
        -   For an IBM DB2 Universal URL, specify: \[jdbc:db2://sysmvs1.stl.ibm.com:&lt;port number&gt;/&lt;database name&gt;:user=&lt;username&gt;;password=&lt;password&gt;\]

            For example: jdbc:db2://sysmvs1.stl.ibm.com:5021/regionsdb:user=example;password=wlrs21.

        -   For an Oracle URL, specify: \[jdbc:oracle:thin:@&lt;IP address&gt;:&lt;port number&gt;:&lt;database name&gt;\]

            For example: jdbc:oracle:thin:@172.31.255.255:4028:OracleMain.

        -   For a Microsoft SQL URL, specify: \[jdbc:sqlserver://&lt;IP address&gt;;user=&lt;username&gt;;password=&lt;password&gt;\]

            For example: jdbc:sqlserver://localhost;user=example;password=w3lrs2.

        -   For a MySQL URL, specify: \[jdbc:mysql://&lt;IP address&gt;/database?user=&lt;username&gt;;password=&lt;password&gt;\]

            For example: jdbc:mysql://localhost/database?user=example;password=65wlrs.

        -   For a Sybase URL, specify: \[jdbc:sybase:Tds:&lt;IP address&gt;:&lt;port number&gt;/&lt;database name&gt;?user=&lt;username&gt;;password=&lt;password&gt;\]

            For example: jdbc:sybase:Tds:172.31.255.255:4100/SYBMAIN?user=example;password=wlrs1m.

5.  Use a network tool, such as ping, to verify that the HPOM server is running and the IP address matches the value in the **Host IP** field.

6.  Click **Test connector** to verify the connection between the MID Server and the HPOM connector.

7.  If the test fails, follow the instructions that the error issues to correct the problem and then run another test.

    **Note:** Use a network tool, such as ping, to verify credential correctness and network connectivity from the MID Server to the HPOM server.

8.  After a successful test, select **Active** and then click **Update**.


**Parent Topic:**[Configure a pull connector](t_EMConfigureConnectorInstance.md)

**Related topics**  


[Configure a pull connector](t_EMConfigureConnectorInstance.md)

