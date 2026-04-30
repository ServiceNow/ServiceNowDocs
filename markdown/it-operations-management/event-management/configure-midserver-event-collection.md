---
title: Configure a MID Server for event collection using a push operation \(listener\)
description: The MID Server supports the collection of event messages, using the MID Web Server to collect data from external sources and transforming \(parsing\) them to the format required for event fields in the event \[em\_event\] table. The transformed events are then transmitted to the instance.
locale: en-US
release: zurich
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure a push connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Configure a MID Server for event collection using a push operation \(listener\)

The MID Server supports the collection of event messages, using the MID Web Server to collect data from external sources and transforming \(parsing\) them to the format required for event fields in the event \[em\_event\] table. The transformed events are then transmitted to the instance.

## Before you begin

Ensure that the Event Management Connectors \(sn\_em\_connector\) plugin is installed on the ServiceNow AI Platform instance.

Role required: evt\_mgmt\_admin

## About this task

The MID Web Server extension enables external clients to push metric data and events to the MID Server. See [Configure the MID Web Server extension](configure-mid-web-server-extension.md). Use the MID WebService Event Collector to enable a URL method to push event messages to the MID Server. See [Configure the MID WebService Event Collector Context](configure-em-context-extension.md).

Configure a MID Server with either **EventManagement** or **All** in the Supported Applications List.

To ensure uninterrupted services, consider also configuring a failover MID Server cluster.

## Procedure

1.  Navigate to **All** &gt; **MID Server** &gt; **Servers**.

2.  Double-click the MID Server that you want to configure, or click **New** to create a new MID Server.

3.  In the **Supported Applications** section, click **Edit**.

    1.  Click **Edit**.

    2.  In the slushbucket, either select **Event Management** or **ALL** and click the **&gt;** add button.

    3.  Click **Save**.

4.  To ensure that the MID Server is validated, under Related Links, select **Validate**.

    For more information, see [Validate a MID Server](https://www.servicenow.com/docs/access?context=t_ValidateAMIDServer&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

5.  Click **Update**.


## What to do next

Configure the MID WebService Event Collector to enable a URL method to push event messages to the MID Server. For more information, see [Configure the MID WebService Event Collector Context](configure-em-context-extension.md).

**Related topics**  


[Configure key-based MID Web Server authentication](configure-mid-web-server-extension-metric-data.md)

[Configure the MID Web Server extension](configure-mid-web-server-extension.md)

[Configure the MID WebService Event Collector Context](configure-em-context-extension.md)

