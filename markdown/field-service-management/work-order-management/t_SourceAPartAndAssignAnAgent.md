---
title: Source a part and assign an agent
description: The work order sourcing option is useful when you want to assign a work order task to agents who already have the required parts in their stockroom or to a specific agent who needs you to obtain the parts for them.
locale: en-US
release: zurich
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Part requirements, Inventory, Manage work order tasks, Prepare work orders, Use, Field Service Management]
---

# Source a part and assign an agent

The work order sourcing option is useful when you want to assign a work order task to agents who already have the required parts in their stockroom or to a specific agent who needs you to obtain the parts for them.

## Before you begin

Role required: wm\_agent, wm\_qualifier, wm\_dispatcher, wm\_admin, or [qualifier combination role](../reference/r_UserRoleInstallWFieldSrvMgmnt.md)

## About this task

The sourcing option shows the full list of tasks and part requirements to source for a work order or task. For each task, the agents and stockrooms that have the required parts are listed. Also, the skills and parts required for each task are displayed. Select an agent to see if the agent has the skills and parts required for the task. The time slots during which the agent is available within the work order window are shown to help you schedule task work efficiently.

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Work Order** &gt; **All Work Orders**.

2.  Open a work order.

3.  Open a work order task that is not in **Closed** or **Cancelled** state.

4.  Click **Source**.

5.  In the Source Work Order list, click a work order task.

    The **Agent** field under **Agent info** is populated automatically based on information provided in the work order task.

6.  To specify a different agent, click the Lookup using list icon \(![List icon.](../image/IconReferenceLookup.png)\).

    Only agents that meet the criteria in the work order task are available for selection. The system populates the **Skills** and **Parts** fields automatically, based on the agent specified. If a not available icon \(![Not available icon.](../image/NotAvailableIcon.png)\) appears next to a part, the specified agent either does not have the part or does not have enough units of the part to complete the task.

7.  Point to the icon to obtain information about how many units of the part are needed and how many units the agent has in their stockroom.

8.  To filter agents and reserve parts, click the arrow next to **Agent info** to expand the section.

    -   Select the skills and parts options to filter the agents.
    -   Select **Reserve parts in agent stockroom** to reserve parts located in the specified agent's stockroom. This automatically sources the parts already present.
9.  In the **Date** field, select the date on which the work should take place.

    If the agent is available on the date specified, the **Assign** button appears in the **Schedule** field.

10. If necessary, you can update the **Scheduled start** and **Scheduled end** fields in the **Task info** section.

    -   If you change the **Scheduled start** and **Scheduled end** fields in the **Part Requirements** section at the top of the screen, the corresponding fields in **Task info** are also changed. If you make changes to the fields in the **Task info** section, the corresponding fields in the Part Requirements section are not changed.
    -   Any edits to the **Estimated travel duration**, **Estimated work duration**, or **Scheduled start time** fields on the Task form appear automatically in **Task info**.
11. Click **Assign**.

12. To revert your changes to Agent Info, click **Refresh**.

    You cannot use **Refresh** after you have saved the record.

13. Click **Save**.

    The agent is not assigned until you save the record.

14. Source any parts the specified agent does not yet have reserved.

    In the left pane, select a part from the list of part requirements under the task.

15. Click **Source Part** and complete the transfer order.


