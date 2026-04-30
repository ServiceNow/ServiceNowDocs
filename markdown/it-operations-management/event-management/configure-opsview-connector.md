---
title: Configure Opsview\_v2 connector
description: Configure the Opsview\_V2 connector instance to receive alerts from an Opsview Monitor source.
locale: en-US
release: yokohama
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configure a pull connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Configure Opsview\_v2 connector

Configure the Opsview\_V2 connector instance to receive alerts from an Opsview Monitor source.

## Before you begin

Ensure you have the supported version of the Opsview\_V2 connector: 6.7.0.

Role required: evt\_mgmt\_admin

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Integrations** &gt; **Connector Instances**.

2.  Click **New** and create a connector instance with the following details:

<table id="table_h1z_lm2_sbb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Descriptive name for the Opsview connector.

</td></tr><tr><td>

Description

</td><td>

Description for the use of the Opsview event collection instance.

</td></tr><tr><td>

Host IP

</td><td>

Specify the Opsview IP address.

</td></tr><tr><td>

Credential

</td><td>

Either select the required credentials from the list or click **New** and create the required credentials. If you create the credentials, save them using a unique and recognizable name, for example, OpsviewOPS.**Note:** User should have the CONFIGUREVIEW role with access to 'VIEW ALL, CHANGE NONE'.

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

The frequency in seconds that the system checks for new events from Opsview.

</td></tr><tr><td>

Last error message

</td><td>

The last error message is automatically updated.

</td></tr><tr><td>

Connector definition

</td><td>

Select **Opsview\_v2**.

</td></tr><tr><td>

Connector Instance Values section

</td><td>

The parameters that are specific to Opsview\_V2 display here when the form is saved.

</td></tr><tr><td>

MID Servers \(MID Server for Connectors section\)

</td><td>

Optional. Name of a MID Server. If no MID Server is specified, an available MID Server that has a matching IP range is used. In the MID Servers for Connectors section, specify a MID Server that is up and valid. You can configure several MID Servers. If the first is down, the next MID Server is used. If that MID Server is not available, the next is selected, and so on. MID Servers are sorted according to the order that their details were entered into the MID Server for Connectors section.

</td></tr></tbody>
</table>3.  Right-click the form header and select **Save**.

    The connector instance values are added to the form and the parameters that are relevant to the connector appear.

4.  In the Connector Instance Values section, specify the Opsview\_v2 values.

    1.  **days\_from**.

        Specify the number of days for which events must be collected at the first collection cycle. Default value 7 days.

    2.  **debug**.

        Display debug messages. Default value: false. Specify true to see debug messages.

    3.  **logPayloadForDebug**.

        Display payload related debug messages. Default value: false. Specify true to see payload related debug messages.

    4.  **eventtype\_filter**.

        Specify filters for event collection based on the eventtype attribute. Specify one of these values 0,1,2,3.

    5.  **port**.

        Default value is 80.

        .

    6.  **protocol**.

        The default protocol type is HTTPS.

5.  Right-click the form header and select **Save**.

6.  To verify the connection between the MID Server and the connector, select **Test Connector**.

7.  If the test fails, follow the instructions that the error issues to correct the problem and then run another test.

    If this message appears: `Connection test failed: Failed to connect to Opsview on test connector. Invalid API Key`, then enter the API Key for the specific user to be able to read the Opsview events.

    **Note:** Use a network tool, such as ping, to verify credential correctness and network connectivity from the MID Server to the Opsview Monitor source.

8.  After a successful test, select the **Active** check box and then select **Update**.


**Parent Topic:**[Configure a pull connector](t_EMConfigureConnectorInstance.md)

