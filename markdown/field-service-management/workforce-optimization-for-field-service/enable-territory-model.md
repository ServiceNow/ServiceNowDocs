---
title: Enable the Field Service territory model
description: Activate the territory model to display the Territory field in the work order task form so the task can be assigned to an agent or crew associated with the selected territory. The territory model maintains a record of territories mapped to it.
locale: en-US
release: yokohama
product: Workforce Optimization for Field Service
classification: workforce-optimization-for-field-service
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring Field Service Territory Planning, Setting up your workforce, Configuring Field Service Management, Field Service Management]
---

# Enable the Field Service territory model

Activate the territory model to display the **Territory** field in the work order task form so the task can be assigned to an agent or crew associated with the selected territory. The territory model maintains a record of territories mapped to it.

## Before you begin

Role required: sn\_fsm\_tp.fsm\_territory\_planner

## About this task

Activate the Field Service Territory Planning plugin \(com.snc.fsm\_territory\_planning\). For more information, see [Activate Field Service Territory Planning](Activate-fsm-territory-planning.md).

## Procedure

1.  Navigate to **All** &gt; **Territory Planning** &gt; **Territory Model**.

2.  Open the Field\_Service\_Territories territory model.

3.  Select the **Active** check box.

4.  Click **Update**.


## Result

After activating the Field Service territory model successfully, the **Territory** field is added to the work order task form. It allows you to assign tasks to agents or crews to specific territories.

The agent's calendar filters based on territories in the Dispatcher Workspace, and the **Qualifier type for Schedule Optimization** system property is automatically set to **Territory**. For more information, see [Schedule optimization properties](../reference/schedule-optimization-properties.md).

Moreover, with **sn\_fsm.use\_query\_rules** query rule being active, agents, dispatchers, and qualifiers can view the work order tasks if they are created in their territories, ensuring data security.

