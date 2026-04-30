---
title: Monitor HTTP points
description: Use the Monitoring HTTP Entry Points and Monitoring HTTP Entry Points Metrics policies that come with the ITOM Monitoring scoped app to monitor http and https entry points and entry points metrics. You can customize these policies as needed, or you can configure a new policy to monitor service entry points.
locale: en-US
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Operating system and application monitoring using ACC, Exploring ACC Framework, Agent Client Collector, IT Operations Management]
---

# Monitor HTTP points

Use the **Monitoring HTTP Entry Points** and **Monitoring HTTP Entry Points Metrics** policies that come with the ITOM Monitoring scoped app to monitor `http` and `https` entry points and entry points metrics. You can customize these policies as needed, or you can configure a new policy to monitor service entry points.

## Before you begin

Role required: agent\_client\_collector\_admin

## About this task

An entry point is the access point for a service. In an Agent Client Collector policy, you specify the service you want to monitor, and the policy monitors the service's entry points.

## Procedure

1.  Navigate to **All** &gt; **Agent Client Collector** &gt; **Policies**.

2.  Select either the **Monitoring HTTP Entry Points** or **Monitoring HTTP Entry Points Metrics** policy.

    The relevant **Policy - Monitoring HTTP Entry Points** page opens.

3.  On the **Monitored CIs** tab:

    1.  In the **Table** field, ensure that the **sn\_itmon\_http\_entrypoint** database view table is selected for the Agent Client Collector to retrieve http and https entry points for monitoring.

    2.  In the **Filter** section, configure a filter for the services and entry points to be taken from the **sn\_itmon\_http\_entrypoint** database view table.

4.  Click the **Proxy Settings** tab and select the type of proxy you want to enable for the entry point monitoring.

    -   **Single proxy agent**: Select to enable monitoring a single agent, which you select in the **Proxy agent** field that appears after selecting this option.
    -   **Multi-proxy agents by filter**: Select to enable monitoring multiple agents. Configure a filter in the **Proxy filter** section that appears after selecting this option to monitor only the agents that match the filter's conditions.
    -   **Script based proxy**: Select to enable monitoring an agent based on a script.
    You must configure a proxy to run an HTTP policy.

5.  Click the **Checks** tab and in the **Filter checks by groups** field, select **HTTP** to display all of the http checks in the **Available** cell.

6.  Select the relevant checks and click the right arrow button to move them to the **Selected** cell.

7.  Select the **Active** check box at the top of the page to activate the policy.

8.  Click **Update**.

    The policy monitors the entry points specified by the policy's configurations.


**Parent Topic:**[Operating system and application monitoring using Agent Client Collector](../concept/itom-monitoring-for-acc.md)

