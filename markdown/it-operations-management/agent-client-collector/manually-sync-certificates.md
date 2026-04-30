---
title: Manually refresh Agent Client Collector certificates
description: Refresh Agent Client Collector self-signed certificates manually to validate Agent Client Collector plugins, instead of waiting for the scheduled synchronization. For example, you can use this feature when the agent can't validate a plugin and you don't want to wait for the scheduled synchronization.
locale: en-US
release: xanadu
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring Agent Client Collector Framework, Agent Client Collector Framework, Agent Client Collector, IT Operations Management]
---

# Manually refresh Agent Client Collector certificates

Refresh Agent Client Collector self-signed certificates manually to validate Agent Client Collector plugins, instead of waiting for the scheduled synchronization. For example, you can use this feature when the agent can't validate a plugin and you don't want to wait for the scheduled synchronization.

## Before you begin

Role required: agent\_client\_collector\_admin

## Procedure

1.  Navigate to **All** &gt; **Agent Client Collector** &gt; **MID Servers**.

2.  Select a MID Server.

3.  In the Related Links section, select **Trigger ACC certificate sync**.


## Result

Self-signed certificates are sent from the MID Server to the Agent Client Collector to validate the agent's plugins.

