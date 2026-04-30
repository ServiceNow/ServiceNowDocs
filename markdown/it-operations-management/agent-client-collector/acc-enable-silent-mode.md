---
title: Pause Agent Client Collector data collection
description: If CPU consumption on your server is getting too high, you can manually turn off the Agent Client Collector data collection to pause all checks performed by the agent, except for the agent's keep alive messages.
locale: en-US
release: xanadu
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Enabling Agent Client Collector data collection, Agent Client Collector Framework, Agent Client Collector, IT Operations Management]
---

# Pause Agent Client Collector data collection

If CPU consumption on your server is getting too high, you can manually turn off the Agent Client Collector data collection to pause all checks performed by the agent, except for the agent's keep alive messages.

## Before you begin

Role required: agent\_client\_collector\_admin

## Procedure

1.  Navigate to **All** &gt; **Agent Client Collector** &gt; **Agents**.

    The **Agent Client Collectors** page appears, displaying the list of configured agents.

2.  Select the checkbox next to the relevant agents.

3.  In the **Actions on selected rows...** dropdown, select **Pause data collection** to pause data collection on the agents \(**Data Collection = Off \(manual\)**\).

    Select **Resume data collection** to resume data collection on the agents.

    Alternatively, you can set the status of an agent by selecting the agent and in the **Related Links** section, select the **Pause data collection** link to pause data collection on the agent. To resume data collection on the agent, select the **Resume data collection** link.


**Parent Topic:**[Enabling Agent Client Collector data collection](../concept/data-collection-enabling.md)

