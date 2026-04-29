---
title: Restart an agent manually
description: Perform manual restart of an agent when the agent configuration file has been refreshed, or if the agent is unstable. You can perform manual restart only on agents installed in a Windows environment and for Linux-based agents that use systemd.
locale: en-US
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [ACC installation, ACC deployment - servers, Configuring Agent Client Collector, Agent Client Collector, IT Operations Management]
---

# Restart an agent manually

Perform manual restart of an agent when the agent configuration file has been refreshed, or if the agent is unstable. You can perform manual restart only on agents installed in a Windows environment and for Linux-based agents that use `systemd`.

## Before you begin

Role required: agent\_client\_collector\_admin

## Procedure

1.  Navigate to **All** &gt; **Agent Client Collector** &gt; **Agents**.

    The **Agent Client Collectors** page appears with the list of agents.

    ![Agent Client Collectors list](../image/ACC-Agent-Client-Collectors.png)

2.  Select the check box of the agent you want to restart.

    You can select multiple agents.

3.  In the **Actions on selected rows...** list underneath the list of agents, select **Restart agent**.

    A confirmation dialog box appears.

    ![Restart agent confirmation dialog box](../image/ACC-Restart-Confirm.png)

4.  Select **Restart**.

    Alternatively, you can restart the agent from within the agent record by selecting the agent name and, in the **Related Links** section, select **Restart agent**.


