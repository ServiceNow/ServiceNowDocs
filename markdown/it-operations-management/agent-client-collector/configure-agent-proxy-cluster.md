---
title: Create a proxy agent cluster
description: Create a cluster of agents on multiple proxy servers to monitor services external to the host server. Creating a cluster of agents enables you to assign that cluster to multiple policies instead of having to assign the agents individually to every policy.
locale: en-US
release: yokohama
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Using proxy agents in Agent Client Collector, Agent Client Collector Monitoring, Agent Client Collector, IT Operations Management]
---

# Create a proxy agent cluster

Create a cluster of agents on multiple proxy servers to monitor services external to the host server. Creating a cluster of agents enables you to assign that cluster to multiple policies instead of having to assign the agents individually to every policy.

## Before you begin

Role required: agent\_client\_collector\_admin

## About this task

A proxy agent cluster monitors the CIs that match the filter specified on the policy's **Monitored CIs** tab.

A proxy agent cluster must contain at least one agent. All of the cluster's agents monitor the CIs specified in its assigned policy. No special configuration is necessary on the policy level to enable proxy cluster monitoring.

The default CPU threshold value when working with proxy agent clusters is 80%. You can modify this value in the **proxy\_cpu\_percentage\_limit** property.

## Procedure

1.  Navigate to **All** &gt; **Agent Client Collector** &gt; **Configuration** &gt; **Proxy Agent Cluster**.

2.  Select **New**.

3.  In the **Name** field, enter a descriptive name for the cluster.

4.  Add an agent to the cluster.

    1.  In the **Agents in cluster** section, locate the **Agent** column and select **Insert a new row**.

    2.  Select the search icon \(![search icon](../../event-management/image/search-icon.png)\) and select an agent to add to the cluster.

    3.  Select the check icon \(![check icon](../image/check-icon.png)\) to add the agent to the cluster.

    Repeat this step for each agent that you want to add to the cluster.

5.  Select **Submit**.


## Result

The **Proxy Agent Clusters** page appears and displays the agent added to the cluster.

## What to do next

Select this proxy cluster to monitor CIs specified in an agent policy. For details, see [Configure an agent on a proxy server](configure-agent-proxy-server.md).

