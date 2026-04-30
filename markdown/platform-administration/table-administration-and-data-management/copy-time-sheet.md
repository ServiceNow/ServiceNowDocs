---
title: Copy time cards from a previous time sheet
description: Another option for creating time cards is to copy them from an existing timesheet, which copies all the time cards \(for project as well as non-project tasks\) from a selected time sheet.
locale: en-US
release: yokohama
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Create a time card, Time cards, Time Card management, Work with the Task table, Table administration, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Copy time cards from a previous time sheet

Another option for creating time cards is to copy them from an existing timesheet, which copies all the time cards \(for project as well as non-project tasks\) from a selected time sheet.

## Before you begin

Role required: timecard\_user

## About this task

You can also perform this task from the [Time Sheet Portal](../concept/worker-portal.md).

## Procedure

1.  Open the time sheet record that you want to create the time cards for.

2.  Click the **Copy from previous time sheet** related link.

3.  In the **Select Time Sheet** field, select a previous time sheet that you want to copy the time cards from.

4.  You can copy the time logged for the tasks in the previous time sheet, select the **Copy time logged** check box.

5.  Click **OK**.


## Result

-   **Time cards for project tasks**

    Time cards for all the project tasks that are in progress or planned in the current week are copied from the selected time sheet. If a time card for a project task exists, a duplicate time card is not created during copying.

-   **Time cards for non-task category**

    Time cards for all non-task category such as meetings and trainings are copied from the selected time sheet. If a time card for a non-task category exists, a duplicate time card is created during copying.


**Note:**

-   If the previous time sheet has rate types and the time sheet policy of the user allows rate types, then rate types are also copied into the current time sheet.

-   If the previous time sheet has rate types, but the time sheet policy of the user no longer allows rate types, then rate types are not copied to the current time sheet.
-   If the previous time sheet has a rate type that is inactive, that rate type is not copied. If necessary, the user can enter a different rate type before saving the individual time cards.

**Parent Topic:**[Create a time card](t_CreateATimeCard.md)

