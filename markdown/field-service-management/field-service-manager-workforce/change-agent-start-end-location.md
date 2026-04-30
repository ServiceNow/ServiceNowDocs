---
title: Change start and end locations for agents
description: Change the start-of-day and end-of-day locations for your agents, offering the flexibility needed for specific work order tasks.
locale: en-US
release: yokohama
product: Field Service Manager Workforce
classification: field-service-manager-workforce
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Managing territories and agents from Territory Planning console, Manage workforce, Using Field Service Management, Field Service Management]
---

# Change start and end locations for agents

Change the start-of-day and end-of-day locations for your agents, offering the flexibility needed for specific work order tasks.

## Before you begin

Role required: sn\_fsm\_tp.fsm\_territory\_planner, sn\_fsm\_tp.fsm\_territory\_manager, wm\_admin

## About this task

Ensure the Territory Planning plugin is activated. For more information, see [Activate Field Service Territory Planning](Activate-fsm-territory-planning.md).

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Dispatching** &gt; **Agents**.

2.  Select the user for whom you want to add or change the start and end locations.

3.  Select the **Agent Schedule Attribute Plans** related list.

    **Note:** You can switch the agent's user profile view to **FSM Profile** or add the **Agent Schedule Attribute Plans** related list to the form if it doesn't appear by default.

4.  Select any existing field or select **New**.

    The **Agent Schedule Attribute Plan** form shows.

5.  In the **From** field, select the start date.

6.  In the **To** field, select the end date.

7.  In the **Start location** field, select the location where an agent starts work.

8.  In the **End location** field, select the location where an agent ends work.

9.  Select **Submit**.

    The `Agent Schedule Attribute Plans` table is updated with agent's start and end locations.


## Result

The scheduling mechanisms consider an agent's start and end locations from the `Agent Schedule Attribute Plans` table for the given day.

**Parent Topic:**[Managing territories and agents from Territory Planning console](../concept/using-territory-planning-console.md)

