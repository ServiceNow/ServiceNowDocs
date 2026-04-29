---
title: Configure event collection from HP OMi
description: Configure the HP Operations Manager \(OMi\) connector instance to receive alerts from the HP OMi server.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure a pull connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Configure event collection from HP OMi

Configure the HP Operations Manager \(OMi\) connector instance to receive alerts from the HP OMi server.

## Before you begin

Supported versions: 10.01, 10.10, 10.11, 10.12, 10.60, and 10.61.

The OMi connector is not supported on versions below version 10.

Create Basic Auth type of credential to connect to OMI.

Role required: evt\_mgmt\_admin

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Integrations** &gt; **Connector Instances**.

2.  Click **New** and create a connector instance with the following details:

    |Field|Value|
    |-----|-----|
    |Name|Descriptive name for the OMi connector.|
    |Description|Description for the use of the OMi event collection instance.|
    |Host IP|Specify the OMi IP address.|
    |Credential|Click in the **Credential** field. Select a Basic Auth credential from the list or click the search icon. Either select the required credentials from the list or click **New** and create the required credentials using Basic Auth type. If you create the credentials, save them using a unique and recognizable name, for example OMiOPS.|
    |Event collection last run time|Last run time value. Automatically updated.|
    |Last event collection status|Last run time status. Automatically updated.|
    |Event collection schedule \(seconds\)|Frequency in seconds that the system checks for new events from OMi. The default value is 120 seconds.|
    |Last error message|Last error message. Automatically updated.|
    |Connector Definition|Select **OMi**.|
    |MID Servers \(MID Server for Connectors section\)|Optional. Name of a MID Server. If no MID Server is specified, an available MID Server that has a matching IP range is used. In the MID Servers for Connectors section, specify a MID Server that is up and valid. You can configure several MID Servers. If the first is down, the next MID Server is used. If that MID Server is not available, the next is selected, and so on. MID Servers are sorted according to the order that their details were entered into the MID Server for Connectors section.|

3.  Right-click the form header and select **Save**.

    The connector instance values are added to the form and the parameters that are relevant to the connector appear.

    ![OMi Connector Instance Values section](../image/omi-connector-value.png)

4.  In the Connector Instance Values section, specify the OMi values.

    1.  **days\_from**.

        Specify the number of days for which events must be collected on the first collection cycle. Default `7`.

    2.  **debug**.

        Default `false`. To enter debug mode, specify `true`.

    3.  **port**.

        Default `80`.

    4.  **protocol**.

        Default `http`.

    5.  **query\_filter**.

        Default value is false. If you do want to use this extra filter to query events, specify the event attributes. For example, `assigned_user = "admin" AND title = "My Title"`. The query filter criteria are:

        -   A filter property that specifies an event attribute, such as, `related_ci`
        -   A supported operator, for example, `OR` or `AND`
        -   A value for the filter property, for example, `admin` or `integrator`
        Everything from the query\_filter field undergoes URL encoding and is then passed as a parameter to the OMi API call. For detailed information on how to build the filter query, see “Filtering by Event Attributes: query” in the HP OMi Extensibility Guide. For example, to query the events for a list of events that are assigned to the admin user, specify:

        `event_list?query=assigned_ user%20EQ%20"admin"`

        To nest query\_filter event attributes, specify the hierarchy using square brackets "\[ \]".

    6.  **inclusion list**.

        Default value:`false`. Specify a comma-separated list to include this feature to add attributes that should be collected and added to the Event Management **Additional information** field.

5.  Right-click the form header and select **Save**.

6.  Click **Test Connector** to verify the connection between the MID Server and the connector.

7.  If the test fails, follow the instructions that the error issues to correct the problem and then run another test.

    **Note:** Use a network tool, such as ping, to verify credential correctness and network connectivity from the MID Server to the HP OMi server.

8.  After a successful test, select the **Active** check box and then click **Update**.


**Parent Topic:**[Configure a pull connector](t_EMConfigureConnectorInstance.md)

