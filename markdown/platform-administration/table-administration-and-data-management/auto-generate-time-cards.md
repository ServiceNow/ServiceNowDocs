---
title: Auto-generate time cards
description: As an admin, you can configure a scheduled job to generate time cards automatically for project tasks assigned to time card users.
locale: en-US
release: australia
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Create time card, Time cards, Time Card management, Working with Task table, Table admin, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Auto-generate time cards

As an admin, you can configure a scheduled job to generate time cards automatically for project tasks assigned to time card users.

## Before you begin

Role required: admin

## About this task

In addition to the manual option **Generate Time Cards**, a scheduled job can be run to automatically generate the time cards for project tasks. A job can be scheduled to run every week, for example, on every Sunday to generate time sheets for all users for the next week. You can configure when to run the scheduled job based on the business process of the organization. By default, the scheduled job is turned off. For more information, see [Schedule a script execution](../../reference-pages/task/t_ScheduleAScriptExecution.md) .

**Note:** The scheduled job auto-generates time cards only for those users who have the **Auto create time cards every week** option set to true in their assigned [time sheet policy](create-time-sheet-policy.md#time_sheet_policy_form).

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  In the Scheduled Jobs list, select **Auto Generate Time Cards**.

3.  Configure the following parameters in the script as per the business requirements:

    -   run for \(CURRENT\_WEEK, NEXT\_WEEK, LAST\_WEEK\)
    -   Group Name \(includeGroups, excludeGroups\)
    **Note:**

    -   If a time card exists for a project task for the time card week, a duplicate time card is not created.
    -   Time cards are generated only for those project tasks that are in progress or planned in that week.
    -   The **Allow time card reporting on** field on the [project form](https://www.servicenow.com/docs/access?context=t_CreateAProject&version=australia&pubname=australia-it-business-management&ft:locale=en-US) determines the level that the time cards for the project tasks are created at.

## Example

The following example script is executed when a scheduled job is run to generate time cards for the `Current week` for the `Database` and `Hardware` groups:

```
// Clone this schedule job to run separately for different groups at different times
// One of the following values
// TimeCardConstants.CURRENT_WEEK
// TimeCardConstants.NEXT_WEEK
// TimeCardConstants.LAST_WEEK
var runFor = TimeCardConstants.CURRENT_WEEK;

// Comma separated group sys ids or group names. TimeSheet/TimeCards will be auto generated for time card users in the given groups.
var includeGroups = [Database,Hardware];
var excludeGroups = [];

var generator = new TimeCardGenerator();
generator.generateFromConfig(runFor, includeGroups, excludeGroups);
```

**Parent Topic:**[Create a time card](t_CreateATimeCard.md)

