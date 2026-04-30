---
title: Create and run a manual risk indicator in the Risk Workspace
description: Create and run a manual risk indicator to identify the possibility of a future adverse impact on your organization. Indicators are an early warning system and they enable you to take preventative actions on risks. In a manual indicator, the results are manually gathered using task assignments.
locale: en-US
release: zurich
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Use Risk Workspace, Risk Management, Governance, Risk, and Compliance]
---

# Create and run a manual risk indicator in the Risk Workspace

Create and run a manual risk indicator to identify the possibility of a future adverse impact on your organization. Indicators are an early warning system and they enable you to take preventative actions on risks. In a manual indicator, the results are manually gathered using task assignments.

## Before you begin

Role required: sn\_risk.manager or sn\_risk.admin

## Procedure

1.  Navigate to **All** &gt; **Risk** &gt; **Risk Workspace** &gt; **Indicators** &gt; **Risk indicators**.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_ynl_yjz_dv"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Category

</td><td>

Category of the indicator. For example, select **Risk Indicator** to create a risk indicator.

</td></tr><tr><td>

Inherit from template

</td><td>

Option to create the indicator from an existing template.

</td></tr><tr><td>

Template

</td><td>

Template used to create the indicator. This field appears only if the **Inherit from template** option is selected.

</td></tr><tr><td>

Override template

</td><td>

Option to override the template's properties such as the name of the indicator.

</td></tr><tr><td>

Name

</td><td>

Name of the indicator. If you select a template in the **Template** field, then this field is automatically set to the template name.

</td></tr><tr><td>

Description

</td><td>

Brief description of the indicator. This field is automatically set if you select a template in the **Template** field.

</td></tr><tr><td>

Entity

</td><td>

Entity used to filter risks.

</td></tr><tr><td>

Applies to record

</td><td>

Record that the entity applies to. This field is automatically set.

</td></tr><tr><td>

Risk

</td><td>

Filtered risk that is related to the indicator.**Note:** If you have selected an indicator template, then the risk is also filtered based on the template.

</td></tr><tr><td>

Owning group

</td><td>

Group that owns the indicator. This field is automatically set based on the owning group of the risk.

</td></tr><tr><td>

Owner

</td><td>

Owner of the indicator. This field is automatically set to the owner's name based on the risk.

</td></tr><tr><td class="sub-head" colspan="2">

Method

</td></tr><tr><td>

Type

</td><td>

Method used to determine the type of indicator. Select **Manual**.

</td></tr><tr><td>

Target type

</td><td>

Type of the target value. Choices are as follows:-   **None**: Use this option if you do not want to set up any target or threshold for the indicator.
-   **Percentage**: Use this option to determine the indicator result by a percentage value.
-   **Count**: Use this option to determine the indicator result by a count value or total number.


</td></tr><tr><td>

Value mandatory

</td><td>

Option to decide if a value is required in the indicator task for a manual indicator. **Note:** This option is automatically selected when **Count** or **Percentage** is selected from the **Target type** field.

</td></tr><tr><td>

Target

</td><td>

Numerical value that is your goal for the indicator. This value determines if the indicator succeeded \(passed\) or failed. For example, if your goal for employee retention is 80%, you can enter the goal as the value. Any result less than 80% would mean the indicator failed.

</td></tr><tr><td>

Result if the value meets or exceeds the target value

</td><td>

Result configuration field. The choices are as follows:-   **Passed**
-   **Failed**
 For example, assume you enter `80` in the **Target** field. If the indicator result output is more than 80, then the **Indicator status** field is set to **Passed** or **Failed** based on the value configured in the **Result based on target value** field.

</td></tr><tr><td>

Instructions for collecting data

</td><td>

More instructions on how to collect data.

</td></tr><tr><td>

Reference field

</td><td>

Connection between the supporting data table and the **Applies to record** field of the entity.

</td></tr><tr><td class="sub-head" colspan="2">

Basic Criteria

</td></tr><tr><td colspan="2">

**Note:** This section appears only after you specify supporting data.

</td></tr><tr><td>

Criteria

</td><td>

Criteria to filter the data from the source table. Click **Set conditions** inside the field and create filters for the conditions.

</td></tr><tr><td class="sub-head" colspan="2">

Schedule

</td></tr><tr><td>

Collection frequency

</td><td>

Collection frequency for indicator results. Indicator tasks and results are generated automatically based on the indicator schedule.

</td></tr><tr><td>

First run date

</td><td>

Date the indicator was first run.

</td></tr><tr><td>

Next run date

</td><td>

Next collection time for indicator results. This field is automatically set based on the value in the **Collection frequency** field. You can also edit this field and change the date.**Note:** This field only gets updated based on the scheduled runs and not when the indicators are manually executed.

</td></tr><tr class="sub-head"><td class="sub-head" colspan="2">

Results

</td></tr><tr><td>

Status

</td><td>

Status of the indicator to show whether the indicator passed or failed.

</td></tr><tr><td>

Previous status

</td><td>

Previous status of the indicator to show whether the indicator passed or failed.

</td></tr></tbody>
</table>4.  Click **Save**.

5.  To collect supporting data, click **Specify supporting data** and do the following:

    1.  In the **Source table** field, select the table used for collecting supporting data.

    2.  In the **Supporting data fields** field, select the fields of the source table that are used for collecting the supporting data.

        While specifying the supporting data fields, you cannot dot-walk in the Risk Workspace.

    3.  In the **Sample size** field, specify the minimum number of records that must be used for collecting supporting data.

    4.  Click **Save** and reload the form.

6.  Click **Execute**.

    An indicator task is created and assigned to the risk owner. After the risk owner closes the indicator task, the Indicator Results related list appears.

7.  To see the results of the indicator task, click the Indicator Results related list and do the following:

    1.  Click the result that you want to view.

    2.  To view the snapshot of the supporting data, click **View supporting data**.

    3.  To view a particular live record, click **View** for that record.

        Live records always open in the classic user interface and not in the Risk Workspace user interface.


**Parent Topic:**[Using the Risk Workspace](../concept/using-risk-workspace.md)

