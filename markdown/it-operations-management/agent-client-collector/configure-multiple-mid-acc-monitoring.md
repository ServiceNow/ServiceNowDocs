---
title: Configure multiple MID Servers to work with Agent Client Collector Monitoring
description: Connect agents to multiple MID Servers to enable Agent Client Collector Monitoring functionality. Multiple MID Servers can support each other with load balancing and domain separation.
locale: en-US
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure a MID Server to work with ACC-M, ACC deployment - servers, Agent Client Collector, IT Operations Management]
---

# Configure multiple MID Servers to work with Agent Client Collector Monitoring

Connect agents to multiple MID Servers to enable Agent Client Collector Monitoring functionality. Multiple MID Servers can support each other with load balancing and domain separation.

## Before you begin

Role required: agent\_client\_collector\_admin

## About this task

When configuring multiple MID Servers, use the same port for all MID Servers. Using different ports requires you to add each MID Server individually, as described in [Configure a MID Server to work with Agent Client Collector Monitoring](configure-mid-acc-monitoring.md).

## Procedure

1.  Navigate to **All** &gt; **Agent Client Collector** &gt; **MID Servers**.

2.  Select the check boxes corresponding to the MID Servers you want to connect to your agent.

3.  In the **Actions on selected rows...** window, select **Setup ACC Monitoring**.

    The option includes the number of MID Servers selected out of the number of available MID Servers. For example: **Setup ACC Monitoring \(7 of 8\)** indicates that 7 MID Servers were selected out of 8 available MID Servers.


## Result

A confirmation window appears, indicating that the selected MID Servers are connected to the agent.

