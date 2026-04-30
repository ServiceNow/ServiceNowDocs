---
title: Configure event collection from vCenter
description: Configure the VMware vCenter Server \(vCenter or vCenter\_V2\) connector instance to receive events from your VMware vSphere environment.
locale: en-US
release: yokohama
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Configure a pull connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Configure event collection from vCenter

Configure the VMware vCenter Server \(vCenter or vCenter\_V2\) connector instance to receive events from your VMware vSphere environment.

## Before you begin

Events collected by this connector are events that match the vCenter ESX Servers event rule.

Supported version: 7.0.2.00500.

Role required: evt\_mgmt\_admin

## About this task

Starting from the Xanadu release, the OOTB \(Out-Of-The-Box\) event rules provided with the connector, which you have not previously used \(i.e., neither activated, deactivated, nor modified\), will now have the **Apply additional matching rules** check box set to true. Previously, this check box was disabled. This change allows you to execute more event rules or automation using the same filter conditions for the events.

**Note:** This feature applies only to active event rules.

This connector has the **debug** and **logPayloadForDebug** log parameters enabled. The **debug** parameter logs debug messages, such as calls made to the source system to retrieve events. The **logPayloadForDebug** parameter logs event and metric payloads from the source system. Once debugging is complete, set this parameter to **false** to prevent overloading the system.

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Integrations** &gt; **Connector Instances**.

2.  Click **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Descriptive and unique name for the vCenter connector.|
    |Description|Description for the use of the vCenter event collection instance.|
    |Connector definition|Name of the required connector definition. Select **vCenter** or **vCenter\_V2** \(vCenter\_V2 is located in the Event Management connectors scope\).|
    |Host IP|IP address where vCenter is installed.|
    |Credential|Permission to connect to vCenter. Click the search icon in the **Credential** field. Either select the required credentials from the list or click **New** and create the required credentials on the Credentials form. If you create the credentials, save them using a unique and recognizable name, for example, vCenterCHCK.|
    |Event collection last run time|Last run time value. Automatically updated.|
    |Last event collection status|Last run status. Automatically updated.|
    |Event collection schedule \(seconds\)|Frequency, in seconds, that the system checks for new events from vCenter. The default value is 120 seconds.|
    |Last error message|Last error message. Automatically updated.|

4.  Right-click the form header and select **Save**.

    The connector instance values are added to the form and the parameters that are relevant to the connector appear.![vCenter Connector Instance Values](../image/vcenter-connector-values.png)

5.  In the Connector Instance Values section, specify the vCenter values.

    |Field|Value|
    |-----|-----|
    |collect\_stateless\_events|Events that have a status \(stateful\) are collected when this field is set to `false` \(default\). These events are of type AlarmStatusChangedEvent and AlarmClearedEvent. If this field is set to `true`, events of other types are collected as well.|
    |port|Specify the value of the port. Default value: `443`.|
    |protocol|Specify the protocol. Default value: `https`.|

6.  In the MID Servers for Connectors section, specify a MID Server that is up and is valid.

    If no MID Server is specified, an available MID Server that has a matching IP range is used.

    You can configure several MID Servers. If the first is down, the next MID Server is used. If that MID Server is not available, the next is selected, and so on. MID Servers are sorted according to the order that their details were entered into the MID Server for Connectors section.

7.  Right-click the form header and select **Save**.

8.  Test the connection between the MID Server and the vCenter connector.

    1.  Click **Test Connector**.

        If the test fails, follow the instructions that the error issues to correct the problem and then run another test.

        **Note:** Use a network tool, such as ping, to verify credential correctness and network connectivity from the MID Server to the external monitoring tool.

    2.  After a successful test, select the **Active** check box.

9.  Click **Update**.


**Parent Topic:**[Configure a pull connector](t_EMConfigureConnectorInstance.md)

