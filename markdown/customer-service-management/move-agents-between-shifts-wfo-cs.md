---
title: Move agents to another shift or schedule
description: Move one or more agents from their current shift to a shift in the same schedule or in a different schedule for a specified date range.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/move-agents-between-shifts-wfo-cs.html
release: brazil
topic_type: task
last_updated: "2026-10-05"
reading_time_minutes: 3
keywords: [move agents, shift planning, team calendar, schedule]
breadcrumb: [Schedule, Workforce Optimization for Customer Service, Agent management, Use, Customer Service Management]
---

# Move agents to another shift or schedule

Move one or more agents from their current shift to a shift in the same schedule or in a different schedule for a specified date range.

## Before you begin

The Move agents feature is turned off by default. An administrator must turn on the Move agents feature by setting the **sn\_shift\_planning.enable\_move\_agents** system property to true.

The **Move Agents** option is displayed only for published schedules that have not yet ended. It is not displayed for schedules in Draft status or for schedules that have already ended.

Role required: sn\_shift\_planning.admin

## About this task

When you move agents, the system moves them from the source schedule to the target schedule for the date range that you specify. All the agents that you select share the same effective start and end dates.

For each move, you specify:

-   The source shift that the agents move from.
-   The target schedule and shift that the agents move to. The target schedule can be the same schedule as the source.
-   The agents to move.
-   The effective start and end dates.
-   Whether the agents return to the source shift after the effective end date.

## Procedure

1.  Navigate to **Workspaces** &gt; **Manager Workspace**.

2.  In the left navigation panel, select **Schedule**.

    The **Team calendar** tab opens by default.

3.  On the right side of the team calendar, select the **Show schedule** icon, which is the first icon.

4.  Select the schedule plan that contains the agents you want to move from.

5.  Select the shift that the agents are currently on.

    The **Work shift details** panel opens.

6.  In the **Assign agents** section, select **Manage** &gt; **Move agents**.

    The **Move agents** dialog box opens. The **Move from** section shows the current schedule plan, with its date range, and the current shift plan.

7.  In the **Move to** section, complete the fields.

<table id="move-agents-between-shifts-wfo-cs-fields"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Move from &gt; Schedule plan

</td><td>

The schedule plan that the agents are on now, with its start and end dates.This field is non-editable.

</td></tr><tr><td>

Move from &gt; Shift plan

</td><td>

The shift that the agents are on now. This is the shift that you selected on the team calendar.This field is non-editable.

</td></tr><tr><td>

Move to &gt; Schedule plan

</td><td>

The schedule that the agents move to. Select the current schedule to move agents to a different shift in the same schedule, or select a different schedule. This field is required.

</td></tr><tr><td>

Move to &gt; Shift plan

</td><td>

The shift that the agents move to. The list shows the shifts that are available for the schedule that you selected. This field is required.

</td></tr><tr><td>

Select agents

</td><td>

The agents to move. The list shows only the agents who are on the shift that you selected. This field is required.

</td></tr><tr><td>

Effective start date

</td><td>

The first day of the move, in `YYYY-MM-DD` format. To move agents for only a few days, enter dates that cover just those days. This field is required.

</td></tr><tr><td>

Effective end date

</td><td>

The last day of the move, in `YYYY-MM-DD` format. This field is required.

</td></tr><tr><td>

Return agents to source schedule after move ends

</td><td>

This field is visible only if there are days remaining to work in the source schedule after move is complete

</td></tr></tbody>
</table>8.  Select **Save**.

    A message confirms the move.


## Result

The agents move to the target shift for the date range that you specified. The shifts update for the agents in Manager Workspace and in the agents' own workspace. The system records each move as a Move Request record.

For each agent, the system does the following:

-   Creates a move request record that logs the move. The record is created first, so the history is kept even if the move fails partway through.
-   Removes the agent from the source shift for the effective period, if the source and target schedules cover overlapping dates. If the schedules don't overlap, there is nothing to remove.
-   Adds the agent to the target shift only for the days that the agent is not already scheduled on that target shift.

**Parent Topic:**[Scheduling in Workforce Optimization for Customer Service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/scheduling-configurable-wfo-cs.md)

