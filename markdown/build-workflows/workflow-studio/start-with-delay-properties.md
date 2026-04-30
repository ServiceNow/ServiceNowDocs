---
title: Start with delay input properties
description: Specify a duration of time to wait before running an activity or a stage whose start rule and conditions have been met. Give users time to act during automated playbooks. Give users time to wait for a specific date and time to complete actions.
locale: en-US
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Stages and activities, Building playbooks, Use, Workflow Studio, Build workflows]
---

# Start with delay input properties

Specify a duration of time to wait before running an activity or a stage whose start rule and conditions have been met. Give users time to act during automated playbooks. Give users time to wait for a specific date and time to complete actions.

## Roles and availability

This input is available for all stages and common activities, except for the Placeholder activity. Users with the admin, playbook.admin, pd\_author, or pd\_content\_author can configure the properties of this input.

## Input properties

Open the activity or stage properties panel, show additional options, and enable the **Start with delay** option to configure the following input properties.

<table id="table_ajt_sr3_plb"><thead><tr><th>

Input

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Duration Type

</td><td>

Choice

</td><td>

Option to specify how long of duration to wait. Options include -   **Explicit Duration**: Wait for a specific time period, such as 5 minutes.
-   **Relative Duration**: Wait for a specific time period from a selected Duration data pill or date/time value, such as 5 minutes after the playbook starts.
-   **Percentage Duration**: Wait for a specific percentage of a time period between the start of the activity or stage and a specified end time, such as 50%.

**Note:** The percentage value must be from **0** through **100** only.


</td></tr><tr><td>

Wait for

</td><td>

Template Value

</td><td>

Option to set a duration value manually or to select a Duration data pill from the data pill picker ![Data pill picker](../images/data-pill-picker-icon.png).-   **Explicit Duration**: Wait duration in hours, minutes, and seconds.
-   **Relative Duration**: Wait duration in hours, minutes, and seconds before or after a specific time. Select **Relative Duration** to specify a wait duration from a specific date.

**Note:** Past dates don't affect the wait duration.


You can enter a wait value of up to 999 hours.**Note:** The actual wait duration can vary due to the instance processing time. The playbook always waits for the time that you specify for this field, but other work in the queue may add to the wait time.

</td></tr><tr><td>

Wait for Percentage

</td><td>

Integer

</td><td>

Percentage of time to wait from a specified end date before running an activity or stage. You can manually enter an end date or select a date/time data pill from the data pill picker ![Data pill picker](../images/data-pill-picker-icon.png). If you select an end date in the past, the wait duration is set to **0**. This field is only available when you set the **Duration Type** to **Percentage Duration**.

</td></tr><tr><td>

During the following schedule

</td><td>

Reference.Schedule \[cmn\_schedule\]

</td><td>

Schedule used to calculate an end date that occurs during your hours of operation. For example, the calculated end date for a 10-hour duration that occurs during a 8-5 weekdays schedule will always be one or more business days in the future. If you leave this field blank, the calculated end date does not follow a schedule. For information on creating schedules, see [Define a schedule](https://www.servicenow.com/docs/access?context=t_DefineASchedule&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

</td></tr></tbody>
</table>**Parent Topic:**[Stages and activities](../concept/process-automation-designer-lanes-activities.md)

**Related topics**  


[Add and configure a stage in a playbook](../task/add-configure-stage.md)

[Activity definitions](../concept/activity-definitions.md)

[Add and configure an activity in a playbook](../task/add-configure-activity.md)

[Use AI agent as an activity](../task/ai-agent-as-activity.md)

[Automation Assets](../concept/automation-assets.md)

[Optional activities](../concept/optional-activities.md#)

[Decision activities](../task/create-a-decision-activity.md)

[Decision stages](../task/create-decision-stage.md)

[Questionnaire activity](questionnaire-activity.md)

[Parallel branches](../task/create-parallel-activity.md)

[Add dynamic inputs to an activity](../task/add-dynamic-inputs-to-activity.md)

[Playbook activity state mapping](../../workspace/concept/playbook-activity-state-mapping.md)

