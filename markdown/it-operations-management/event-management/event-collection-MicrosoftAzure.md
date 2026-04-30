---
title: Event collection from Microsoft Azure Monitor
description: The MID WebServer Event Collector enables you to collect JSON formatted event messages sent from the Microsoft Azure portal.
locale: en-US
release: zurich
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Integrate with push connectors, Configure a push connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Event collection from Microsoft Azure Monitor

The MID WebServer Event Collector enables you to collect JSON formatted event messages sent from the Microsoft Azure portal.

## Before you begin

Ensure that the Event Management Connectors \(sn\_em\_connector\) plugin is installed on the ServiceNow AI Platform instance.

Ensure that you:

-   Deploy and start the MID Server. See [MID Server configuration](https://www.servicenow.com/docs/access?context=c_MIDServerConfiguration&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US) .
-   Configure and start the MID Web Server. See [Configure the MID Web Server extension](configure-mid-web-server-extension.md).
-   Configure and start the MID WebService Event Collector. See [Configure the MID WebService Event Collector Context](configure-em-context-extension.md).

Role required: evt\_mgmt\_admin

## About this task

On the Azure portal, alert correlation rules are defined through the **Correlate alerts** setting within Alert Processing Rules. When **Correlate alerts** is assigned on the Azure portal, the Azure Monitor alerts received on the ServiceNow® instance within 60 minutes are grouped using tag based alert clustering.

JSON formatted event messages are sent from Microsoft Azure. The MID Server transforms the collected event messages by parsing them using the TransformEvents\_MidAzureMonitor script include, located here: **Event Management** &gt; **Integrations** &gt; **PushConnectors**. In the Push Connectors page, click **Azure Monitor Mid Push Connector**.

The default format of the URL to push event messages from Microsoft Azure to the MID Server is `http://<MID_Web_Server_User>:<MID_Web_Server_Password>@<MID_Server_IP>:<MID_Web_Server_Port>/api/mid/em/inbound_event?Transform=TransformEvents_MidAzureMonitor`.

|Variable|Description|
|--------|-----------|
|MID\_Server\_IP|IP address of the MID Web Server Extension.|
|MID\_Web\_Server\_Port|Listening port of the MID Web Server Extension.|
|MID\_Web\_Server\_User|Username for the MID Web Server Extension.|
|MID\_Web\_Server\_Password|Password of the user of the MID Web Server.|

The following procedure describes the collection of JSON formatted event messages using basic authentication.

## Procedure

1.  In the Azure Monitor Portal, make sure the MID Server IP is accessible from the Azure portal and the MID rest point is accessible from Microsoft Azure or install the MID Server on a Azure VM and provide the Azure VM public address in the URL and allow the mid\_web\_Server\_port in **Azure VM** &gt; **Networking Settings** &gt; **Inbound port rules**.

2.  Create an action group with a webhook and provide the rest endpoint as `http://<MID_Web_Server_User>:<MID_Web_Server_Password>@<MID_Server_IP>:<MID_Web_Server_Port>/api/mid/em/inbound_event?Transform=TransformEvents_MidAzureMonitor`

    **Note:** For more information about adding a webhook to an action group, see [Create and manage action groups in the Azure portal](https://docs.microsoft.com/en-us/azure/azure-monitor/alerts/action-groups) on the Microsoft documentation site.

3.  In the Webhook section, make sure **Yes** is selected for the **Enable the common alert schema** option.

4.  Navigate to **Alerts** &gt; **Manage Alert Rules**.

5.  Add the action group with the webhook to an alert rule.


## What to do next

If you want to send alert state changes on the ServiceNow instance from the ServiceNow alerts to the Azure Portal, you need to enable the Azure Monitor Bi-directional connector. For more information, see [Configure Azure Monitor Bi-directional connector](configure-azure-bi-directional-connector.md).

**Parent Topic:**[Integrate with push connectors](configure-listener-transform-script.md)

