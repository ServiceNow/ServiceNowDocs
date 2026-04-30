---
title: Automated Metric Intelligence setup
description: When you initially set up Metric Intelligence, you can automate many of the setup steps. For example, the automated setup configures a MID Server for Metric Intelligence and creates a MID Server distributed cluster which contains that MID Server.
locale: en-US
release: xanadu
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Get started with Metric Intelligence, Activating Metric Intelligence, Metric Intelligence, Agent Client Collector Monitoring, Agent Client Collector, IT Operations Management]
---

# Automated Metric Intelligence setup

When you initially set up Metric Intelligence, you can automate many of the setup steps. For example, the automated setup configures a MID Server for Metric Intelligence and creates a MID Server distributed cluster which contains that MID Server.

## Before you begin

Role required: evt\_mgmt\_admin

## About this task

When the following conditions are met, the related link **Setup Metric Intelligence** appears on the MID Server form, enabling automated setup:

-   The MID Server has been validated.
-   The MID Server is in a running state.
-   The property **sa.metric.display.mid.setup.action** is set to true \(default value\).

The Metric Intelligence automated setup performs the following setup tasks:

1.  Configures the MID Server with the **Operation Intelligence** application
2.  Adds the **Metrics** capability to the MID Server
3.  Creates a new MID Server cluster of type ‘distributed’ set with a default port of 47100 for Apache Ignite
4.  Adds the MID Server to the new MID Server distributed cluster
5.  Creates a Metric Intelligence Metrics Extension and starts it
6.  Opens the Metric Intelligence Metrics Context form. On this form, you can click the **Setup REST Listener** UI action to create the MID Web Server extension configured with the ‘Enable REST Listener’ option and default port 8097

If automatic setup fails, you can create a MID Server distributed cluster manually, as described in the Use the **Setup Metric Intelligence** link only to create the first MID Server distributed cluster that contains a single MID Server, with default values. After the automated setup completes, you have to manually create any additional MID Server distributed clusters or add Metric Intelligence MID Servers.

## Procedure

1.  Navigate to **All** &gt; **MID Server** &gt; **Servers**.

2.  Select the MID Server that you want to configure as a Metric Intelligence MID Server.

3.  On the MID Server form, select **Setup Metric Intelligence** in the Related Links section.

4.  In the newly created Metric Intelligence Metrics Extension form:

    1.  Wait for the Status value to be **Started**.

    2.  If configuring the MID Server for pushing, select the UI action **Setup REST Listener**.

    A notification appears about the MID Server extension being created. The **MID Web Server Extension** field appears and **Enable REST Listener** is checked. You can preview the MID Server Extension record to verify that its Status value is **Started**.


**Related topics**  


[MID Server and MID Server distributed cluster for Metric Intelligence](../concept/ops-intelligence-mid-server.md)

