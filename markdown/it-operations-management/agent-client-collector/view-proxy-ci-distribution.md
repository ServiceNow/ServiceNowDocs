---
title: Enable load balancing between proxy agents in a cluster
description: Enable load balancing between proxy agents in a cluster so that if an agent is not functioning properly, monitored CIs are redistributed to another agent. After enabling load balancing, you can view the CIs monitored by each proxy agent in a policy.
locale: en-US
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Assign a proxy agent cluster to a policy, Using proxy agents in ACC, ACC deployment - servers, Configuring Agent Client Collector, Agent Client Collector, IT Operations Management]
---

# Enable load balancing between proxy agents in a cluster

Enable load balancing between proxy agents in a cluster so that if an agent is not functioning properly, monitored CIs are redistributed to another agent. After enabling load balancing, you can view the CIs monitored by each proxy agent in a policy.

## Before you begin

Ensure that you have upgraded to Tokyo patch 1 or San Diego patch 7.

Role required: agent\_client\_collector\_user

## Procedure

1.  Navigate to **All** &gt; **Agent Client Collector** &gt; **Configuration** &gt; **Policies**.

2.  Select the policy containing the CIs you want the proxy agents to monitor.

3.  Select the **Proxy Settings** tab.

4.  Enable load balancing for the proxy agents by clearing the **Run checks on all proxy agents \(No load balancing\)** check box.

    Load balancing is enabled for the proxy agents monitoring the CIs. For example, if you have five agents and 10 matching CIs in the policy, each agent monitors two CIs.

5.  In the **Related Links** section, select **Show distribution of proxy agent’s CIs**.

    A pop-up window displays the distribution of monitored CIs among agents within the policy.


**Parent Topic:**[Assign a proxy agent cluster to a policy](assign-proxy-cluster-policy.md)

