---
title: Create a risk indicator
description: Create a risk indicator to identify the possibility of a future adverse impact on your organization. Indicators are an early warning system, and they enable you to take preventative action on the risks.
locale: en-US
release: yokohama
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Use, Risk Management, Governance, Risk, and Compliance]
---

# Create a risk indicator

Create a risk indicator to identify the possibility of a future adverse impact on your organization. Indicators are an early warning system, and they enable you to take preventative action on the risks.

## Before you begin

Role required: sn\_risk.manager or sn\_risk.admin

## About this task

Generally, indicators are automatically created using the normal process of indicator templates. You can also manually create new indicators. You can also create an indicator by using an indicator template. When you relate an indicator template to a risk statement, the risk indicators are automatically generated.

## Procedure

1.  Navigate to **All** &gt; **Risk** &gt; **Indicators** &gt; **Indicators**.

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

Record that the entity applies to.

</td></tr><tr><td>

Risk

</td><td>

Filtered risk that is related to the indicator.**Note:** If you have selected an indicator template, then the risk is also filtered based on the template.

</td></tr><tr><td>

Owning group

</td><td>

Group that owns the indicator.

</td></tr><tr><td>

Owner

</td><td>

Owner of the indicator. This field is automatically set to the owner's name based on the risk.

</td></tr><tr><td class="sub-head" colspan="2">

Method

</td></tr><tr><td>

Type

</td><td>

Method used to determine the type of indicator. The choices are as follows:-   **Manual**: Manual indicators are used for data that cannot be retrieved from a ServiceNow instance because it comes from an external system, such as customer data from a third-party sales system.
-   **Basic**: Basic indicators are automated indicators based on an indicator source. The indicator source specifies a table and a frequency at which the scores from this table are saved.
-   **Script**: Scripted indicators use a custom script to collect the data.


</td></tr><tr><td>

Target type

</td><td>

Type of the target value. The choices are as follows:-   **None**: Use this option if you do not want to set up any target or threshold for the indicator.
-   **Percentage**: Use this option to determine the indicator result by a percentage value.
-   **Count**: Use this option to determine the indicator result by a count value or total number.


</td></tr><tr><td>

Value mandatory

</td><td>

Option to decide if a value must be compulsory in the indicator task for a manual indicator. **Note:** This option appears only if **Manual** is selected from the **Type** field. This option is automatically selected when **Count** or **Percentage** is selected from the **Target type** field.

</td></tr><tr><td>

Target

</td><td>

Value to determine if the indicator will pass or fail.

</td></tr><tr><td>

Result based on target value

</td><td>

Result configuration field. The choices are as follows:-   **Passed**
-   **Failed**
 For example, assume you enter `100` in this field. If the indicator result output is more than 100, then the indicator status will pass or fail based on the value configured in this field.

</td></tr><tr><td>

Instructions for collecting data

</td><td>

More instructions on how to collect data.

</td></tr><tr><td class="sub-head" colspan="2">

Supporting Data

</td></tr><tr><td colspan="2">

**Note:** Starting with version 10.1, the system displays the actual historical data for the supporting data records from the indicator results or indicator tasks.

</td></tr><tr><td>

Collect supporting data

</td><td>

Option to enable collecting supporting data or evidence every time the indicator runs.

</td></tr><tr><td>

Source table

</td><td>

Table used for collecting supporting data.

</td></tr><tr><td>

Supporting data fields

</td><td>

Fields of the source table that are used for collecting the supporting data.

</td></tr><tr><td>

Sample size

</td><td>

Minimum number of records that must be used for collecting supporting data.

</td></tr><tr><td class="sub-head" colspan="2">

Basic Criteria

</td></tr><tr><td colspan="2">

To filter the data on the source table, use the basic criteria. This section appears only when **Manual** or **Basic** is selected from the **Type** field.

</td></tr><tr><td>

Criteria

</td><td>

Criteria to filter the data from the source table.

</td></tr><tr><td>

Use reference field

</td><td>

Option to enable the use of the **Reference field**.

</td></tr><tr><td>

Reference field

</td><td>

Connection between the supporting data table and the **Applies to record** field of the entity.

</td></tr><tr><td class="sub-head" colspan="2">

Additional Criteria

</td></tr><tr><td colspan="2">

To create indicators with targets, use the advanced filter criteria. This section appears only when you select **Basic** from the **Type** field. This section is used to provide more filter criteria.

</td></tr><tr><td>

Additional criteria

</td><td>

More criteria to filter the data to calculate the target value. This section only appears when **Percentage** is selected from the **Target type** field.

</td></tr><tr><td class="sub-head" colspan="2">

Schedule

</td></tr><tr><td>

Collection frequency

</td><td>

Collection frequency for indicator results. Indicator tasks and results are generated automatically based on the indicator schedule.

</td></tr><tr><td>

Next run time

</td><td>

Next collection time for indicator results. This field is automatically set based on the value in the **Collection frequency** field.

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
</table>4.  Click **Submit**.


## Result

The risk indicator is created and is ready to be executed.

**Parent Topic:**[Using Risk Management](../concept/using-risk-mgmt.md)

