---
title: Configure the Agent Client Collector capabilities for MID Servers
description: Configure the MID Servers with Agent Client Collector capabilities to enable the MID Servers to work with agents. Agents that have identical MID Server capabilities are eligible for automatic MID Server selection.
locale: en-US
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Automatic MID Server selection, Configuring ACC with a MID Server, ACC deployment - servers, Configuring Agent Client Collector, Agent Client Collector, IT Operations Management]
---

# Configure the Agent Client Collector capabilities for MID Servers

Configure the MID Servers with Agent Client Collector capabilities to enable the MID Servers to work with agents. Agents that have identical MID Server capabilities are eligible for automatic MID Server selection.

## Before you begin

Role required: agent\_client\_collector\_admin

## About this task

A capability defines MID Server functions. Any MID Server that is assigned with a capability that has **Is ACC Capability=true** is enabled to work with an agent. For details on the MID Server capabilities, see [MID Server capabilities](https://www.servicenow.com/docs/access?context=mid-server-capabilities&version=australia&pubname=australia-integrate-applications&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **MID Server** &gt; **Capabilities**.

2.  Select a capability to enable the MID Server to work with the agent.

    1.  Select the ACC Capability column next to the AgentClientCollector entry.

    2.  Set the value to **true**.

3.  Enable other capabilities for Agent Client Collector MID Servers by selecting the Is ACC Capability column next to the AgentClientCollector entry and setting the value to **true**.


## Result

MID Servers with the same capabilities are eligible to be used during automatic MID Server selection.

**Parent Topic:**[Automatic MID Server selection](../concept/acc-auto-mid-selection.md)

