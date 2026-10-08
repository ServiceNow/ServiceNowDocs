---
title: Create a control indicator using the Compliance Workspace
description: Indicator data for controls, risk, and audit evidence are measured differently depending on the GRC application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/governance-risk-compliance/grc-compliance-management-workspace/create-ctrl-indicator-ws.html
release: australia
product: GRC: Compliance Management Workspace
classification: grc-compliance-management-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Manage control indicators using the Compliance Workspace, Use, GRC Compliance workspace, Use, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Create a control indicator using the Compliance Workspace

Indicator data for controls, risk, and audit evidence are measured differently depending on the GRC application.

## Before you begin

Role required: sn\_compliance\_admin, sn\_compliance\_manager

## Procedure

1.  Navigate to **Workspaces** &gt; **Compliance Workspace**

2.  Select the List icon on the sidebar.

3.  From **Control monitoring** list, navigate to **All indicators**.

4.  Select **New**.

5.  On the form, fill in the fields.

<table id="table_ynl_yjz_dv"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Category

</td><td>

The type of indicator being created. Select **Compliance Indicator** for control indicator.

</td></tr><tr><td>

Inherit from template

</td><td>

Use a selected template to fill in the form.

</td></tr><tr><td>

Template

</td><td>

If you selected the **Inherit from template** check box, select the template you want to use to fill in the form. After you have selected a template, the rest of the fields in the Create New Indicator screen are pre-filled and set to Read-only.

</td></tr><tr><td>

Override template

</td><td>

If you selected the **Inherit from template** check box, and you want to customize your entries in the form, select this check box. You can then edit some or all of the fields on the form.

</td></tr><tr><td>

Name

</td><td>

Name of the indicator.

</td></tr><tr><td>

Description

</td><td>

A description of this indicator.

</td></tr><tr><td>

Entity

</td><td>

Entity associated with this indicator.

</td></tr><tr><td>

Control

</td><td>

Control associated with this indicator.

</td></tr><tr><td>

Owning group

</td><td>

Group that owns the indicator.

</td></tr><tr><td>

Owner

</td><td>

Indicator owner.

</td></tr><tr class="sub-head"><td colspan="2">

Method

</td></tr><tr><td>

Type

</td><td>

Results can be gathered manually using task assignment or automatically using basic filter conditions, Performance Analytics, or a script.-   Manual
-   Basic
-   Script


</td></tr><tr><td>

Target Type

</td><td>

Type of the target value. The choices are as follows:-   **None**: Use this option if you don’t want to set up any target or threshold for the indicator.
-   **Percentage**: Use this option to determine the indicator result by a percentage value.
-   **Count**: Use this option to determine the indicator result by a count value or total number.


</td></tr><tr><td>

Target

</td><td>

Value to determine if the indicator will pass or fail.

</td></tr><tr><td>

Value mandatory

</td><td>

Option to decide if a value must be compulsory in the indicator task for a manual indicator. **Note:** This option appears only if **Manual** is selected from the **Type** field. This option is automatically selected if **Count** or the **Percentage** is selected from the **Target type** field.

</td></tr><tr><td>

Result if the value meets or exceeds the target value

</td><td>

Result configuration field. The choices are as follows:-   **Passed**
-   **Failed**
 For example, assume you enter `100` in this field. If the indicator result output is more than 100, then the indicator status will pass or fail based on the value configured in this field.

</td></tr><tr><td>

Instructions for collecting data

</td><td>

Additional instructions for the collection of indicator results.

</td></tr><tr><td>

Applies to

</td><td>

Entity related to the **Item**.

</td></tr><tr><td>

Last result passed

</td><td>

Option that indicates whether last result passed.

</td></tr><tr class="sub-head"><td colspan="2">

Schedule

</td></tr><tr><td>

Collection frequency

</td><td>

Collection frequency for indicator results. Indicator tasks and results are generated automatically based on the indicator schedule.

</td></tr><tr><td>

Next run date

</td><td>

Next collection time for indicator results.

</td></tr><tr><td>

First run rate

</td><td>

First collection time for indicator results. This field is automatically set based on when an indicator or indicator template runs for the first time. This value in this field can't be modified.

</td></tr><tr><td>

Due date duration \(days\)

</td><td>

Due date duration in days between the creation and due date of the indicator task and generation of its results.The due date duration added to the creation date reflects as the **Due date** of the indicator task.

This field appears only when **Manual** is selected from the **Type** field.

For more information, see [Performance enhancements for Indicator nightly job](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/governance-risk-compliance/grc-compliance-management-workspace/performance-enhancements-indicator-jobs.md).

</td></tr><tr class="sub-head"><td colspan="2">

Supporting Data

</td></tr><tr><td colspan="2">

**Note:** Starting with Version 10.1, the actual historical data for the supporting data records from the indicator results or indicator tasks is displayed. Earlier, only the real-time state of the records collected could be viewed.

</td></tr><tr><td>

Specify supporting data

</td><td>

Option to enable collecting supporting data or evidence every time the indicator runs.This option appears after the indicator is saved.

</td></tr><tr><td>

Source table

</td><td>

Use supporting data to gather supporting evidence from other applications.

</td></tr><tr><td>

Supporting data fields

</td><td>

Supporting data fields based on the selected table.

</td></tr><tr><td>

Sample collection type

</td><td>

 

</td></tr><tr><td>

Sample size

</td><td>

Minimum number of records that must be used for collecting supporting data.For example, a basic indicator could query a large table, returning thousands of records with each indicator execution. You don't have to save all of them; just a sample of those records. If you enter a sample size of 100, only 100 records are saved, even though the query returned thousands.

</td></tr><tr class="sub-head"><td colspan="2">

Basic criteria

</td></tr><tr><td>

Criteria

</td><td>

Use **Set Conditions** to create criteria to filter the data from the source table.

</td></tr><tr><td>

Use reference field

</td><td>

Option to enable the use of the **Reference field**.

</td></tr><tr><td>

Reference field

</td><td>

Connection between the supporting data table and the **Applies to record** field of the entity.

</td></tr><tr class="sub-head"><td colspan="2">

Additional criteria

</td></tr><tr><td colspan="2">

To create indicators with targets, use the advanced filter criteria. This section appears only when you select **Basic** from the **Type** field. This section is used to provide more filter criteria.

</td></tr><tr><td>

Additional criteria

</td><td>

Use **Set Conditions** to add additional criteria.This section only appears when **Percentage** is selected from the **Target type** field.

</td></tr><tr class="sub-head"><td colspan="2">

Settings

</td></tr><tr><td>

Functional domain

</td><td>

Identifies the business function the indicator template belongs to. For example, Cybersecurity and risk, or IT risk and compliance.

</td></tr></tbody>
</table>6.  Select **Submit**.


## What to do next

If you are implementing the [Policy and Compliance Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/governance-risk-compliance/policy-and-compliance-management/policy-compliance-impl-checklist.md) software, you have completed the mandatory setup steps. Return to the [Policy and Compliance Management setup checklist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/governance-risk-compliance/policy-and-compliance-management/policy-compliance-impl-checklist.md) and proceed to the optional steps, as needed.

