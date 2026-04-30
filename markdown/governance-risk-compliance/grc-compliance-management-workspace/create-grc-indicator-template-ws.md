---
title: Create a GRC indicator template using the Compliance Workspace
description: Compliance or risk managers create indicator templates in the Compliance Workspace from which many indicators can be created.
locale: en-US
release: xanadu
product: GRC: Compliance Management Workspace
classification: grc-compliance-management-workspace
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Manage control indicators using the Compliance Workspace, Using the Compliance Workspace, Performing compliance tasks in Compliance Workspace, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Create a GRC indicator template using the Compliance Workspace

Compliance or risk managers create indicator templates in the Compliance Workspace from which many indicators can be created.

## Before you begin

Role required:

-   sn\_compliance.admin or sn\_compliance.manager
-   sn\_risk.admin or sn\_risk.manager
-   sn\_audit.admin or sn\_audit.manager
-   sn\_grc.user

## Procedure

1.  Navigate to one of the following locations:

    -   **All** &gt; **Policy and Compliance** &gt; **Compliance Workspace** &gt; **Indicators** &gt; **Indicator Templates**.
    -   **Risk** &gt; **Indicators** &gt; **Indicator Templates**.
    -   **Audit** &gt; **Indicators** &gt; **Indicator Templates**.
2.  Select the **Create** list and click **Indicator**.

3.  Select **New**.

4.  On the form, fill in the fields.

<table id="table_ynl_yjz_dv"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the indicator.

</td></tr><tr><td>

Description

</td><td>

Description of the indicator.

</td></tr><tr><td>

Category

</td><td>

Category for which you’re creating an indicator template. For example, select **Risk Indicator Template** to create a risk indicator template.

</td></tr><tr><td>

Active

</td><td>

Option that determines whether the indicator template is active.

</td></tr><tr><td class="sub-head" colspan="2">

Method

</td></tr><tr><td>

Type

</td><td>

Method used to determine the type of indicator template. The choices are as follows:-   **Manual**: Manual indicators are used for data that can’t be retrieved from a ServiceNow instance because it comes from an external system, such as customer data from a third-party sales system.
-   **Basic**: Basic indicators are automated indicators based on an indicator source. The indicator source specifies a table and a frequency at which the scores from this table are saved.
-   **Script**: Scripted indicators use a custom script to collect the data.


</td></tr><tr><td>

Target Type

</td><td>

Type of the target value. The choices are as follows:-   **None**: Use this option if you don’t want to set up any target or threshold for the indicator.
-   **Percentage**: Use this option to determine the indicator result by a percentage value.
-   **Count**: Use this option to determine the indicator result by a count value or total number.


</td></tr><tr><td>

Result if the value meets or exceeds the target value

</td><td>

Result configuration field. The choices are as follows:-   **Passed**
-   **Failed**
 For example, assume you enter `100` in this field. If the indicator result output is more than 100, then the indicator status will pass or fail based on the value configured in this field.

</td></tr><tr><td>

Target

</td><td>

Value to determine if the indicator will pass or fail.

</td></tr><tr><td>

Value mandatory

</td><td>

Option to decide if a value must be compulsory in the indicator task for a manual indicator. **Note:** This option appears only if **Manual** is selected from the **Type** field. This option is automatically selected if **Count** or the **Percentage** is selected from the **Target type** field.

</td></tr><tr><td>

Instructions

</td><td>

Additional instructions for the template.

</td></tr><tr><td class="sub-head" colspan="2">

Supporting Data

</td></tr><tr><td colspan="2">

**Note:** Starting with version 10.1, the actual historical data for the supporting data records from the indicator results or indicator tasks are displayed. Earlier, only the real-time state of the records collected could be viewed.

</td></tr><tr><td>

Collect supporting data

</td><td>

Option to enable collecting supporting data or evidence every time the indicator runs.

</td></tr><tr><td>

Table

</td><td>

Table used for collecting supporting data.

</td></tr><tr><td>

Supporting data fields

</td><td>

Fields of the source table to be used for collecting the supporting data.

</td></tr><tr><td>

Sample size

</td><td>

Minimum number of records that must be used for collecting supporting data.For example, a basic indicator could query a large table, returning thousands of records with each indicator execution. You don't have to save all of them; just a sample of those records. If you enter a sample size of 100, only 100 records are saved, even though the query returned thousands.

</td></tr><tr><td class="sub-head" colspan="2">

Basic Criteria

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

</td></tr><tr class="sub-head"><td class="sub-head" colspan="2">

Schedule

</td></tr><tr><td>

Collection frequency

</td><td>

Collection frequency for indicator results. Indicator tasks and results are generated automatically based on the indicator schedule.

</td></tr><tr><td>

Due date duration \(days\)

</td><td>

Due date duration in days between the creation and due date of the indicator task and generation of its results.The due date duration added to the creation date reflects as the **Due date** of the indicator task.

This field appears only when **Manual** is selected from the **Type** field.

For more information, see [Performance enhancements for Indicator nightly job](../concept/performance-enhancements-indicator-jobs.md).

</td></tr><tr><td>

First run date

</td><td>

First collection time for indicator results. This field is automatically set based on when an indicator or an indicator template runs for the first time. This value in this field cannot be modified.

</td></tr><tr><td>

Next run date

</td><td>

Next run time to collect indicator results of all downstream indicators for this indicator template.

</td></tr></tbody>
</table>5.  When you have completed these entries, you can also view information on the following related lists:

    -   Control Objectives/Risk Statements
    -   Content References
    **Note:** The **Control Objectives/Risk Statements** tab enables you to reuse the same template for multiple control objectives or risk statements, or both of them.

6.  Select **Submit**.


