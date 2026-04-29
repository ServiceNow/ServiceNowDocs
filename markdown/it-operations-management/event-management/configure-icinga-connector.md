---
title: Configure event collection from an Icinga2 connector
description: Configure the Icinga 2 \(Icinga\) connector instance to receive events while monitoring your network resources.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure a pull connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Configure event collection from an Icinga2 connector

Configure the Icinga 2 \(Icinga\) connector instance to receive events while monitoring your network resources.

## Before you begin

Role required: evt\_mgmt\_admin

Supported version: 2.4.1.

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Integrations** &gt; **Connector Instances**.

2.  Click **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Descriptive and unique name for the Icinga connector.|
    |Description|Description for the use of the Icinga event collection instance.|
    |Connector definition|Name of the required connector definition. Select **Icinga2**.|
    |Host IP|IP address where Icinga is installed.|
    |Credential|Permission to connect to Icinga. Click the search icon in the **Credential** field. Use Basic Authentication credentials. Either select the required credentials from the list or click **New** and create the required credentials on the Credentials form. If you create the credentials, save them using a unique and recognizable name, for example, ICINGA2CHCK.|
    |Event collection last run time|Last run time value. Automatically updated.|
    |Last event collection status|Last run status. Automatically updated.|
    |Event collection schedule \(seconds\)|Frequency, in seconds, that the system checks for new events from Icinga. The default value is 120 seconds.|
    |Last error message|Last error message. Automatically updated.|

4.  Right-click the form header and select **Save**.

    The connector instance values are added to the form and the parameters that are relevant to the connector appear.

    ![Icinga Connector Instance Values](../image/icinga2-connector-values.png)

    1.  debug: Display debug messages. Default value: false. Specify true to see debug messages.
    2.  logPayloadForDebug: Display payload related debug messages. Default value: false. Specify true to see payload related debug messages.
5.  In the Connector Instance Values section, verify and where required, modify the default connector instance values.

<table id="table_ynl_553_mfb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

debug

</td><td>

Display debug messages. Default value: `false`. Specify `true` to see debug messages.

</td></tr><tr><td>

port

</td><td>

Number of the connector port. Default value: `5665`.

</td></tr><tr><td>

protocol

</td><td>

Type of protocol. Default protocol type: `https`.

</td></tr><tr><td>

alert\_type

</td><td>

Provide the Icinga alert type details. There are 2 types of an alert in Icinga2: SOFT and HARD

 SOFT: Connector instance will pull a soft alert.

 HARD: Connector instance will pull a hard alert.

</td></tr></tbody>
</table>6.  In the MID Servers for Connectors section, specify a MID Server that is up and is valid.

    If no MID Server is specified, an available MID Server that has a matching IP range is used.

    You can configure several MID Servers. If the first is down, the next MID Server is used. If that MID Server is not available, the next is selected, and so on. MID Servers are sorted according to the order that their details were entered into the MID Server for Connectors section.

7.  Right-click the form header and select **Save**.

8.  Test the connection between the MID Server and the Icinga connector.

    1.  Click **Test Connector**.

        If the test fails, follow the instructions that the error issues to correct the problem and then run another test.

        **Note:** Use a network tool, such as ping, to verify credential correctness and network connectivity from the MID Server to the external monitoring tool.

    2.  After a successful test, select the **Active** check box.

9.  Click **Update**.


**Parent Topic:**[Configure a pull connector](t_EMConfigureConnectorInstance.md)

