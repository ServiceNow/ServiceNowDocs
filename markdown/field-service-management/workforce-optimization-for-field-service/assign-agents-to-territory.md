---
title: Add suggested agents to a territory
description: View suggested agents of a particular territory and add them directly to a territory.
locale: en-US
release: australia
product: Workforce Optimization for Field Service
classification: workforce-optimization-for-field-service
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure resources, Territory Planning, Set up workforce, Configure, Field Service Management]
---

# Add suggested agents to a territory

View suggested agents of a particular territory and add them directly to a territory.

## Before you begin

Role required: sn\_fsm\_tp.fsm\_territory\_planner, sn\_fsm\_tp.fsm\_territory\_manager

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace**.

2.  Click the Lists icon \(![Lists icon.](../image/lists-icon.jpg)\).

3.  In the **Field Service Territories** list, select **All**.

4.  Click the territory for which you want to view suggested agents and add them to the territory.

    The territory record appears in a new tab.

5.  Click the Suggested Agents icon \(![Suggested Agents icon.](../image/suggested-agents.jpg)\).

    The **Available Members** list appears with the suggested agents.

6.  Select **Add** on the agent card.

    The message appears as the user has been added to territory.

7.  Select **Save**.

    The agent is added to the territory and appears in the **Agent Memberships** tab.

8.  Define the work duration for agents.

    1.  On the **Agent Memberships** tab, open the agent's record.

    2.  Select **Agent Schedules** tab and click **New**.

    3.  On the form, fill in the fields.

        |Fields|Description|
        |------|-----------|
        |From Date|Start date of the work duration for the territory.|
        |To date|End date of the work duration for the territory. For more information, see **sn\_fsm\_tp.territory\_membership\_override\_to\_date** in [Field Service Territory Planning console properties](../reference/territory-planning-components-fsm.md#).|
        |User|Name of agent.|
        |Work schedule|Select the work schedule. For example 8 AM to 5 PM.|
        |Type|Select **Primary Work** for agent as a primary contact for the selected territory.|

    4.  Select **Save**.

        The agent's work duration is specified for the territory.


