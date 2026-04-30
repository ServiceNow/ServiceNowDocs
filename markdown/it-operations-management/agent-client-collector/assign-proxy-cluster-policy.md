---
title: Assign a proxy agent cluster to a policy
description: Assign a proxy agent cluster to a policy when monitoring services external to the host server, such as URLs or external databases in the cloud. The agents in the cluster monitor all of the policy's CIs.
locale: en-US
release: xanadu
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Using proxy agents in Agent Client Collector, Agent Client Collector Monitoring, Agent Client Collector, IT Operations Management]
---

# Assign a proxy agent cluster to a policy

Assign a proxy agent cluster to a policy when monitoring services external to the host server, such as URLs or external databases in the cloud. The agents in the cluster monitor all of the policy's CIs.

## Before you begin

Ensure that you have a policy containing the checks that monitor external services. For details on these checks and policies, see [Agent Client Collector Monitoring default checks and policies](../reference/agent-policies-checks.md).

Role required: agent\_client\_collector\_admin

## About this task

Only one app should be run on a given proxy agent because running multiple apps is likely to cause performance degradation.

## Procedure

1.  Navigate to **All** &gt; **Agent Client Collector** &gt; **Agents** &gt; **Policies**.

2.  Select the policy containing the checks that you want to run on a proxy server.

3.  Select the **Proxy Settings** tab.

4.  Select **Edit in Sandbox** to enable modifying fields on the form.

5.  Indicate whether you are assigning a single proxy agent or a proxy agent cluster to monitor the policy CIs.

    -   Assign a single proxy agent by selecting **Single proxy agent** and selecting an agent.
    -   Enable a proxy agent cluster by selecting **Multi-proxy agents by cluster**. Provide the name of the cluster in the field that appears.
6.  Determine whether to select multiple proxy agents from the agents list through a filter or a script.

    -   To select agents through a filter, configure a filter or retain or modify an existing filter when the **Multi-proxy agents by filter** option is selected.

        **Note:**

        -   This field appears only when the **Hide Multi Proxy Agent by filter, if its not selected** property \(**sys\_ui\_policy**\) has been set to **active=false**.
        -   If you remove the filter in an existing policy, the option disappears.
    -   To select agents through a script:
        1.  Select **Edit in Sandbox**.
        2.  Clear any selected proxy options in the **Proxy Settings** tab.
        3.  Select **Multi-proxy agents by script**.
        4.  In the **Proxy script** field that appears, enter a script to assign services to different proxy agents as a form of load balancing.
7.  Determine whether to load-balance the selected multi-proxy agents that monitor the matching CIs in the policy's **Monitored CIs** tab or have each agent monitor the matching CIs.

    -   To load balance the selected multi-proxy agents that monitor the matching CIs, clear the **Run checks on all proxy agents \(No load balancing\)** option.

        For example, if you have five agents in a cluster or five agents using the filter/script option and 10 matching CIs in the policy, each agent would monitor two CIs.

        You can also enable load balancing at a later time, as described in [Enable load balancing between proxy agents in a cluster](view-proxy-ci-distribution.md).

    -   To have each agent monitor all matching CIs, select the **Run checks on all proxy agents \(No load balancing\)** option.

        If there are 10 matching CIs in the policy, each agent would monitor all 10. For example, you might want to use this option for multiple proxy servers in different geographic locations.

        If an agent is not functioning properly, the monitored CIs are redistributed to another agent.

    **Note:** For existing or active policies, the **Run checks on all proxy agents \(No load balancing\)** option is enabled by default. For new and inactive policies, this option is turned off by default.

8.  Select **Activate**.


