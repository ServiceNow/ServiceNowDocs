---
title: Configure event collection from NagiosXI
description: Configure the NagiosXI connector instance to receive events from the Nagios Core monitor.
locale: en-US
release: xanadu
product: Event Management
classification: event-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Configure a pull connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM Health, IT Operations Management]
---

# Configure event collection from NagiosXI

Configure the NagiosXI connector instance to receive events from the Nagios Core monitor.

## Before you begin

Supported version: 5.5.2.

The NagiosXI connector instance requires a credential that lets the instance access NagiosXI accounts. You can use an existing credential or create a new one. For more information, see [Create Nagios XI server credentials](create-credentials-nagiosix.md).

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

Descriptive name for the Nagios connector.

</td></tr><tr><td>

Description

</td><td>

Description for the use of the NagiosXI event collection instance.

</td></tr><tr><td>

Host IP

</td><td>

Specify the Nagios XI IP address.

</td></tr><tr><td>

Credential

</td><td>

Select the credential with basic authentication that you created for this connector. For more information, see [Create Nagios XI server credentials](create-credentials-nagiosix.md). Ensure that the user password contains the NagiosXI user API key, for example 04lquEPqf4JimWCm8RWbJokOpW8LYBUfEvJp9OSHSRYe4QDrHPFndYbWcCHapBpk.

</td></tr><tr><td>

Event collection last run time

</td><td>

The last run time value is automatically updated.

</td></tr><tr><td>

Last event collection status

</td><td>

The last run time status is automatically updated.

</td></tr><tr><td>

Event collection schedule \(seconds\)

</td><td>

The frequency, in seconds, that the system checks for new events from Nagios. The default value is 120 seconds.

</td></tr><tr><td>

Last error message

</td><td>

The last error message is automatically updated.

</td></tr><tr><td>

Connector Definition

</td><td>

Select **NagiosXI**.

</td></tr><tr><td>

MID Servers \(MID Server for Connectors section\)

</td><td>

Optional. Name of a MID Server. If no MID Server is specified, an available MID Server that has a matching IP range is used. In the MID Servers for Connectors section, specify a MID Server that is up and valid. You can configure several MID Servers. If the first is down, the next MID Server is used. If that MID Server is not available, the next is selected, and so on. MID Servers are sorted according to the order that their details were entered into the MID Server for Connectors section.

</td></tr></tbody>
</table>4.  Right-click the form header and select **Save**.

    The connector instance values are added to the form and the parameters that are relevant to the connector appear.

5.  In the Connector Instance Values section, specify the Nagios values.

    -   **initial\_sync\_in\_days**. Specify the number of days for which events must be collected at the first collection cycle. Default value `7` days.
    -   **port**. Default value `80`.
    -   **protocol**. The default protocol type is `http`.
    -   **time\_zone**. The default time zone is `GMT`; update this value to the Nagios timezone. For example, if Nagios is sending the events according to the EDT time zone, update this value to `GMT-04:00` \(abbreviations such as **EDT** are not supported\).
    -   **severity\_by\_state\_type**. The default value is `false`. When set to `true`, the state\_type is used along with the state to determine the severity which creates less critical events as shown in the following mapping table.
    |\_state\_type\(Connector definition parameter\)|State \(Nagios JSON payload attribute\)|State\_type \(Nagios JSON payload attribute\)|ServiceNow Severity|
    |-----------------------------------------------|---------------------------------------|---------------------------------------------|-------------------|
    |false|2|0/1|1 \(Critical\)|
    |false|1|1|1\(Critical\)|
    |false|1|0|2\(Major\)|
    |false|0|0/1|5\(OK\)|
    |true|0|0/1|5\(OK\)|
    |true|1|0|4 \(Warning-soft -&gt; Warning\)|
    |true|2|0|2\(Critical-soft -&gt; Major\)|
    |true|3|0|4\(Unknown-soft-&gt; Warning\)|
    |true|1|1|3\(Warning-hard -&gt; Minor\)|
    |true|2|1|1\(Critical-hard -&gt; Critical\)|
    |true|3|1|3\(Unknown-hard -&gt; Minor\)|

6.  Right-click the form header and select **Save**.

7.  Click **Test Connector** to verify the connection between the MID Server and the connector.

8.  If the test fails, follow the instructions that the error issues to correct the problem and then run another test.

    If this message appears: `Connection test failed: Failed to connect to Nagios on test connector. Invalid API Key`, then enter the API Key for the specific user to be able to read the Nagios events.

    **Note:** Use a network tool, such as ping, to verify credential correctness and network connectivity from the MID Server to the Nagios Core monitor.

9.  After a successful test, select the **Active** check box and then click **Update**.


-   **[Create Nagios XI server credentials](create-credentials-nagiosix.md)**  
Create credentials to access Nagios XI server.

**Parent Topic:**[Configure a pull connector](t_EMConfigureConnectorInstance.md)

