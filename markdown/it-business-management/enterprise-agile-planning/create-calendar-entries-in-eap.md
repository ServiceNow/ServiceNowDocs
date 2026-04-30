---
title: Create calendar entries for iterations in EAP
description: Define timelines for planning calendars so that the teams can create their own iterations in the Backlog and Planning Board of Enterprise Agile Planning.
locale: en-US
release: yokohama
product: Enterprise Agile Planning
classification: enterprise-agile-planning
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure, Enterprise Agile Planning, Strategic Planning, Strategic Portfolio Management]
---

# Create calendar entries for iterations in EAP

Define timelines for planning calendars so that the teams can create their own iterations in the Backlog and Planning Board of Enterprise Agile Planning.

## Before you begin

Role required: sn\_apw\_advanced.eap\_admin

## About this task

This task is explained using Planning Interval \(PI\) and Sprint as an example. These are the calendars available by default in the workspace and PI is set as the parent for Sprint.

By the end of this task, you define the timeline for a PI and its child Sprints. The EAP teams can then create their own team-specific PIs and Sprints, within this defined timeline, in a naming convention of their choice.

**Note:** You can create PIs in a naming convention of your choice, but the Sprint names are predefined. After creating Sprints for the PI, you can manually update their names per your preference.

## Procedure

1.  Navigate to **Workspaces** &gt; **Strategic Planning Workspace**.

2.  From the **Settings** menu, select **Enterprise Agile Planning** &gt; **Planning calendars**.

3.  Select **Planning Interval** to create entries for it.

4.  Select **New calendar entry**.

5.  On the form, fill in the name of the entry, and the start and end dates for the planning interval.

    For example, you’re creating a PI for 01 January 2024 to 31 March 2024.

6.  Create calendar entries for the Sprint calendar based on the PI start and end dates.

    1.  Select **Create child entries on Sprint**.

    2.  In the **Number of child entries \(Sprint\)** field, enter the number of sprints you want to create for this PI.

    3.  In the **Sprint length \(days\)** field, enter the number of days your Sprint is made of.

    For the PI that spans from 01 January 2024 to 31 March 2024, you can create 6 Sprints with a length of 14 days each.

    ![New Planning Interval Calendar entry.](../images/eap-new-calendar-entry.png)

7.  Select **Create**.


## Result

A PI and its child sprints are created with the timelines that you defined. The EAP teams can create their own PI and Sprint iterations with their own naming convention.

## Example

PI 1 is created for 2024-01-01 to 2024-03-31. Within this PI, child six Sprints are created, each with a length of 14 days.

![PI1 and its child Sprints.](../images/eap-pi-and-sprint.png)

Under the Digital Banking portfolio, the teams create their own ARTs and Sprints as follows:

-   Payment Analytics ART creates two PIs: **Digi bank ST2 ART1 PI1** and **Digi bank ST2 ART1 PI2**.
-   The Agile Teams PAT Team 1 and PAT Team 2 create sprints within these PIs:
    -   PAT Team 1 creates **PAT 1 Sprint 1**, **PAT 1 Sprint 2**, and so on.
    -   PAT Team 2 creates **PAT 2 Sprint 1**, **PAT 2 Sprint 2**, and so on.

The teams can use these PIs and Sprints to schedule their work.

![Team-specific sprints in EAP Backlog.](../images/eap-teams-sprints.png)

