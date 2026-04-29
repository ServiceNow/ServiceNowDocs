---
title: Use the SAP Solution Manager Push connector
description: The MID Server web service Event Collector enables you to collect alerts sent from the SAP Solution Manager through event stream notification capabilities. The interface runs both a Push and a Pull interface to interact directly with the SAP Solution Manager.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Enable SAP connector configurations, Configure SAP Solution Manager connector, Configure a pull connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Use the SAP Solution Manager Push connector

The MID Server web service Event Collector enables you to collect alerts sent from the SAP Solution Manager through event stream notification capabilities. The interface runs both a Push and a Pull interface to interact directly with the SAP Solution Manager.

## Before you begin

-   Deploy and start the MID Server.
-   Configure and start the MID Web Server.
-   Configure and start the MID Server web service Event Collector.

Role required: evt\_mgmt\_admin

## About this task

SAP Solution Manager sends JSON formatted event messages to the MID Server. The MID Server parses the collected alert messages and transforms them using the SAP Solman Transform \[**TransformEvents\_SAPSolman**\] script.

JSON formatted messages are collected using basic authentication. For details on other supported authentication methods, see [Configure the MID Web Server extension](configure-mid-web-server-extension.md).

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Integrations** &gt; **Push connectors**.

2.  Select the **SAP Solman Transform Script** script.

3.  Use the following URL to push alert messages from SAP Solution Manager to the MID Server:

    `http://<MID_Server_IP>:<MID_Web_Server_Port>/api/mid/em/inbound_event?Transform=TransformEvents_SAPSolman`, where the following are true:

    -   **MID\_Server\_IP** is the IP address of the MID Web Server extension
    -   **MID\_Web\_Server\_Port** is the listening port of the MID Web Server extension

## What to do next

Create an Remote Function Call \(RFC\) in the SAP Solution Manager and install a transport, as described in [Configure RFC in SAP Solution Manager](configure-sap-solution-mgr.md).

**Parent Topic:**[SAP configurations enabling the SAP Solution Manager connector](../concept/sap-manager-connector.md)

**Related topics**  


[Configuring MID Servers](https://www.servicenow.com/docs/access?context=c_MIDServerConfiguration&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)

[Configure the MID Web Server extension](configure-mid-web-server-extension.md)

[Configure the MID WebService Event Collector Context](configure-em-context-extension.md)

