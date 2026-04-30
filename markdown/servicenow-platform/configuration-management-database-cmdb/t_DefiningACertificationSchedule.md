---
title: Define a certification schedule
description: A certification schedule specifies the fields to display, the fields that require certification, certification task assignments, completion requirements for task owners, frequency of schedule, and detailed instructions.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Data Certification planning, Data Certification on Core UI, Data Certification, CMDB data management, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Define a certification schedule

A certification schedule specifies the fields to display, the fields that require certification, certification task assignments, completion requirements for task owners, frequency of schedule, and detailed instructions.

## Before you begin

Role required: admin

## About this task

Use the preview option to see what tasks are created before saving the schedule. If the tasks are not what you want, edit the schedule and preview the tasks again. The system creates certification tasks automatically when it executes a schedule.

To schedule a certification:

## Procedure

1.  Navigate to **All** &gt; **Data Certification** &gt; **Schedule Definitions**.

2.  Click **New**

3.  Fill in the fields \(see table\).

4.  Click **Submit**.

<table id="table_mnf_j53_3p"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

A schedule name.

</td></tr><tr><td>

Filter

</td><td>

A certification filter for this schedule.

</td></tr><tr><td>

Table

</td><td>

\[Read-only\] The table holding the records to be certified. To change the table name, select a different **Filter** or create a new **Filter**.

</td></tr><tr><td>

Display fields

</td><td>

The fields displayed in the Certification Task list to provide context. These do not require certification themselves. For example, although users are not required to certify the **Name** field of a record, it displays so that users know what record they are certifying.

</td></tr><tr><td>

Certification fields

</td><td>

The fields to certify on this certification schedule.

</td></tr><tr><td>

Assignment type

</td><td>

A choice list to select how the certification schedule assigns the certification tasks.-   **User Field**: Select a user reference field on the table being certified. As an example, select the user named in the **Managed by** field to identify the user who performs the task. This selection displays the **Assign to** and **Assign to empty** fields. If the reference field on the record is empty, the value in the **Assign to empty** field is used.
-   **Specific User**: Select a specific user to perform the tasks. This selection displays the **User** field.
-   **Group Field**: Select a group reference field on the table being certified. As an example, select the **Support group** field to identify the user who performs the task. This selection displays the **Assign to group** and **Assign to empty** fields. All members of the group from the reference field on the record are assigned to the tasks. If the reference field on the record is empty, the value in the **Assign to empty** field is used.
-   **Specific Group**: Select a specific group to perform the tasks. This selection displays the **Group** field. All members of the named group are assigned to the tasks.


</td></tr><tr><td>

User

</td><td>

This field appears when:-   **Assignment type** is **Specific User**. This system assigns this user to all certification tasks for this schedule.
-   The **Assign to empty** field is set to **Create Assigned Task**, and you have selected **User Field** as the assignment type. The system assigns this user to certification tasks containing unassigned records.
 You can only select users with the certification role.

</td></tr><tr><td>

Assign to group

</td><td>

The group field that defines the group assigned to the certification tasks. This field is available only when the **Assignment type** is **Group Field**.

</td></tr><tr><td>

Group

</td><td>

The specific group to which certification tasks are assigned for this schedule. This field is available only when the **Assignment type** is **Specific Group**

</td></tr><tr><td>

Assign to

</td><td>

The user field that defines which user is assigned to the certification task. This field is available only when the **Assignment type** is **User Field**.

</td></tr><tr><td>

Assign to empty

</td><td>

The behavior to use if the field selected in **Assign to** or **Assign to group** is blank on the record being certified. For example, if a task must be assigned to a manager, but no manager is identified, the value in this field determines what happens. This field appears only when the **Assignment type** is **User Field** or **Group Field**. The possible selections are:-   **Do Not Create Task**: No task is created when the **Assign to** or **Assign to group** field is empty.
-   **Create Unassigned Task**: Create a task, but do not assign it to any user or group. The task can be manually assigned later.
-   **Create Assigned Task**: Create a task and assign it to the user or group specified. If you selected an assignment type of **User Field**, the **User** field is available. If you selected the **Group Field** type, the **Group** field is available.
 The schedule automatically creates certification tasks for all records that do have "Assign to" populated, regardless of which selection you make for "Assign to empty."

</td></tr><tr><td>

Days to complete

</td><td>

\[Required\] The number of days that task owners have to complete the certification tasks. When the certification schedule is part of a certification audit definition, the **Days to Complete** audit definition value overrides the value set for the certification schedule.

</td></tr><tr><td>

Active

</td><td>

Check box to activate this certification schedule, generating certification tasks at the scheduled date and time. Clear this check box to hide scheduling fields on the form \(except **Last run date**\) and not generate certification tasks.

</td></tr><tr><td>

Run

</td><td>

How often to run the schedule that generates certification tasks:-   Daily
-   Weekly
-   Monthly
-   Periodically
-   Once
-   On Demand


</td></tr><tr><td>

Day

</td><td>

When **Run** is **Weekly**, the day of the week when the schedule runs and generates certification tasks.When **Run** is **Monthly**, the day of the month the schedule runs and generates certification tasks. If the day is **29**, **30** or **31**, the certification runs on the last day of the month for shorter months.

</td></tr><tr><td>

Repeat Interval

</td><td>

When **Run** is **Periodically**, the frequency that the schedule runs to generate certification tasks, entered in time, days, or both. For example, set **Days** to **10** and **Hours** to **14:00:00** to run the schedule and generate certification tasks every 10 days at 14:00.

</td></tr><tr><td>

Starting

</td><td>

When **Run** is **Periodically** or **Once**, the date and time the schedule runs and generates certification tasks.

</td></tr><tr><td>

Time

</td><td>

When **Run** is **Daily**, **Weekly**, **Monthly**, or **Once**, the time of day, on a 24-hour clock, the schedule runs and generates certification tasks.

</td></tr><tr><td>

Last run date

</td><td>

\[Read-only\] The date and time that the schedule ran last, either on its regular schedule or manually, and generated certification tasks.

</td></tr><tr><td>

Next scheduled run

</td><td>

\[Read-only\] The next date and time the schedule runs and generates certification tasks.

</td></tr><tr><td>

Task Description

</td><td>

A description to add to the **Short Description** field of the certification task.

</td></tr><tr><td>

Instructions

</td><td>

An HTML field for providing instructions to the user or group performing the certification.

</td></tr></tbody>
</table>
**Related topics**  


[Data Certification planning](../concept/c_PlanningDataCertification.md)

