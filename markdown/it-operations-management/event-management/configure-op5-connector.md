---
title: Configure OP5 or OP5\_v2 connector
description: Configure the OP5 or OP5\_v2 Monitor connector instance to receive alerts from an OP5 Monitor source.
locale: en-US
release: zurich
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure a pull connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Configure OP5 or OP5\_v2 connector

Configure the OP5 or OP5\_v2 Monitor connector instance to receive alerts from an OP5 Monitor source.

## Before you begin

The OP5\_v2 connector is supported in Event Management connectors version 2.3.0 - August 2022, available from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

Supported version:

-   OP5: 7.3.15
-   OP5\_v2: 8.3.8

Role required: evt\_mgmt\_admin

## About this task

Starting from the Xanadu release, the OOTB \(Out-Of-The-Box\) event rules provided with the connector, which you have not previously used \(i.e., neither activated, deactivated, nor modified\), will now have the **Apply additional matching rules** check box set to true. Previously, this check box was disabled. This change allows you to execute more event rules or automation using the same filter conditions for the events.

**Note:** This feature applies only to active event rules.

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Integrations** &gt; **Connector Instances**.

2.  Click **New** and create a connector instance with the following details:

    |Field|Value|
    |-----|-----|
    |Name|Descriptive name for the OP5 or OP5\_v2 connector.|
    |Description|Description for the use of the OP5 or OP5\_v2 event collection instance.|
    |Host IP|Specify the OP5 or OP5\_v2 IP address.|
    |Credential|Either select the required credentials from the list or click **New** and create the required credentials. If you create the credentials, save them using a unique and recognizable name, for example, OP5OPS.|
    |Event collection last run time|The last run time value is automatically updated.|
    |Last event collection status|The last run time status is automatically updated.|
    |Event collection schedule \(seconds\)|The frequency in seconds that the system checks for new events from OP5 or OP5\_v2.|
    |Last error message|The last error message is automatically updated.|
    |Connector definition|Select **OP5** or **OP5\_v2**.|
    |Connector Instance Values section|The parameters that are specific to **OP5** or **OP5\_v2** display here when the form is saved.|
    |MID Servers \(MID Server for Connectors section\)|Optional. Name of a MID Server. If no MID Server is specified, an available MID Server that has a matching IP range is used. In the MID Servers for Connectors section, specify a MID Server that is up and valid. You can configure several MID Servers. If the first is down, the next MID Server is used. If that MID Server is not available, the next is selected, and so on. MID Servers are sorted according to the order that their details were entered into the MID Server for Connectors section.|

3.  Right-click the form header and select **Save**.

    The connector instance values are added to the form and the parameters that are relevant to the connector appear.

4.  In the Connector Instance Values section, specify the OP5 or OP5\_v2 values.

    1.  **days\_from**.

        Specify the number of days for which events must be collected at the first collection cycle. Default value `7` days.

    2.  **debug**.

        Displays debug messages. Default value: false. Specify true to see debug messages

    3.  **logPayloadForDebug**.

        Displays payload related debug messages. Default value: false. Specify true to see payload related debug messages.

    4.  **port**.

        Default value `443`.

    5.  **state\_types**.

        Specify filters for event collection based on the **state\_types** attribute. You can filter events based on state type. Specify the type, for example, `soft` or `hard`.

5.  Right-click the form header and select **Save**.

6.  Click **Test Connector** to verify the connection between the MID Server and the connector.

7.  If the test fails, follow the instructions that the error issues to correct the problem and then run another test.

8.  After a successful test, select the **Active** check box and then click **Update**.


**Parent Topic:**[Configure a pull connector](t_EMConfigureConnectorInstance.md)

