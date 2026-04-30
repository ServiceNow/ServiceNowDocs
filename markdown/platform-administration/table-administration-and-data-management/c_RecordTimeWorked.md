---
title: Record time worked
description: The time card retrieves time accrued on a project or spent working on any record in the Task table from the Time worked field.
locale: en-US
release: yokohama
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Time Card management, Work with the Task table, Table administration, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Record time worked

The time card retrieves time accrued on a project or spent working on any record in the Task table from the **Time worked** field.

This field does not appear by default on the Project Task, Incident, Problem, and Change forms and must be added by personalizing the form. Time recorded in this field is used to populate an existing time card or to create a new time card if one does not exist. A [time sheet policy](../task/create-time-sheet-policy.md#time_sheet_policy_form) controls this behavior.

**Note:**

When time worked is updated, a time card is created only if:

-   the user is a time card user, AND
-   the user is assigned to the task through **Assigned to** or **Additional assignee list** field.

The Time worked field has a counter that acts like a stopwatch for the duration of the time spent in the record. A button in the field can stop and start the counter. By default, the Time worked counter is enabled and begins recording the elapsed time when the record is opened. Stop the counter with the stop button and restart it with the play button.

If you are creating time cards from time worked entries, you can ask your admin to add the **Time Worked** related list to display the time worked records on the time card form. You will also notice an informational message on the time card to let you know that changes to time worked records overrides values in the time card. This is displayed using a [Create a formatter and add it to a form](../../form-administration/task/t_CreateAFormatter.md), which can be added or removed by configuring the form.

**Parent Topic:**[Time Card Management](time-card-management.md)

