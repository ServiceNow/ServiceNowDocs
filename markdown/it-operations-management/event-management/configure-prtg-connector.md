---
title: Configure PRTG connector
description: Configure the PRTG connector instance to receive alerts from a Paessler PRTG Network Monitor source.
locale: en-US
release: yokohama
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Configure a pull connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Configure PRTG connector

Configure the PRTG connector instance to receive alerts from a Paessler PRTG Network Monitor source.

## Before you begin

Role required: evt\_mgmt\_admin

Supported version: 21.3.71.

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Integrations** &gt; **Connector Instances**.

2.  Click **New** and create a connector instance with the following details:

    |Field|Value|
    |-----|-----|
    |Name|Descriptive name for the PRTG connector.|
    |Description|Description for the use of the PRTG event collection instance.|
    |Host IP|Specify the PRTG IP address.|
    |Credential|Either select the required credentials from the list or click **New** and create the required credentials. If you create the credentials, save them using a unique and recognizable name, for example, `PRTGOPS`.|
    |Event collection last run time|The last run time value is automatically updated.|
    |Last event collection status|The last run time status is automatically updated.|
    |Event collection schedule \(seconds\)|The frequency in seconds that the system checks for new events from PRTG.|
    |Last error message|The last error message is automatically updated.|
    |Connector definition|Select **PRTG**.|
    |Connector Instance Values section|The parameters that are specific to **PRTG** display here when the form is saved.|
    |MID Servers \(MID Server for Connectors section\)|Optional. Name of a MID Server. If no MID Server is specified, an available MID Server that has a matching IP range is used. In the MID Servers for Connectors section, specify a MID Server that is up and valid. You can configure several MID Servers. If the first is down, the next MID Server is used. If that MID Server is not available, the next is selected, and so on. MID Servers are sorted according to the order that their details were entered into the MID Server for Connectors section.|

3.  Right-click the form header and select **Save**.

    The connector instance values are added to the form and the parameters that are relevant to the connector appear.

4.  In the Connector Instance Values section, specify the PRTG values.

    1.  **add\_columns**.

        Specify which columns to be returned by the connector. Separate the names with a comma and without a space between the names. The output is stored in the **Additional information** field of the event. Default value `false`. If `false` is specified, only the default list of columns is retrieved: parent, name, type, objid, tags, message, status, priority, datetime, actions, baselink, basetype, modifiedby.

        **Note:** Only columns names that are applicable to the **Message** content type can be specified.

    2.  **date\_format**.

        The format date and time. Default format M/d/yyyy/ h:mm:ss a. If you receive an event whose date is in a different format, modify this value to match the format of the incoming event. If you do not, the event will not be processed correctly.

        For example, if an event arrives on June 27, 2019 at 11:25 AM with a listed date of **2019/06/27/ 11:25:00 a**, modify the **date\_format** value to **yyyy/M/d/ h:mm:ss a** to match the format of the received event.

        In the **date\_format**, `a` represents AM, and `p` represents PM.

    3.  In the **days\_from** field, specify the number of days for which events must be collected at the first collection cycle.

        Default value `7` days.

    4.  **debug**.

        Default value `false`.

    5.  **port**.

        Default value `80`.

    6.  **protocol**.

        The default protocol type is `http`.

    7.  **prtg\_api\_fetched\_events\_num**.

        Maximum number of events, per query, that can be fetched from the PRTG client into the MID Server. Default number: `50,000`.

    8.  **time\_zone**.

        The default time zone is the `GMT` time zone; update this value to the PRTG time zone. For example, if PRTG is sending events according to the `EDT` time zone, update this value to `GMT-4` \(abbreviations such as EDT are not supported\).

5.  Right-click the form header and select **Save**.

6.  Click **Test Connector** to verify the connection between the MID Server and the connector.

7.  If the test fails, follow the instructions that the error issues to correct the problem and then run another test. 

    If this message appears: `Connection test failed: Failed to connect to PRTG on test connector. Invalid API Key`, then enter the API Key for the specific user to be able to read the PRTG events.

    **Note:** Use a network tool, such as ping, to verify credential correctness and network connectivity from the MID Server to PRTG.

8.  After a successful test, select the **Active** check box and then click **Update**.


**Parent Topic:**[Configure a pull connector](t_EMConfigureConnectorInstance.md)

