---
title: Configure event collection from Zabbix server
description: Configure the Zabbix server connector instance to receiving alerts from the Zabbix server.
locale: en-US
release: yokohama
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configure a pull connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Configure event collection from Zabbix server

Configure the Zabbix server connector instance to receiving alerts from the Zabbix server.

## Before you begin

Supported versions: from 3.0.0 up to 7.0.0

The Zabbix server connector instance requires a credential that lets the instance access Zabbix server accounts. You can use an existing credential or [create a new one](create-credentials-zabbix.md).

Role required: evt\_mgmt\_admin

## About this task

This connector has the **logPayloadForDebug** log parameter enabled, which logs event and metric payloads from the source system. Once debugging is complete, set this parameter to **false** to prevent overloading the system.

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Integrations** &gt; **Connector Instances**.

2.  Click **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Descriptive name for the connector.|
    |Host IP|IP address for the Zabbix server.|
    |Credential|Select the credential with basic authentication that you created for this connector. For more information, see [Create Zabbix server credentials](create-credentials-zabbix.md).|
    |Schedule \(seconds\)|Frequency, in seconds, that the system checks for new events from the Zabbix server.|
    |Description|Description for the use of the Zabbix server event collection instance.|
    |Connector Definition|Name of the connector definition. Select **Zabbix**.|
    |Last error message|Last error message. Automatically updated.|
    |Last run time|Last run time value. Automatically updated.|
    |Last run status|Last run time status. Automatically updated.|
    |MID Servers \(MID Server for Connectors section\)|Optional. Name of a MID Server. If no MID Server is specified, an available MID Server that has a matching IP range is used. In the MID Servers for Connectors section, specify a MID Server that is up and valid. You can configure several MID Servers. If the first is down, the next MID Server is used. If that MID Server is not available, the next is selected, and so on. MID Servers are sorted according to the order that their details were entered into the MID Server for Connectors section.|

4.  Right-click the form header and select **Save**.

    The connector instance values are added to the form and the parameters that are relevant to the connector appear.![Zabbix connector values](../image/zabbix-connector-values.png)

5.  Verify and modify the values, as needed.

    In the Connector Instance Values section, the default connector instance values appear.

<table id="table_fnm_wbr_k2b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

days\_from

</td><td>

Number of days for which events must be collected at the first collection cycle. Default value: `2` **Note:** The maximum number of past events that can be collected is 3,000. The first time that this connector runs, the number of past events is counted in the past from the current date.

</td></tr><tr><td>

port

</td><td>

Port number. Default: `80`

</td></tr><tr><td>

protocol

</td><td>

Protocol type. Default: `https`

</td></tr></tbody>
</table>6.  Right-click the form header and select **Save**.

7.  Click **Test Connector** to verify the connection between the MID Server and the connector.

8.  If the test fails, follow the instructions that are issued by the error to correct the problem and then run another test.

    **Note:** Use a network tool, such as ping, to verify credential correctness and network connectivity from the MID Server to the Zabbix server.

9.  After a successful test, select **Active** and then click **Update**.


-   **[Create Zabbix server credentials](create-credentials-zabbix.md)**  
Create credentials to access Zabbix server.

**Parent Topic:**[Configure a pull connector](t_EMConfigureConnectorInstance.md)

