---
title: Automatic MID Server selection
description: Automatic selection of MID Servers ensures that each agent uses the most efficient available MID Server.
locale: en-US
release: yokohama
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Configuring Agent Client Collector with a MID Server, Configuring Agent Client Collector Framework, Agent Client Collector Framework, Agent Client Collector, IT Operations Management]
---

# Automatic MID Server selection

Automatic selection of MID Servers ensures that each agent uses the most efficient available MID Server.

The Agent Client Collector automatic MID Server selection feature set is disabled by default. There are several factors to consider before determining if automatic MID Server selection is right for your use cases.

## Use case considerations

Automatic MID Server selection provides several benefits. [MID Server capabilities](https://www.servicenow.com/docs/access?context=t_ConfigureCapabilities&version=yokohama&pubname=yokohama-servicenow-platform&section=r_MIDServerCapabilities&ft:locale=en-US) can narrow the list of MID Servers an agent can potential connect to. Automatic MID Server selection keeps the back-end URL configuration list up to date on the agent host without additional work flows.

When automatic MID Server selection is enabled, the agent performs a connectivity test against the list of available MID Servers and determines the best connection based on latency and number of currently connected agents.

However, there are several additional considerations that may make automatic MID Server selection wrong for your use case.

The ACC automatic MID Server selection is not a true load balancer and should be considered a fail-over mechanism. There is higher complexity for choosing a back-end URL as it is derived from multiple input sources. If, instead, an application load balancer is used only one back-end URL needs to be specified. See [Enable the Agent Client Collector load balancer](../task/acc-enable-load-balancer.md) for more information.

By default, each agent is sent the list of all MID Servers listening for ACC connections. Since that list includes MID Servers running in restricted areas, the agents can try to connect to them which can generate security alerts.

Your DNS configuration should be considered before using automatic MID Server selection because the resolution can lead to unexpected results. The DNS resolution is done periodically. End User Compute systems that alternate between internal corporate, Wi-Fi, VPN, or external networks may not be able to reconnect if the network context has changed.

## Automatic selection process

When automatic selection is enabled, the ServiceNow instance sends periodic MID Server updates to existing agents. The agent selects a MID Server based on information it receives from the ServiceNow instance.

During automatic MID Server selection, the agent selects a primary MID and a secondary MID list, and writes them to the agent’s config file. The agent uses this list for fail-over protection when the primary MID/secondary MID in the list loses connection.

When an agent detects that its IP address has changed, it automatically connects with the most efficient MID Server available from the agent's list of MID Servers.

To secure communication between the MID Server and the agent, use the MID Server's unified key store. For details on using the MID Server unified key store, see [MID Server unified key store](https://www.servicenow.com/docs/access?context=mid-unified-keystore&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

-   **[Enable automatic MID Server selection](../task/acc-disable-auto-mid-selection.md)**  
Enabling automatic MID Server selection lets the agent perform a connectivity test against the list of available MID Servers and determine the best connection based on latency and number of currently connected agents. Automatic MID Server selection is disabled by default.
-   **[Configure the Agent Client Collector capabilities for MID Servers](../task/configure-acc-capability.md)**  
Configure the MID Servers with Agent Client Collector capabilities to enable the MID Servers to work with agents. Agents that have identical MID Server capabilities are eligible for automatic MID Server selection.
-   **[Configure the automatic MID Server selection based on the Agent Client Collector capabilities](../task/configure-auto-mid-eligibility-by-capability.md)**  
Configure the MID Servers that are ineligible for automatic MID Server selection with the agent. For example, you may want to block a MID Server from connecting to your agent due to firewall constraints.

**Parent Topic:**[Configuring Agent Client Collector with a MID Server](acc-configuring-with-mid.md)

**Related topics**  


[Enable automatic MID Server selection](../task/acc-disable-auto-mid-selection.md)

