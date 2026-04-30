---
title: Configure event collection from IBM Netcool
description: Configure the IBM Netcool\_V2 connector to receive events from IBM Netcool/OMNIbus Object Servers and Impact Servers. The IBM Netcool\_V2 connector uses REST API calls and is bidirectional.
locale: en-US
release: xanadu
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configure a pull connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM Health, IT Operations Management]
---

# Configure event collection from IBM Netcool

Configure the IBM Netcool\_V2 connector to receive events from IBM Netcool/OMNIbus Object Servers and Impact Servers. The IBM Netcool\_V2 connector uses REST API calls and is bidirectional.

## Before you begin

For the IBM Netcool\_V2 connector:

-   Role required: evt\_mgmt\_admin
-   Perform connector validation on IBM NetCool/OMNIbus version 8.1.0.

## About this task

To use IBM Netcool\_V2 connector, configure a connector instance for the MID Server.

**Note:** The IBM Netcool connector is deprecated and only IBM Netcool\_V2 connector is supported.

## Procedure

1.  Navigate to **Event Management** &gt; **Integrations** &gt; **Connector Instances**.

2.  Click **New** and create a connector instance with the following details:

    |Field|Value|
    |-----|-----|
    |Name|Specify a unique name for the Netcool connector instance.|
    |Description|Type a description for the use of the Netcool event collection instance.|
    |Host IP|Specify the Netcool IP address.|
    |Credential|In the Credentials form, click **New**, and create the required credentials. Save the credentials using a unique and recognizable name, for example, NetcoolOPS.|
    |Event collection last run time|The last run time value is automatically updated.|
    |Last event collection status|The last run time status is automatically updated.|
    |Event collection schedule \(seconds\)|The frequency in seconds that the system checks for new events from Netcool. The default value is 120 seconds.|
    |Last error message|The last error message is automatically updated.|
    |Connector definition|Select IBM Netcool\_V2 to gather events from the external event source.|
    |MID Servers \(MID Server for Connectors section\)|Specify a MID Server that is up and is valid. You can configure several MID Servers. If the first is down, the next MID Server is used. If that MID Server is not available, the next is selected, and so on. MID Servers are sorted according to the order that their details were entered into the MID Server for Connectors section. If no MID Server is specified, an available MID Server that has a matching IP range is used.|

3.  Right-click the form header and click **Save**.

    The connector instance values are added to the form and the parameters that are relevant to the connector appear.

4.  In the Connector Parameters section, specify the value of the required Netcool parameters.

<table id="choicetable_ict_hmx_n4b"><thead><tr><th align="left" id="d266316e260">

Connector

</th><th align="left" id="d266316e263">

Required parameters

</th></tr></thead><tbody><tr><td id="d266316e269">

**IBM Netcool\_V2**

</td><td>

**port**: The port number on which IBM Netcool is running. For example: 8080**initial\_sync\_in\_days**: The number of days of data fetched on first pull. The default value is 3, but can be changed according to your requirements.

</td></tr></tbody>
</table>5.  Verify that Netcool servers are up and running:

    For the IBM Netcool\_V2 connector, use this REST API call to verify that the Netcool API is up and running: `http://hostname:port/objectserver/restapi/alerts/status`

6.  Right-click the form header and click **Save**.

7.  Click **Test connector** to verify the connection between the MID Server and the Netcool connector.

8.  If the test fails, follow the instructions that are issued by the error to correct the problem and then run another test.

9.  After a successful test, select the **Active** check box and then click **Update**.


**Parent Topic:**[Configure a pull connector](t_EMConfigureConnectorInstance.md)

**Related topics**  


[Configure a pull connector](t_EMConfigureConnectorInstance.md)

