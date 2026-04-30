---
title: Repeat high-volume upgrade for failed agents
description: If high-volume upgrade fails for specific agents, you must clear the problematic agents' history to re-enable upgrade. If the target upgrade version changes, you don't need to clear the agents' history, as the agents upgrade with the next scheduled high-volume upgrade.
locale: en-US
release: yokohama
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2025-04-10"
reading_time_minutes: 1
breadcrumb: [Perform high-volume Agent Client Collector upgrade, Agent Client Collector installation, Configuring Agent Client Collector Framework, Agent Client Collector Framework, Agent Client Collector, IT Operations Management]
---

# Repeat high-volume upgrade for failed agents

If high-volume upgrade fails for specific agents, you must clear the problematic agents' history to re-enable upgrade. If the target upgrade version changes, you don't need to clear the agents' history, as the agents upgrade with the next scheduled high-volume upgrade.

## Before you begin

Roles required: agent\_client\_collector\_admin

-   In a Windows environment: Local SYSTEM account
-   In a Linux environment: sudo rpm/dpkg

## Procedure

1.  Navigate to the Agent Client Collectors page **All** &gt; **Agent Client Collector** &gt; **Agents**.

2.  Select an entry for which the **Version** number is not the highest available version.

3.  Locate the **Agent Upgrade Histories** tab.

    ![Agent Upgrade Histories tab](../image/agent-upgrade-histories-tab.png)

4.  Underneath the check box ![Check box](../image/check-box-icon.png) icon, hover next to a failed upgrade entry and select the check box that appears.

5.  Select the arrow next to the **Actions on selected rows...** drop-down and select **Delete**.


## Result

The specified agents will be upgraded with the next scheduled high volume upgrade.

