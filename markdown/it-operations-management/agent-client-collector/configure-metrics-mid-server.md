---
title: Manually configure a MID Server for Metric Intelligence
description: To use Metric Intelligence, configure at least one MID Server with Metric Intelligence as a supported application, with the Metrics capability, and which runs the Metric Intelligence Metrics extension. Then, add that Metric Intelligence MID Server as a member to a MID Server distributed cluster.
locale: en-US
release: xanadu
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Get started with Metric Intelligence, Activating Metric Intelligence, Metric Intelligence, Agent Client Collector Monitoring, Agent Client Collector, IT Operations Management]
---

# Manually configure a MID Server for Metric Intelligence

To use Metric Intelligence, configure at least one MID Server with Metric Intelligence as a supported application, with the Metrics capability, and which runs the Metric Intelligence Metrics extension. Then, add that Metric Intelligence MID Server as a member to a MID Server distributed cluster.

## Before you begin

Ensure that the MID Server meets all software, hardware, and configuration requirements to be configured for Metric Intelligence.

Role required: To access the MID Server - mid\_server. To configure a MID Server in an instance \(for example, to add a supported application\), refer to the MID Server documentation.

## Procedure

1.  Navigate to **All** &gt; **MID Server** &gt; **Servers**.

2.  Click the MID Server that you want to configure for Metric Intelligence.

3.  Add the Metric Intelligence application:

    1.  At the center of the MID Server form, click **Supported Applications**.

    2.  In the **Supported Applications** section, click **Edit**.

    3.  In the slushbucket, select **OperationalIntelligence** and click the **&gt;** add button.

    4.  Click **Save**.

4.  Add the Metrics capability:

    1.  At the center of the MID Server form, click **Capabilities**.

    2.  In the **Capabilities** section, click **Edit**.

    3.  In the slushbucket, select **Metrics** and click the '&gt;' add button.

    4.  Click **Save**.

5.  Click **Update**.


## What to do next

Create a MID Server distributed cluster, and add the Metric Intelligence MID Server as a member to that cluster.

