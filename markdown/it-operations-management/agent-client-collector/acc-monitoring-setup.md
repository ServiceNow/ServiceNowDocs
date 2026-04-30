---
title: Enable Agent Client Collector monitoring on the MID Server
description: Enable Agent Client Collector monitoring on the MID Server by configuring the Agent Client Collector framework \(ACC-F\) and Metric Intelligence extensions in a single action. Enabling Agent Client Collector monitoring also enables monitoring on agents connected to the MID Server.
locale: en-US
release: yokohama
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring Agent Client Collector with a MID Server, Configuring Agent Client Collector Framework, Agent Client Collector Framework, Agent Client Collector, IT Operations Management]
---

# Enable Agent Client Collector monitoring on the MID Server

Enable Agent Client Collector monitoring on the MID Server by configuring the Agent Client Collector framework \(ACC-F\) and Metric Intelligence extensions in a single action. Enabling Agent Client Collector monitoring also enables monitoring on agents connected to the MID Server.

## Before you begin

Role required: evt\_mgmt\_admin

## Procedure

1.  Navigate to **All** &gt; **Agent Client Collector** &gt; **MID Servers**.

2.  On the MID Server page, select a MID Server to view the MID Server's details.

3.  In the **Related Links** section, select **Setup ACC Monitoring** and enter the relevant port number in the **MID Web Server Port** field of the dialog box.


## Result

The MID Server is configured to support both the Agent Client Collector and Metric Intelligence.

**Note:** You are prompted to enter a port number only on initial ACC Monitoring setup.

**Parent Topic:**[Configuring Agent Client Collector with a MID Server](../concept/acc-configuring-with-mid.md)

