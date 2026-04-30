---
title: Configure the automatic MID Server selection based on the Agent Client Collector capabilities
description: Configure the MID Servers that are ineligible for automatic MID Server selection with the agent. For example, you may want to block a MID Server from connecting to your agent due to firewall constraints.
locale: en-US
release: xanadu
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Automatic MID Server selection, Configuring Agent Client Collector with a MID Server, Configuring Agent Client Collector Framework, Agent Client Collector Framework, Agent Client Collector, IT Operations Management]
---

# Configure the automatic MID Server selection based on the Agent Client Collector capabilities

Configure the MID Servers that are ineligible for automatic MID Server selection with the agent. For example, you may want to block a MID Server from connecting to your agent due to firewall constraints.

## Before you begin

Role required: agent\_client\_collector\_admin

## About this task

Agents with different levels of Agent Client Collector \(ACC\) capability can’t be considered for automatic MID Server selection. If you want to block a MID Server from automatic MID Server selection, you can assign the MID Server different ACC capabilities from all MID Servers, but not the primary MID Server, in your environment.

## Procedure

1.  Configure the Agent Client Collector capabilities for MID Servers, as described in [Configure the Agent Client Collector capabilities for MID Servers](configure-acc-capability.md).

2.  Navigate to **All** &gt; **Agent Client Collector** &gt; **MID Servers**.

3.  Select the MID Server that you want to be ineligible for automatic MID Server selection.

4.  Select the additional actions icon ![Additional Actions icon.](../image/additional-actions-icon.png) and select **View** &gt; **Default View**.

5.  Select the **Capabilities** tab.

6.  Ensure that the MID Server isn’t assigned with the capabilities that have **Is ACC Capability=true** on the **Capabilities** tab.


## Configuring MID Servers to be ineligible for automatic MID Server selection

1.  Assign the **AgentClientCollector** capability to MID Server A and MID Server C, but not to MID Server B.
2.  On the MID Server Capabilities page:
    1.  Assign a capability to MID Server A and MID Server C.
    2.  Assign a different capability to MID Server B.
3.  Install Agent Client Collector Framework and specify MID Server A as the MID Server during installation.

    After installation, the agent has **Status=Up** and its MID Server is MID Server A.

4.  Execute the MID Server Selection scheduled job to determine which MID Servers are eligible for automatic MID Server selection.

    MID Server B is ineligible for automatic selection, because it doesn’t have the same ACC capability as MID Server A. MID Server C is eligible, because it has the same ACC capability as MID Server A.


