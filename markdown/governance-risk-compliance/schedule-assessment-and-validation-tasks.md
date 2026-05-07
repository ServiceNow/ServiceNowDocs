---
title: Schedule assessment and validation tasks
description: Schedule assessment and validation tasks for model risks in the Monitor stage to ensure regulatory compliance and effective risk management.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Use, Model Risk Management, Governance, Risk, and Compliance]
---

# Schedule assessment and validation tasks

Schedule assessment and validation tasks for model risks in the Monitor stage to ensure regulatory compliance and effective risk management.

## Before you begin

Role required: sn\_model\_risk\_mgmt.model\_governance or sn\_model\_risk\_mgmt.risk\_coordinator

## About this task

You can schedule assessment and validation tasks for a model risk in the Monitor stage. You can also configure the conditions and frequency for these tasks in the model workflow settings. Based on the configuration, the assessment and validation tasks are created automatically. For more information, refer to [Configure Model Workflow Settings](create-model-workflow-settings.md).

This task guides you on how to schedule assessment and validation tasks manually from the model risk record.

## Procedure

1.  Navigate to **All** &gt; **Model Risk Workspace**.

2.  Select the list icon ![](../image/list-icon-mrm.png).

3.  From the list, navigate to **Models** &gt; **Monitor**.

4.  Select the model record to schedule assessment and validation tasks.

5.  Select **Edit schedule** on the Assessment schedule or Validation schedule card.![Edit schedule button on the assessment and validation task cards.](../image/schedule-tasks.png)

6.  On the Edit assessment schedule dialog, fill in the fields.

<table id="table_bxs_q5j_hgc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Default frequency

</td><td>

Default assessment frequency defined in the model workflow settings. This field is auto-populated.

</td></tr><tr><td>

Last assessment date

</td><td>

Date when the last assessment was performed for the model. This field is auto-populated.

</td></tr><tr><td>

Frequency

</td><td>

How often assessments should be performed. The options are as follows:-   **Daily**: Creates an assessment every day.
-   **Weekly**: Creates an assessment once every week.
-   **Monthly**: Creates an assessment once every month.
-   **Quarterly**: Creates an assessment once every three months.
-   **Semi-annually**: Creates an assessment once every six months.
-   **Annually**: Creates an assessment once every year.
-   **Custom**: Enables you to define your own interval and period for scheduling assessments.
-   **None**: Disables automatic scheduling for assessments.
This field is auto-populated with the frequency defined in the Model workflow settings, if available. You can modify the value, and a Modified tag appears after the change.

</td></tr><tr><td>

Next assessment date

</td><td>

Date on which the next assessment is scheduled to start. This field is auto-populated based on the last assessment date and the defined frequency.**Note:** If assessment tasks are skipped, you must manually define the next assessment date.

</td></tr><tr><td>

Due in \(days\)

</td><td>

Number of days within which the assessment task must be completed after it starts.

</td></tr><tr><td>

Repeat every

</td><td>

Interval value for how often the assessment repeats. For example, enter 2 to repeat every 2 units of the selected period. You can select the unit value in the **Period** field. This field appears only when **Custom** is selected from **Frequency** field.

</td></tr><tr><td>

Period

</td><td>

Time unit for the custom interval. The options are as follows:-   **Days**
-   **Weeks**
-   **Months**
-   **Years**
This field appears only when **Custom** is selected from **Frequency** field.

</td></tr></tbody>
</table>7.  On the Edit assessment schedule dialog, fill in the fields.

<table id="table_pgy_sg1_2hc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Default frequency

</td><td>

Default validation frequency defined in the model workflow settings. This field is auto-populated.

</td></tr><tr><td>

Last validation date

</td><td>

Date when the last validation was performed for the model. This field is auto-populated.

</td></tr><tr><td>

Frequency

</td><td>

How often assessments should be performed. The options are as follows:-   **Daily**: Creates a validation task every day.
-   **Weekly**: Creates a validation task once every week.
-   **Monthly**: Creates a validation task once every month.
-   **Quarterly**: Creates a validation task once every three months.
-   **Semi-annually**: Creates a validation task once every six months.
-   **Annually**: Creates a validation task once every year.
-   **Custom**: Enables you to define your own interval and period for scheduling validation task.
-   **None**: Disables automatic scheduling for validation task.
This field is auto-populated with the frequency defined in the Model workflow settings, if available. You can modify the value, and a Modified tag appears after the change.

</td></tr><tr><td>

Next validation date

</td><td>

Date on which the next validation task is scheduled to start. This field is auto-populated based on the last validation date and the defined frequency.**Note:** If validation tasks are skipped, you must manually define the next validation date.

</td></tr><tr><td>

Due in \(days\)

</td><td>

Number of days within which the validation task must be completed after it starts.

</td></tr><tr><td>

Repeat every

</td><td>

Interval value for how often the validation task repeats. For example, enter 2 to repeat every 2 units of the selected period. You can select the unit value in the **Period** field. This field appears only when **Custom** is selected from **Frequency** field.

</td></tr><tr><td>

Period

</td><td>

Time unit for the custom interval. The options are as follows:-   **Days**
-   **Weeks**
-   **Months**
-   **Years**
This field appears only when **Custom** is selected from **Frequency** field.

</td></tr></tbody>
</table>8.  To use the frequency defined in the Model workflow settings, select **Revert to default frequency**.![Revert to default frequency button.](../image/revert-to-default-frequency.png)


**Parent Topic:**[Using Model Risk Management](../concept/using-mrm.md)

