---
title: Configure event collection from OBM
description: Configure the Operation Bridge Manager \(OBM\), also known as OMi v2, connector instance to receive alerts from the OBM server. The OBM connector script OBM v2 will be available after installing the Event Management Connectors app.
locale: en-US
release: xanadu
product: Event Management
classification: event-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Configure a pull connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM Health, IT Operations Management]
---

# Configure event collection from OBM

Configure the Operation Bridge Manager \(OBM\), also known as OMi v2, connector instance to receive alerts from the OBM server. The OBM connector script OBM v2 will be available after installing the Event Management Connectors app.

## Before you begin

Supported versions: 10.01, 10.10, 10.11, 10.12, 10.60, 10.61, and 11.01.

Role required: evt\_mgmt\_admin

## About this task

Starting from the Xanadu release, the OOTB \(Out-Of-The-Box\) event rules provided with the connector, which you have not previously used \(i.e., neither activated, deactivated, nor modified\), will now have the **Apply additional matching rules** check box set to true. Previously, this check box was disabled. This change allows you to execute more event rules or automation using the same filter conditions for the events.

**Note:** This feature applies only to active event rules.

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Event Connectors \(Pull\)** &gt; **Connector Instances**.

2.  Click **New** and create a connector instance with the following details:

<table id="table_ykb_xn2_sbb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Descriptive name for the OBM connector.

</td></tr><tr><td>

Description

</td><td>

Description for the use of the OBM event collection instance.

</td></tr><tr><td>

Host IP

</td><td>

Specify the OBM IP address.

</td></tr><tr><td>

Credential

</td><td>

Select the required credentials from the list or click **New** and create the required credentials. If you create the credentials, save them using a unique and recognizable name, for example OBMOPS.

</td></tr><tr><td>

Event collection last run time

</td><td>

The last run time value is automatically updated.

</td></tr><tr><td>

Last event collection status

</td><td>

The last run time value is automatically updated.

</td></tr><tr><td>

Event collection schedule \(seconds\)

</td><td>

Frequency in seconds that the system checks for new events from OBM. The default value is 120 seconds.

</td></tr><tr><td>

Last error message

</td><td>

The last error message is automatically updated

</td></tr><tr><td>

Connector Definition

</td><td>

Select **OBM V2**.**Note:** This script will be available after installing the Event Management connector scoped app.

</td></tr><tr><td>

MID Servers \(MID Server for Connectors section\)

</td><td>

Specify the MID Server to run the OBM connector instance. You can configure several MID Servers. If the first server is down, the next MID Server If that MID Server is not available, the next is selected, and so on. MID Servers are sorted according to the order that their details were entered into the MID Server for Connectors section. If no MID Server is specified, an available MID Server that has a matching IP range is used.

</td></tr></tbody>
</table>3.  Right-click the form header and select **Save**.

    The parameters that are relevant to the OBM connector appear.

4.  In the Connector Instance Values section, specify the OBM values.

    1.  **days\_from**.

        Specify the number of days for which events must be collected on the first collection cycle. The default value is `7` days and data can only be pulled a maximum of 7 days from the OBM system.

    2.  **debug**.

        The default value is `false`. To enter debug mode, change the value to `true`.

    3.  **port**.

        The default value is `80`.

    4.  **protocol**.

        The default value is `http`.

    5.  **query\_filter**.

        The default value is false. If you do want to use this extra filter to query events, specify the event attributes. For example, `assigned_user = "admin" AND title = "My Title"`. The query filter criteria are:

        -   A filter property that specifies an event attribute, such as, `related_ci`
        -   A supported operator, for example, `OR` or `AND`
        -   A value for the filter property, for example, `admin` or `integrator`
        Everything from the query\_filter field undergoes URL encoding and is then passed as a parameter to the OBM API call. For detailed information on how to build the filter query, see “Filtering by Event Attributes: query” in the OBM Extensibility Guide. For example, to query the events for a list of events that are assigned to the admin user, specify:

        `event_list?query=assigned_ user%20EQ%20"admin"`

        To nest query\_filter event attributes, specify the hierarchy using square brackets "\[ \]".

    6.  **inclusion list**.

        The default value is `false`. Specify a comma-separated list to include this feature to add attributes that should be collected and added to the Event Management **Additional information** field.

5.  Right-click the form header and select **Save**.

6.  Click **Test Connector** to verify the connection between the MID Server and the connector.

7.  If the test fails, follow the instructions that the error issues to correct the problem and then run another test.

    **Note:** Use a network tool, such as ping, to verify that the OBM server is running and the IP address matches the value in the **Host IP** field.

8.  After a successful test, select the **Active** check box and then click **Update**.


**Parent Topic:**[Configure a pull connector](t_EMConfigureConnectorInstance.md)

