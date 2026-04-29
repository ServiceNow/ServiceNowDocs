---
title: Configure an agent on a proxy server
description: Configure an Agent Client Collector on a proxy server when monitoring services external to the host server, such as URLs or external databases in the cloud.
locale: en-US
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using proxy agents in ACC, ACC deployment - servers, Configuring Agent Client Collector, Agent Client Collector, IT Operations Management]
---

# Configure an agent on a proxy server

Configure an Agent Client Collector on a proxy server when monitoring services external to the host server, such as URLs or external databases in the cloud.

## Before you begin

Role required: agent\_client\_collector\_admin

## About this task

Proxy agents should be dedicated agents, as running other apps on a proxy agent is likely to cause performance degradation.

## Procedure

1.  Navigate to **All** &gt; **Agent Client Collector** &gt; **Agents** &gt; **Policies**.

2.  Select the policy containing the checks that you want to run on a proxy server.

    You must configure a proxy server for checks and policies that monitor external services. For details on these checks and policies, see [Agent Client Collector Monitoring default checks and policies](../reference/agent-policies-checks.md).

3.  Select the **Proxy Settings** tab.

4.  Select from the following fields.

<table id="table_pz5_j1c_1kb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Single proxy agent

</td><td>

Select to display the **Proxy agent** field, where you select a single proxy agent.

</td></tr><tr><td>

Multi-proxy agents by cluster

</td><td>

Select to enable a group of proxy agents to monitor the policy CIs. When selecting this check box, the **Agent cluster name** field appears.

</td></tr><tr><td>

Agent cluster name

</td><td>

Select an agent cluster to monitor the policy CIs.

</td></tr><tr><td>

Multi-proxy agents by filter

</td><td>

Select to filter multiple proxy agents from the agent list.When selecting this option, all proxy agents monitor the same services. For example, you may want to use this option for multiple proxy servers in different geographic locations.

 **Note:**

-   This field appears only when the **Hide Multi Proxy Agent by filter, if its not selected** property \(**sys\_ui\_policy**\) is set to **active=false**.
-   This field appears only for existing policies where this option was previously selected. If you remove the filter in an existing policy, the option disappears.


</td></tr><tr><td>

Multi-proxy agents by script

</td><td>

Select to configure a JavaScript for selecting proxy agents.When selecting this option, you can assign services to different proxy agents, which can serve as a form of load balancing.

</td></tr><tr><td>

Run checks on all proxy agents \(No load balancing\)

</td><td>

Clear this option to load balance the selected multi proxy agents that monitor the matching CIs in the policy's **Monitored CIs** tab. Select this option for each agent to monitor all matching CIs in the policy's **Monitored CIs** tab.For example, if you have five agents in a cluster or five agents using the filter/script option and 10 matching CIs in the policy, when you clear this option, each agent monitors two CIs. When selecting this option, each agent monitors all 10 of the matching CIs in the policy.

 For existing or active policies, this option is enabled by default. For new and inactive policies, this option is turned off by default.

 Select this option only in a case where you have an external endpoint for which you want to measure how quickly it is accessed from different locations.

</td></tr></tbody>
</table>5.  Select **Activate**.


**Parent Topic:**[Using proxy agents in Agent Client Collector](../concept/proxy-agent.md)

