---
title: Configure event collection from NNMi
description: Configure the HP Network Node Manager i \(NNMi\) connector instance to receive events while monitoring your network resources.
locale: en-US
release: xanadu
product: Event Management
classification: event-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configure a pull connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM Health, IT Operations Management]
---

# Configure event collection from NNMi

Configure the HP Network Node Manager i \(NNMi\) connector instance to receive events while monitoring your network resources.

## Before you begin

Supported version: 10.30.653.

Role required: evt\_mgmt\_admin

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Integrations** &gt; **Connector Instances**.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_usg_pq2_sbb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Descriptive and unique name for the NNMi connector.

</td></tr><tr><td>

Description

</td><td>

Description for the use of the NNMi event collection instance.

</td></tr><tr><td>

Connector definition

</td><td>

Name of the required connector definition. Select **NNMi**.

</td></tr><tr><td>

Host IP

</td><td>

IP address where NNMi is installed.

</td></tr><tr><td>

Credential

</td><td>

Permission to connect to NNMi. Click the search icon in the **Credential** field. Either select the required credentials from the list or click **New** and create the required credentials on the Credentials form. If you create the credentials, save them using a unique and recognizable name, for example, NNMiCHCK.The selected credentials use basic authentication.

</td></tr><tr><td>

Event collection last run time

</td><td>

Last run time value. Automatically updated.

</td></tr><tr><td>

Last event collection status

</td><td>

Last run status. Automatically updated.

</td></tr><tr><td>

Event collection schedule \(seconds\)

</td><td>

Frequency, in seconds, that the system checks for new events from NNMi. The default value is 120 seconds.

</td></tr><tr><td>

Last error message

</td><td>

Last error message. Automatically updated.

</td></tr></tbody>
</table>4.  Right-click the form header and select **Save**.

    The connector instance values are added to the form and the parameters that are relevant to the connector appear. ![NNMi Connector Instance Values](../image/nnmi-connector-values.png)

5.  In the Connector Instance Values section, verify and where required, modify the default connector instance values.

<table id="table_qjb_lzx_fdb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

days\_from

</td><td>

Number of days for which events must be collected at the first collection cycle. Default value: `7` days. **Note:** The maximum number of past events that can be collected is 3,000. The first time that the connector runs, it collects all events \(up to the 3,000 limit\) that were created from the `days_from` date until the current date.

</td></tr><tr><td>

debug

</td><td>

Display debug messages. Default value: `false`. Specify `true` to see debug messages.

</td></tr><tr><td>

port

</td><td>

Number of the connector port. Default value: `80`.

</td></tr><tr><td>

protocol

</td><td>

Type of protocol. Default protocol type: `http`.

</td></tr></tbody>
</table>6.  In the MID Servers for Connectors section, specify a MID Server that is up and is valid.

    If no MID Server is specified, an available MID Server that has a matching IP range is used.

    You can configure several MID Servers. If the first is down, the next MID Server is used. If that MID Server is not available, the next is selected, and so on. MID Servers are sorted according to the order that their details were entered into the MID Server for Connectors section.

7.  Right-click the form header and select **Save**.

8.  Test the connection between the MID Server and the NNMi connector.

    1.  Click **Test Connector**.

        If the test fails, follow the instructions that the error issues to correct the problem and then run another test.

        **Note:** Use a network tool, such as ping, to verify credential correctness and network connectivity from the MID Server to the external monitoring tool.

    2.  After a successful test, select the **Active** check box.

9.  Click **Update**.


**Parent Topic:**[Configure a pull connector](t_EMConfigureConnectorInstance.md)

