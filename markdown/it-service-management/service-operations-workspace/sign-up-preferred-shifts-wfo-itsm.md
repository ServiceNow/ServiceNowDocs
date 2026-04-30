---
title: Sign up for your preferred shifts
description: Specify one or more shifts in a schedule plan for which you would prefer to sign up.
locale: en-US
release: zurich
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Service Operations Workspace - Scheduling, Workforce Optimization for ITSM in the Service Operations Workspace, Optimize, Service Operations Workspace for ITSM, IT Service Management]
---

# Sign up for your preferred shifts

Specify one or more shifts in a schedule plan for which you would prefer to sign up.

## Before you begin

Role required: sn\_shift\_planning.agent

## About this task

You can receive notifications when your manager makes a schedule plan available for sign up. You can also receive notifications when the schedule plan that's open for sign up is due on the current day or when it's due soon.

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  Select the Schedule icon \(![Schedule icon](../../itsm-manager-workspace/image/schedule-icon.png)\).

3.  Select the **Sign up shifts** tab.

    You can use keywords to search the schedule plans, and view all schedules with active shifts for your assignment groups that you can sign up for. Use the pagination to scroll through all available schedule plans.

    The current state of each schedule plan displays as a highlight in each card. The table below describes the highlighted value.

    |Highlighted value|Description|
    |-----------------|-----------|
    |Available|Shifts for the schedule plan are available for sign up.|
    |Draft|Shifts you've considered for sign-up but have not completed the sign-up process.|
    |Completed|Submitted one or more preferred shifts within the schedule plan.|
    |Closed Incomplete|The schedule plan currently does not have shifts for which you could sign up.|
    |Closed Complete|The schedule plan has at least one preferred shift for which you've signed up.|

4.  Select the Overlapping time off icon \(![Overlapping time off](../../configurable-workforce-optimization-itsm/image/overlapping-time-off-icon.png)\) to analyze if the time off you have requested or the ones that have been approved overlap with the schedule plan available to you for sign up.

5.  To sign up for your preferred shifts, select **Add shifts**.

    You can only sign up for shifts in the schedule plan that have not been published yet.

    The Add shifts pop-up appears. You can search for shift using the search bar and select shifts to save as draft.

    You can sign up for a maximum number of shifts that your administrator has set up in the **sn\_shift\_planning.max\_shifts\_allowed\_for\_signup** system property.

6.  To save the selected shifts for sign-up, select **Save Shifts** and then select **Save as draft**.

7.  Select the plus \(+\) sign and sign up for additional shifts.

    When you have more than one shift, you can reorder them by using the up or down arrows in card for each shift.

8.  Select **Submit**.

    All shifts you have added for sign up will be submitted.


**Parent Topic:**[Service Operations Workspace - Scheduling](../concept/itsm-sow-workspace-scheduling.md)

