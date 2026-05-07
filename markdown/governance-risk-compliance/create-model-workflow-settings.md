---
title: Configure Model Workflow Settings
description: Configure the conditions and frequency for scheduling assessment and validation tasks to maintain a structured and timely approach to model risk management.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [model workflow settings, assessments, validations, model risk management]
breadcrumb: [Configure, Model Risk Management, Governance, Risk, and Compliance]
---

# Configure Model Workflow Settings

Configure the conditions and frequency for scheduling assessment and validation tasks to maintain a structured and timely approach to model risk management.

## Before you begin

Role required: sn\_model\_risk\_mgmt.model\_governance or sn\_model\_risk\_mgmt.admin

## About this task

This task explains how to configure the frequency for assessment and validation tasks, and define filter conditions. You can schedule assessment and validation tasks for a model risk in the Monitor stage. Based on the configuration, tasks are automatically created for model risks that match the defined conditions in the workflow settings.

**Note:** Models with customized frequencies at the model risk record level aren’t affected.

To manually schedule assessment and validation tasks from the model risk record, refer to [Schedule assessment and validation tasks](schedule-assessment-and-validation-tasks.md).

## Procedure

1.  If you're a Model Risk Management admin \[sn\_model\_risk\_mgmt.admin\], navigate to **All** &gt; **Model Risk Configuration** &gt; **Model Workflow Settings**, and continue from step 3.

2.  Users with sn\_model\_risk\_mgmt.model\_governance role, navigate to **All** &gt; **Model Risk Workspace** and do the following:

    1.  Select the list ![](../image/list-icon-mrm.png) icon.

    2.  From the list, navigate to **Model risk configurations** &gt; **Model workflow settings**.

    3.  Continue from step 3.

3.  Select **New**.

4.  On the Create New Model Workflow Settings form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Unique name of the model workflow settings.|
    |Table|Table that the workflow setting applies to. This field is automatically set to **Model Risk**.|
    |Priority|Priority level for this workflow setting. If multiple workflow settings match the same conditions, the system uses the one with the highest priority.|
    |Active|Option to activate the workflow setting. When active, the defined scheduling rules and frequencies are applied to the filtered models.|
    |Filter condition|Conditions that determine which model records the workflow applies to. Select **Set conditions** to choose filter criteria. For more information, refer to [Condition builder](https://www.servicenow.com/docs/access?context=c_ConditionBuilder&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).|

5.  Select **Save**.

6.  To update task schedules, go to the **Frequency settings** tab.

7.  Define the task frequency for Model risk assessment and Model validation task types.

8.  On the Frequency form, fill in the fields.

<table id="table_uwr_vsn_dhc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Frequency

</td><td>

Option to define how often the assessments and validations should occur.

</td></tr><tr><td>

Duration \(days\)

</td><td>

Number of days within which the assessment or validation must be completed after it’s scheduled.

</td></tr><tr><td>

Repeat every

</td><td>

Interval value for how often the task repeats. For example, enter 2 to repeat every 2 units of the selected period. You can select the unit value in the **Period** field. This field appears only when **Custom** is selected from **Frequency** field.

</td></tr><tr><td>

Period

</td><td>

Time unit for the custom interval. The options are as follows:-   **Days**
-   **Weeks**
-   **Months**
-   **Years**
This field appears only when **Custom** is selected from **Frequency** field.

</td></tr></tbody>
</table>    **Note:** Updating the frequency applies the change to all filtered models, except those where the frequency is modified at the model level.

9.  Select **Save**.


