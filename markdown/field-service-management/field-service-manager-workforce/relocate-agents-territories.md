---
title: Move agents between territories in the Territory Planning console
description: Relocate agents between territories to add flexibility to their work.
locale: en-US
release: australia
product: Field Service Manager Workforce
classification: field-service-manager-workforce
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Managing territories and agents, Managing workforce, Use, Field Service Management]
---

# Move agents between territories in the Territory Planning console

Relocate agents between territories to add flexibility to their work.

## Before you begin

Role required: sn\_fsm\_tp.fsm\_territory\_planner, sn\_fsm\_tp.fsm\_territory\_manager

## About this task

-   Using the agent relocation process, you can customize agent membership attributes and availability. This includes changing the start-of-day and end-of-day locations for your agents, offering the flexibility needed for specific work order tasks.
-   By matching resource availability and addressing unscheduled work for agents, schedule planning is significantly improved.
-   When agents are relocated to another territory, any tasks assigned to them in the source territory are unassigned by default. You can also choose to alter the behaviour using `UnassignTaskOnAgentRelocation` extension point.

This video shows the agent relocation process.Agent relocation procedure 

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Territory Planning** &gt; **Territory Planning Console**.

2.  Select the territory and open the record.

3.  Select the Agent Relocation \(![Agent Relocation icon.](../image/agent-relocation.jpg)\) icon.

    The **Relocate agents** form appears in the contextual side panel.

4.  Choose the start date and time for the agent relocation.

5.  Choose the end date and time for the agent relocation.

6.  In the **Available agents** field, select the agents you want to relocate.

    If the agent has assigned tasks or is part of a crew, you see an inline message. You can then choose to proceed with the relocation or select other agents.

7.  Customize agent membership and availability in the source territory during the relocation period.

    1.  Select the **Set as Inactive Agents** option to set agents as inactive.

    2.  Select the **Set as Secondary Agents** option to designate agents as secondary agents.

    **Note:** If not selected, agents remain active and retain primary membership.

8.  In the **Destination territory** field, select the destination territory to which the selected agents are relocated.

9.  Customize agent membership and availability in the destination territory during the relocation period.

    1.  Select the **Set as Primary Agents** option to set agents as primary agents.

        **Note:** If not selected, agents default to secondary members.

    2.  Select the **Set new agent location** option to define the new location for agents.

10. Set the new location in the destination territory for the agents.

    1.  In the **Select start location** field, select the location where the agents start work in the destination territory.

    2.  In the **Select end location** field, select the location where the agents end work in the destination territory.

11. Select **Relocate**.

    A confirmation message appears to indicate the agents have been successfully relocated to the destination territory. Any existing assigned tasks for the agents in the source territory are unassigned and transitioned to **Pending Dispatch** state.


## Result

-   Agent memberships are updated for the specified source and destination territories based on the form selections.
-   **Resource Schedule Attributes** related list in the agent's user profile is updated.

