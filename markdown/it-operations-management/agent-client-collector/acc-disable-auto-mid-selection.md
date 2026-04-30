---
title: Enable automatic MID Server selection
description: Enabling automatic MID Server selection lets the agent perform a connectivity test against the list of available MID Servers and determine the best connection based on latency and number of currently connected agents. Automatic MID Server selection is disabled by default.
locale: en-US
release: yokohama
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Automatic MID Server selection, Configuring Agent Client Collector with a MID Server, Configuring Agent Client Collector Framework, Agent Client Collector Framework, Agent Client Collector, IT Operations Management]
---

# Enable automatic MID Server selection

Enabling automatic MID Server selection lets the agent perform a connectivity test against the list of available MID Servers and determine the best connection based on latency and number of currently connected agents. Automatic MID Server selection is disabled by default.

## Before you begin

Role required: agent\_client\_collector\_admin

## Procedure

-   To enable sending periodic MID Server updates from the ServiceNow instance to existing agents, set the **sn\_agent.enable\_auto\_mid\_selection** system property to **true**.

-   To enable automatic MID Server selection for individual agents:

    1.  Set the **enable-auto-mid-selection** property in the agent's `acc.yml` file to **true**.
    2.  Enable and execute the Update MID List for All Agents and Update MID List for All New Agents scheduled jobs.

## What to do next

To disable automatic MID Server selection again, set each of the properties back to **false**.

To schedule updates more often than once daily, or execute the job on demand, see [Configure the frequency of updating the agent MID Server list](acc-update-mid-server-list.md).

**Parent Topic:**[Automatic MID Server selection](../concept/acc-auto-mid-selection.md)

